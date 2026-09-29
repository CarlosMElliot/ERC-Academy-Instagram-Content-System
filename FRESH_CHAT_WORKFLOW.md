# Fresh Chat Workflow

This is the canonical operating sequence for continuing ERC Academy Instagram content in a new ChatGPT conversation.

## Workflow

**Open repository → Read `START_HERE.md` → Inspect brand documentation + actual visual references → Read `POST_LOG.md` → Check latest handoff → Confirm Test vs. Next Sequential Post → Generate artwork + caption → User review → Publish when authorized → Update log**

### 1. Open the repository
Use this repository as the source of truth. Do not require the user to reteach the ERC Academy system or re-upload reference images already stored here.

### 2. Read `START_HERE.md`
Follow its mandatory reading/review order and current continuation instructions.

### 3. Inspect the brand documentation and actual images
Read the files under `brand/`.

Also inspect:
- `references/REFERENCE_ASSET_MANIFEST.json` first for machine-readable raw image URLs and roles.
- `references/identity/` **first whenever the recurring presenter appears**; this is the primary facial-identity source and overrides full-body assets for facial likeness.
- `references/sample-posts/` for established ERC Academy visual design.
- `references/full-body/` as secondary support for body proportions, clothing fit, posture, pose and composition when the recurring presenter appears.

The repository visual references and written specifications should be used together. If the GitHub connector cannot decode binary PNG/JPEG pixels, enumerate the assets and use their repository/raw URLs where supported by the active image tool. Do not block production or ask for redundant re-uploads solely because the GitHub connector is text-oriented; fall back to the canonical written visual specification when remote-image access is unavailable.

### 4. Read the content strategy and persistent idea/source log
Read:

- `content/aprender-con-ciencia/CONTENT_STRATEGY.md`
- `content/aprender-con-ciencia/CONTENT_IDEA_LOG.md`

Use them to select distinct topics, preserve user-supplied links/references, and prevent repetition across chats and over time.

If the user supplies a link, paper, article, video, book, quote, uploaded file or other source as the basis for a post, log it in `CONTENT_IDEA_LOG.md` and preserve its source/status even if production happens later.

### 5. Read the canonical post log
Read:

`content/aprender-con-ciencia/POST_LOG.md`

Use it to determine the next unused number and avoid duplicates. Never infer publication status from numbering alone.

### 6. Check the latest handoff
Read the newest relevant file under:

`handoff/`

This captures decisions or context that may be newer than older historical documentation.

### 6A. Retrieve presenter pixels when applicable
If the requested artwork includes the recurring ERC Academy presenter, use ERC Academy Publisher before generation. Confirm the canonical identity assets and retrieve the actual highest-priority identity image content with `get_reference_image`. Retrieve relevant full-body assets when needed for proportions, pose, clothing fit, or camera angle. Sample-post assets govern visual/layout continuity.

**Do not generate presenter artwork from metadata or a prose-only facial description when the canonical identity pixels are retrievable.** Do not ask the user to re-upload repository assets that Publisher can retrieve.

### 7. Confirm the production path
Before image generation, ask the user to choose:

**A. Test generation** — generate a non-sequence test for visual/reference fidelity.

**B. Continue the sequence** — generate the next unused Aprender con ciencia post.

At the 2026-09-29 handoff, the expected prompt is:

> **Test generation or continue with #140?**

Always re-check `POST_LOG.md` first. If newer posts have been recorded, suggest the actual next number instead of #140.

A test generation does **not** consume a numbered series slot unless the user explicitly decides to make it an official post.

### 8. Generate the production package
For an official post, prepare together:
- Instagram artwork, normally 4:5 portrait.
- Corresponding Spanish Instagram caption.
- Source/research attribution when applicable.
- Practical PROBALO action.
- Learner-facing CTA.

Maintain ERC Academy's established visual system and use the supplied visual references for continuity.

### 9. Review
Present the result for user review.

If the user requests changes, revise the artwork/caption without advancing the series number.

Do not treat generation or approval as proof of publication.

### 10. Publish only when authorized
When the user authorizes publication, follow:

`publishing/INSTAGRAM_WORKFLOW.md`

Target account: `@erc.nic`.

Check current publisher/account state before publishing and protect against duplicate publication when an earlier attempt has an ambiguous state.

### 11. Update the canonical records
After the final result:
- Update `CONTENT_IDEA_LOG.md` with the final idea/source status.
- Update `POST_LOG.md` with the topic, source, status and relevant notes.
- Create/update the individual post record under `content/aprender-con-ciencia/posts/` when appropriate.
- Record publishing status accurately.
- Advance the next-number state only for an official numbered post.

## Short version

> **Open repo → START_HERE → brand docs + visual references → CONTENT_STRATEGY + CONTENT_IDEA_LOG → POST_LOG → latest handoff → Test or next number? → artwork + caption → review → authorized publish → update logs.**

This workflow is designed so ERC Academy content can continue cleanly across fresh ChatGPT conversations.
