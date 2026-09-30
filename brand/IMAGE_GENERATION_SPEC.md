# ERC Academy Image Generation Specification

## Required output
- Standard Instagram feed artwork defaults to vertical 4:5.
- Follow `BRAND_GUIDE.md`.
- Use approved visual references when available.
- When the recurring presenter appears, **retrieve the actual `references/identity/` image pixels first through ERC Academy Publisher `get_reference_image`**. The identity collection is the primary and highest-priority source for facial likeness. Metadata, filenames, or prose descriptions alone do not satisfy this requirement when the canonical pixels are retrievable.
- Use `references/full-body/` secondarily for body proportions, clothing fit, posture, pose and composition. If facial appearance conflicts, the identity collection wins.
- Use `references/sample-posts/` for ERC Academy layout, color, lighting and graphic continuity.
- Preserve visual continuity while creating a fresh pose/composition.
- Every post also needs a corresponding Spanish Instagram caption.

## Design skeleton
Use a deep navy/royal-blue background, electric-blue diagonal accents, restrained gold dividers, white ERC ACADEMY header, APRENDER CON CIENCIA numbering, oversized cyan/white headline, concise explanatory copy, cyan PROBALO section, strong CTA, source footer and ercacademynic.com.

## Lighting
Dark studio look. Keep exposure, brightness, contrast, saturation, HDR and glow restrained. Do not brighten beyond approved samples.

## Copy density
Keep poster copy scannable on a phone. Put extra context in the caption.

## Quality check
Before approval confirm: when the presenter appears, canonical identity pixels were actually retrieved before generation; numbering is correct; title hierarchy is readable; continuity with approved visual references is acceptable; no accidental brightness/contrast increase; no text collision; topic is not an accidental duplicate; source is present when needed; CTA is present; and a Spanish caption is prepared.


## Reference handoff capability boundary
Retrieving or rendering a canonical image through ERC Academy Publisher proves that ChatGPT can inspect that asset, but it does **not** by itself prove that the built-in image generator received the asset as a conditioning/reference image.

For likeness-critical presenter generation, distinguish these states:

1. **Registered** — the asset appears in `list_reference_images`.
2. **Retrieved/rendered** — `get_reference_image` returned actual pixels to ChatGPT.
3. **Generator-attached** — the active image-generation interface received those pixels as an actual reference input.

Only state 3 is sufficient to claim that generation is conditioned on the canonical identity image. If the active image-generation interface cannot accept Publisher-returned MCP image content as a reference input, do not silently fall back to a prose description and do not claim repository-only identity conditioning worked.

### Multi-reference target
When supported by the active image-generation interface, provide multiple actual reference inputs with explicit roles:

- **Identity authority:** highest-priority asset(s) from `references/identity/` for facial likeness.
- **Pose/body authority:** one or more selected assets from `references/full-body/` for proportions, clothing fit, posture, gesture, camera angle, and pose inspiration.
- **Style authority:** one or more selected assets from `references/sample-posts/` for ERC layout, color, typography hierarchy, lighting, PROBALO/CTA treatment, and footer behavior.

The identity reference always wins facial conflicts. Full-body assets must not override facial identity, and sample posts must not be used as identity references.

### Current verified limitation (2026-09-29)
The current ChatGPT session verified that Publisher v1.0.21 can return the canonical identity pixels and ChatGPT can render them. However, those MCP-returned pixels were not automatically forwarded into the built-in image generator as a reference input. A direct conversation image attachment of the same identity sheet did successfully produce substantially stronger likeness.

Until a supported Publisher/MCP → image-generator reference handoff is verified, keep GitHub/Publisher as the canonical asset library but treat direct generator attachment as the known-good path for likeness-critical generation. Do not repeatedly generate from text after a reference-handoff failure.


## No-API ChatGPT reference bridge status (2026-09-30)

The project must not require the OpenAI API for ERC artwork generation. Keep generation inside ChatGPT's native image-generation experience and keep ERC Academy Publisher focused on canonical reference retrieval and Instagram publishing.

Verified behavior:
- Publisher v1.0.21 successfully retrieves canonical GitHub image bytes and returns MCP image content.
- ChatGPT can inspect the returned reference image, but direct attempts in the current chat to forward that MCP ImageContent/data URI into the native image generator failed at the host/RPC handoff boundary.
- A normal conversation image attachment of the canonical identity sheet remains verified to produce strong presenter likeness.

Do **not** modify the working Publisher encoding/retrieval logic merely to work around this host boundary, and do not add an OpenAI API dependency.

### Supported avenue still to test
Current ChatGPT plugin documentation describes a supported UI/file route in which widget state can expose `imageIds` to the model on later turns. Those IDs must come from ChatGPT-supported file sources such as `window.openai.uploadFile`, `window.openai.selectFiles`, tool-input file parameters, or tool-result file references. This is distinct from returning raw MCP ImageContent.

Therefore the next engineering experiment, if pursued, is a **Publisher UI/file-reference bridge**, not another Base64/MIME rewrite: determine whether canonical GitHub references can be surfaced through a supported ChatGPT file reference and then placed in widget-state `imageIds`. Treat this as experimental until an end-to-end test proves the native generator actually receives the images.

Until that is verified, do not claim fully automatic GitHub → Publisher → native-image-generator conditioning.
