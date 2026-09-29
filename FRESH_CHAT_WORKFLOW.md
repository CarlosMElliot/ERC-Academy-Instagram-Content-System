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
- `Sample ERC_Instagram_Posts/` for established ERC Academy visual design.
- `Full Body Shots/` when the recurring presenter appears in the artwork.

The actual visual references should be used together with the written specifications.

### 4. Read the canonical post log
Read:

`series/aprender-con-ciencia/POST_LOG.md`

Use it to determine the next unused number and avoid duplicates. Never infer publication status from numbering alone.

### 5. Check the latest handoff
Read the newest relevant file under:

`handoff/`

This captures decisions or context that may be newer than older historical documentation.

### 6. Confirm the production path
Before image generation, ask the user to choose:

**A. Test generation** — generate a non-sequence test for visual/reference fidelity.

**B. Continue the sequence** — generate the next unused Aprender con ciencia post.

At the 2026-09-29 handoff, the expected prompt is:

> **Test generation or continue with #140?**

Always re-check `POST_LOG.md` first. If newer posts have been recorded, suggest the actual next number instead of #140.

A test generation does **not** consume a numbered series slot unless the user explicitly decides to make it an official post.

### 7. Generate the production package
For an official post, prepare together:
- Instagram artwork, normally 4:5 portrait.
- Corresponding Spanish Instagram caption.
- Source/research attribution when applicable.
- Practical PROBALO action.
- Learner-facing CTA.

Maintain ERC Academy's established visual system and use the supplied visual references for continuity.

### 8. Review
Present the result for user review.

If the user requests changes, revise the artwork/caption without advancing the series number.

Do not treat generation or approval as proof of publication.

### 9. Publish only when authorized
When the user authorizes publication, follow:

`publishing/INSTAGRAM_WORKFLOW.md`

Target account: `@erc.nic`.

Check current publisher/account state before publishing and protect against duplicate publication when an earlier attempt has an ambiguous state.

### 10. Update the canonical records
After the final result:
- Update `POST_LOG.md` with the topic, source, status and relevant notes.
- Create/update the individual post record under `series/aprender-con-ciencia/posts/` when appropriate.
- Record publishing status accurately.
- Advance the next-number state only for an official numbered post.

## Short version

> **Open repo → START_HERE → brand docs + visual references → POST_LOG → latest handoff → Test or next number? → artwork + caption → review → authorized publish → update log.**

This workflow is designed so ERC Academy content can continue cleanly across fresh ChatGPT conversations.
