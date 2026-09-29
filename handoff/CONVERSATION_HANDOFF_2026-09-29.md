# Conversation Handoff — 2026-09-29

This document records the final decisions from the repository migration/audit conversation so a future chat can continue without reconstructing those decisions.

## Repository state

Repository: `CarlosMElliot/ERC-Academy-Instagram-Content-System`

The repository was intentionally made public by the user. The user explicitly authorized the included visual reference images to remain in the repository.

At the final audit, the repository contained:
- `references/full-body/` — 25 PNG presenter/body reference images.
- `references/sample-posts/` — 10 PNG ERC Academy post/style examples.
- `brand/` — brand, generation and template documentation.
- `content/aprender-con-ciencia/` — series specification, historical context and canonical post log.
- `publishing/` — account/link reference and publishing workflow.
- `README.md` and `START_HERE.md` — repository orientation and mandatory handoff instructions.

## Visual-reference decision

The repository images are intended to eliminate repeated re-uploading of the same references in future chats.

When creating artwork with the recurring presenter:
- consult `references/full-body/` for established appearance, proportions, posture, clothing fit and useful angles;
- create new poses/compositions rather than copying a reference pose mechanically;
- rotate front-facing, three-quarter, profile, walking, pointing, presenting, crossed-arms, hands-in-pockets, seated, listening, writing, demonstrating and prop-interaction compositions as appropriate.

For visual design:
- consult `references/sample-posts/` as the strongest examples of the established ERC Academy visual language;
- preserve the dark navy/royal-blue environment, cyan/electric-blue accents, restrained gold details, bold white/cyan hierarchy, practical PROBALO section, strong CTA and restrained professional lighting;
- do not unnecessarily increase brightness, contrast, saturation, HDR or glow.

## Generation decision

Before creating a new image, confirm which path the user wants:

1. **Test generation** — verify visual/reference fidelity without consuming an official series number.
2. **Continue the sequence** — create the next unused Aprender con ciencia number from `POST_LOG.md`.

When appropriate, explicitly suggest the next number.

At this handoff point, the sequence had reached #139 and #140 was the intended next number unless `POST_LOG.md` has since changed.

A test must not consume a numbered slot unless the user explicitly chooses to make it an official numbered post.

## Production package

For an official Aprender con ciencia post, prepare:
- the 4:5 Instagram artwork by default;
- its corresponding Spanish Instagram caption;
- concise poster copy with additional context moved to the caption;
- source/research attribution when applicable;
- natural Nicaraguan voseo where appropriate;
- a practical PROBALO activity and learner-facing CTA.

Treat image + caption as one production package.

## Publishing

Target account: `@erc.nic`.

Do not infer that a generated or approved post was published. Follow `publishing/INSTAGRAM_WORKFLOW.md` and check current publisher state before a live operation. Avoid duplicate publication when an earlier upload/publish attempt has an ambiguous state.

## Portability objective

The user's goal is that a fresh chat can open this repository, read `START_HERE.md`, inspect the supplied visual references, consult the canonical post log and immediately continue ERC Academy content production without requiring the user to reteach the brand or upload the same reference images again.


## Publisher visual bridge update

The ERC Academy Publisher visual-reference bridge was repaired and verified on version **1.0.21**. The Publisher now loads the current repository manifest dynamically and `get_reference_image` can return the actual canonical image content to ChatGPT. The former stale `.png.png` identity path issue was corrected to `references/identity/reference-sheet-01.png`.

Future presenter generation should therefore retrieve the actual highest-priority identity pixels through Publisher before image generation instead of relying on metadata or a written facial description. New normal reference assets may be added by uploading the image and updating `REFERENCE_ASSET_MANIFEST.json`; they should then be verified with `list_reference_images` and, when pixel-level use is intended, `get_reference_image`. A normal reference addition should not require a Worker redeploy or plugin reinstall.

The repository now carries the detailed operating instructions. A fresh chat only needs a short bootstrap request pointing it to this repository and instructing it to follow README/fresh-chat workflow; the user does not need to reproduce the full brand/image-generation prompt each time.
