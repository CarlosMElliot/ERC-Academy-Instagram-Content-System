# Visual Reference Asset Manifest

This repository contains three canonical visual-reference collections. Identity, full-body, and sample-post assets have distinct roles and must be used together when relevant.

## Primary Identity Reference

Path: `references/identity/`

Current canonical asset: `reference-sheet-01.png.png`.

Purpose: **primary presenter facial-identity reference**. Use this collection first whenever the recurring ERC Academy presenter appears. It governs facial structure, round black glasses, curly dark hairstyle, beard/mustache, skin appearance, expression range, and front/three-quarter/profile facial continuity.

Identity priority rule: **identity references override full-body references for facial likeness**. Full-body assets remain supporting references for body proportions, clothing fit, posture, pose and composition. Sample posts remain the reference for ERC graphic/layout identity.

Do not treat a generated or older full-body face as more authoritative than the dedicated identity collection when there is a conflict.

## Full Body Shots

Path: `references/full-body/`

Count at the 2026-09-29 audit: **25 PNG files**.

Purpose: recurring-presenter continuity. Use these references for established appearance, body proportions, posture, clothing fit, profile/three-quarter angles, walking poses, presenting gestures and full-body composition.

These files are references, not pose templates. Preserve continuity while creating a new composition appropriate to each post.

## Sample ERC Instagram Posts

Path: `references/sample-posts/`

Count at the 2026-09-29 audit: **10 PNG files**.

Purpose: visual-style continuity. These are the primary examples for ERC Academy's Instagram design language, including layout, color balance, typography hierarchy, restrained dark lighting, cyan/blue accents, gold details, PROBALO treatment, CTA placement and footer behavior.

## Priority

For presenter likeness, use this order: **`references/identity/` → `references/full-body/` → written historical descriptions**. For ERC graphic/layout identity, use `references/sample-posts/` together with the brand specifications.

When written instructions and old historical descriptions are too abstract to settle a visual decision, inspect the current sample images. For series numbering, publishing state and editorial history, the written canonical files remain authoritative.

## Public-repository status

The user explicitly authorized these visual references to be stored in this public repository.


## Binary-access behavior

These files remain the canonical visual assets even when a particular GitHub connector can only enumerate them rather than decode their pixel data.

For future chats:
- preserve and use the repository paths/raw GitHub URLs as the canonical locations;
- prefer direct remote-reference use when the active image-capable tool supports URLs;
- do not require the user to re-upload assets already stored here merely because a text connector cannot render them;
- use the written brand/generation specifications and this manifest as the production fallback;
- request a manual upload only for a specific pixel-level comparison that cannot be achieved through repository/raw URL access.

This policy removes binary-connector limitations as a general production blocker while keeping claims about actual pixel inspection accurate.

## Machine-readable visual manifest

Canonical machine-readable index: `references/REFERENCE_ASSET_MANIFEST.json`.

It contains the canonical reference assets across **identity + presenter/full-body + sample-post** collections, including:
- stable asset ID;
- collection/role;
- repository path;
- raw GitHub URL;
- GitHub browser URL;
- blob SHA;
- byte size;
- usage guidance and priority.

### Remote-reference startup procedure

1. Read the JSON manifest before image generation.
2. When the recurring presenter is used, load the `identity` collection first as the primary facial-likeness source.
3. Select relevant `presenter`/full-body assets as secondary support for proportions, clothing fit, posture and pose.
4. Select multiple relevant `sample_post` assets for graphic/layout continuity.
5. Attempt to give the selected `raw_url` values directly to the active image-capable environment if it accepts remote image references.
6. A text-only GitHub connector failing to decode the binary is not evidence that the asset is unavailable publicly.
7. Never claim that pixels were inspected unless the image-capable environment actually rendered them.

The JSON manifest is intended to make visual-reference handoff deterministic and machine-readable across fresh chats.