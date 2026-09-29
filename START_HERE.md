# START HERE — New Chat / Model Handoff

You are working on ERC Academy social-media content. **Do not ask the user to re-explain the brand or re-upload the reference images before reading this repository.**

## Mandatory reading/review order

First read `FRESH_CHAT_WORKFLOW.md` for the end-to-end operating sequence.

1. `brand/BRAND_GUIDE.md`
2. `brand/IMAGE_GENERATION_SPEC.md`
3. Review/enumerate `references/identity/` first whenever the recurring presenter appears. This is the primary facial-identity source and overrides full-body references for facial likeness.
4. Review/enumerate the visual examples in `references/sample-posts/`; use their repository/raw URLs directly when the active image environment supports them, otherwise use the canonical written visual specification without blocking production
5. Review/enumerate the presenter references in `references/full-body/` when the artwork includes the recurring presenter; use repository/raw URLs directly when supported
10. `content/aprender-con-ciencia/SERIES_SPEC.md`
6. `content/aprender-con-ciencia/CONTENT_STRATEGY.md`
7. `content/aprender-con-ciencia/CONTENT_IDEA_LOG.md`
8. `content/aprender-con-ciencia/POST_LOG.md`
9. `content/aprender-con-ciencia/HISTORICAL_CONTEXT.md`
11. `brand/POST_TEMPLATE.md`
13. `publishing/ACCOUNT_AND_LINKS.md`
12. `publishing/INSTAGRAM_WORKFLOW.md`
14. `references/REFERENCE_ASSET_MANIFEST.md` and `references/REFERENCE_ASSET_MANIFEST.json` — use the JSON manifest first when an image-capable environment can consume remote URLs
15. Read the latest file in `handoff/` for migration/session decisions
16. When relevant, inspect individual records under `content/aprender-con-ciencia/posts/`

## How to use the image folders

### `references/identity/` — PRIMARY IDENTITY SOURCE
Use this folder first whenever the recurring presenter appears. It is authoritative for facial likeness: facial structure, glasses, hairstyle, beard/mustache, expression range, and front/three-quarter/profile continuity. If a full-body reference conflicts with this identity set on facial appearance, follow `references/identity/`.

### `references/sample-posts/`
Treat these as the strongest visual-style references. Match their established ERC Academy design language: dark navy/royal-blue environment, cyan/electric-blue accents, restrained gold details, bold white/cyan hierarchy, practical PROBALO section, strong CTA and restrained professional lighting.

Do not simply copy one sample. Preserve the system while varying topic, layout, visual metaphor, pose and composition.

### `references/full-body/`
Use these images as secondary support to maintain continuity of the recurring presenter, including established appearance, body proportions, posture, clothing fit and useful viewing angles. Use them as reference material rather than a requirement to duplicate the exact pose.

Rotate poses naturally: front-facing, three-quarter, profile, walking, pointing, presenting, crossed arms, hands in pockets, seated, listening, writing, demonstrating, holding a notebook/clipboard/laptop, or interacting with visual elements.

## Mandatory choice before image generation

Before generating a new image, confirm which path the user wants:

**A. Test generation** — make a non-sequence test to verify visual/reference fidelity.

**B. Continue the series** — use the next unused sequential Aprender con ciencia number from `POST_LOG.md`.

When useful, explicitly suggest the next number. In the current handoff state, the intended next number is **#140**, unless `POST_LOG.md` has been updated.

Do not consume a numbered series slot for a test unless the user explicitly asks to make the test an official numbered post.

## Default production behavior

- Standard Instagram feed artwork defaults to **4:5 portrait** unless the user requests another ratio.
- Preserve the established ERC Academy visual system.
- Preserve the recurring presenter's established appearance/proportions when using the presenter references.
- Create a fresh pose/composition rather than mechanically copying a reference pose.
- Keep the approved restrained dark studio lighting. Do not unnecessarily increase brightness, contrast, saturation, HDR or glow.
- Prepare the **image and its corresponding Spanish Instagram caption together**.
- Use natural Nicaraguan voseo where appropriate.
- Keep science-related claims appropriately sourced and avoid overclaiming.
- Poster copy should remain concise/mobile-readable; move extra explanation to the caption.
- Before publishing, inspect the post log and current publisher state to prevent duplicates.

## Publishing behavior

Target Instagram account: **@erc.nic**.

A generated post is not automatically evidence that it was published. Follow `publishing/INSTAGRAM_WORKFLOW.md`. If an upload/publish result is ambiguous, check its existing state rather than blindly creating a duplicate.

When the user authorizes a post or an authorized batch, prepare/publish the corresponding artwork and caption according to the current publisher capabilities and then update the post log.

## Current working state

- Instagram: `@erc.nic`
- Current working sequence reached: **#139**
- Intended next new post: **#140**, subject to `POST_LOG.md`
- #139 was generated/approved in the latest recovered working context; its publication state was previously pending/unconfirmed.
- Historical status is not perfectly linear. Never infer publication solely from the number.

## Portability goal

This repository is the canonical ERC Academy Instagram-content handoff. A new chat should be able to read these files and visual references and continue the project without making the user repeatedly teach the brand or re-upload the same reference images.


## Repository-first binary asset handling

The GitHub connector may enumerate PNG/JPEG assets and expose repository/raw URLs while still being unable to decode binary pixels itself. That limitation must not automatically stop ERC Academy production.

- Do not ask the user to re-upload existing repository references just because the GitHub connector is text-oriented.
- Use the canonical written descriptions, manifest, handoff, and post records together with the enumerated repository asset paths.
- Read `references/REFERENCE_ASSET_MANIFEST.json` and pass its `raw_url` values to an image-capable environment when that environment supports remote references. Prefer several sample-post references plus several presenter references rather than relying on a single image.
- If remote binary references are unsupported, continue from the canonical visual specification unless the user explicitly needs pixel-perfect matching to a specific source image.
- Never claim pixel-level inspection unless the active tool actually rendered the image.
