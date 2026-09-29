# ERC Academy Instagram Content System

Canonical source of truth for ERC Academy's Instagram content system and the **Aprender con ciencia** series.

This repository is designed so a fresh ChatGPT conversation can understand **where to start, how ERC content should look, where new ideas come from, what has already been used, how publishing works, and how to continue the series without the user rebuilding the context manually.**

## Start here

For a new conversation, use this order:

1. **`FRESH_CHAT_WORKFLOW.md`** — the end-to-end operating procedure.
2. **`START_HERE.md`** — the detailed model/chat handoff and mandatory reading order.
3. Follow the workflow into the brand, references, content-memory and publishing folders.

The short production flow is:

> **Open repo → workflow/handoff → brand + visual references → content strategy + idea log → post log → latest handoff → Test or next post? → research/develop → artwork + caption → review → authorized publish → update logs.**

---

## Project at a glance

This repository is the **production-ready, canonical source of truth** for ERC Academy's Instagram content system. It is designed to let a fresh chat continue the project without rebuilding the brand, history, references or workflow from scratch.

- **Brand system** — preserves ERC Academy's visual language, layout, Spanish caption style, tone and image-generation rules.
- **Presenter visual model** — includes 25 full-body reference images for identity continuity while allowing new poses, camera angles and compositions.
- **Visual examples** — includes established ERC Academy sample posts for layout and graphic-style continuity.
- **Content strategy** — defines where new ideas come from and how research is translated into useful English-learning content.
- **Source and idea memory** — new links, research, books, files and ideas are persisted in the repository instead of living only in chat history.
- **Anti-repetition system** — checks prior topics, claims, exercises, sources, headlines and visual concepts before developing new content.
- **Protected numbering** — official post history is tracked so numbers are not accidentally reused; the current intended continuation point is **#140** unless `POST_LOG.md` has since changed.
- **Test vs. official workflow** — before image generation, determine whether the user wants a test generation or the next official sequential post. Tests do not consume official numbers unless explicitly promoted.
- **Artwork + caption package** — official content is developed as both the visual post and its corresponding Spanish Instagram caption.
- **Publishing workflow** — tracks preparation/publication state and includes duplicate-publishing safeguards.
- **Fresh-chat onboarding** — README, `FRESH_CHAT_WORKFLOW.md` and `START_HERE.md` tell a new chat exactly how to initialize itself.
- **Persistent repository maintenance** — meaningful new project information must be written back to the appropriate GitHub log/document before work is considered complete.
- **README maintenance** — this overview and operating documentation should be updated when major structure, capability, limitation or cross-cutting workflow rules change.
- **Portable template mode** — a clone can be reconfigured for another project, brand, Instagram account or numbering sequence with **`REINITIALIZE_PROJECT`**, while the canonical ERC Academy repository is protected from silent reset.
- **Known historical limitation** — posts **#102–138** are protected/reserved in the post log but are not all individually reconstructed under `posts/`. They must not be reused, and missing historical details must not be invented.

**In short:** the repository stores the **brand + presenter + references + research memory + content history + numbering + publishing workflow + future-chat instructions** needed to keep ERC Academy's Instagram system continuous across conversations.

---

## How to start a fresh ChatGPT chat

You should not need to re-explain ERC Academy or re-upload the reference images already stored in this repository.

Start a new chat with:

> Continue my ERC Academy Instagram content system from this repository:
> https://github.com/CarlosMElliot/ERC-Academy-Instagram-Content-System
>
> Read the README and follow the repository's fresh-chat workflow. Use the repo as the source of truth, including its brand rules, visual references, content strategy, idea/source log, post history, and publishing workflow. Then tell me the current status and ask me whether I want a test generation or the next official Aprender con ciencia post.

The expected sequence is:

> **Repo → README → Fresh Chat Workflow → Start Here → brand + references → content strategy → idea/source log → post log → latest handoff → current status → Test or next official post?**

After initialization, continue naturally. Examples: **“Continue with the next post”** or **“Use this research link as inspiration for a future post.”** When a source is supplied for future content, preserve it in the repository's content idea/source log according to the content strategy.

---

## Supplying new research links, files, or references

You do **not** need to edit the repository manually when you find a new source. Paste the link directly into the ChatGPT conversation, upload the source file, or identify the book/article/video/reference and state what you want done with it.

Examples:

> Use this as a reference/source for a future Aprender con ciencia post: [paste link]

> Use this source for the next Aprender con ciencia post: [paste link]

> Save this for later. Do not create a post yet: [paste link]

### Required repository logging behavior

When the user supplies a new source intended for ERC Academy content, the working chat should **persist it in this repository**, not leave it only in conversation history.

1. Read/inspect the source when available.
2. Check `content/aprender-con-ciencia/CONTENT_IDEA_LOG.md` and `POST_LOG.md` for an existing matching source or substantially repeated teaching idea.
3. Add or update an entry in `CONTENT_IDEA_LOG.md` with the source/link or stable identifier, date, proposed topic/claim, topic family, status and notes.
4. Use `INBOX` or `HOLD` when the source is only being saved for later. This does **not** consume an official post number.
5. When the source becomes an official post, update the same idea entry to `USED`, connect it to the post number, update `POST_LOG.md`, and create/update `posts/[NUMBER].md`.
6. Preserve used, rejected, merged and held entries. Do not erase them, because the history is part of the anti-repetition system.
7. If the source cannot be opened or verified, log that limitation instead of inventing its contents.

Multiple links or uploaded references may be supplied in one chat. Each meaningful source should remain traceable in the repository.

This means the repository—not an individual ChatGPT conversation—is the durable memory for ERC Academy content sources, ideas and official posts.

---

## How to use the visual reference library

The visual-reference folders have **two different jobs** and should be used together when producing new ERC Academy artwork.

### `references/full-body/` — presenter identity and pose reference

The 25 full-body images are the canonical visual-model reference set for the recurring ERC Academy presenter. They are not merely archived photos and they are **not pose templates that must be copied literally**.

When the image-generation environment can access these references, inspect multiple relevant images to preserve recognizable continuity such as facial structure, round black glasses, curly dark hair, short beard/mustache, body proportions, clothing fit and the presenter's overall appearance.

Use that identity reference to create **new, natural poses and camera angles** appropriate to each post. Valid variation includes front-facing, three-quarter views, profile views, walking, crossed arms, hands in pockets, pointing or presenting, sitting, listening, writing, demonstrating, holding a notebook/clipboard/laptop, interacting with educational graphics, and placing the presenter on either side of the composition.

Do **not** force every new image to reproduce the exact pose of one reference photograph. The goal is **identity continuity with pose/composition variety**.

### `references/sample-posts/` — ERC graphic and layout identity

The sample-post images define the established visual language of the series: dark navy/royal-blue environment, cyan/electric-blue framing, restrained gold accents, typography hierarchy, headline treatment, PROBALO section, CTA placement, source/footer treatment, spacing, density and overall professional/scientific mood.

In practical terms:

> **Full-body references = what the presenter should look like.**  
> **Sample-post references = what an ERC Academy post should look like.**

Use both together with `brand/BRAND_GUIDE.md` and `brand/IMAGE_GENERATION_SPEC.md`.

### Repository-first visual-reference rule

The repository is the canonical home for ERC Academy visual references. A fresh chat should **not ask the user to re-upload reference images simply because the GitHub connector cannot return binary PNG bytes**.

Use the reference system in this order:

1. Read the written canonical descriptions in `BRAND_GUIDE.md`, `IMAGE_GENERATION_SPEC.md`, `REFERENCE_ASSET_MANIFEST.md`, the latest handoff, and any detailed post records.
2. Enumerate the actual files in `references/sample-posts/` and `references/full-body/` and retain their repository paths/raw GitHub URLs as the canonical asset locations.
3. If the active image-generation or multimodal environment can consume those repository/raw URLs directly, use them.
4. If the current connector can only enumerate binary assets but cannot render their pixels, continue production from the canonical written visual specification and repository asset metadata instead of blocking the workflow or asking the user to re-upload the same files.
5. Only request a manual re-upload when the user specifically requires pixel-level fidelity from a particular reference **and** the active image tool cannot accept repository/raw URLs or otherwise access that image.

Do not falsely claim pixel-level inspection when the tool did not render the file. However, inability of the GitHub text connector to decode PNG bytes is **not by itself a reason to stop production**.

---

## Persistent maintenance contract — mandatory for every future chat

This repository is intended to be **self-maintaining documentation and durable project memory**. A chat that creates, approves, changes, publishes, rejects, researches, or otherwise materially changes ERC Academy Instagram work must not leave the new state only in conversation history.

### Hardcoded end-of-work rule

Before considering any ERC Academy content task complete, the working chat must ask:

> **What new durable information was created in this chat, and which repository files must be updated so the next fresh chat can recover it without relying on conversation memory?**

Then update the repository as appropriate.

At minimum:

- New source, research link, book, article, video, uploaded reference, or content idea → update `content/aprender-con-ciencia/CONTENT_IDEA_LOG.md`.
- New official/approved numbered post → update `POST_LOG.md` and create/update `posts/[NUMBER].md`.
- Publication attempt/result/state → update the relevant post record and publishing/history documentation when materially useful.
- New brand, presenter, visual, caption, editorial, numbering, workflow, or publishing rule → update the canonical file that owns that rule.
- New visual reference asset → update `references/REFERENCE_ASSET_MANIFEST.md` and the relevant reference folder.
- Important cross-cutting behavior that a human or fresh chat needs to know → update this `README.md`, `FRESH_CHAT_WORKFLOW.md`, and/or `START_HERE.md` as appropriate.
- Major session decisions or migrations that are not captured cleanly elsewhere → update the latest handoff or create a new dated handoff.

**Do not update README for every tiny post detail.** README is the stable map and operating contract. Update it automatically when repository structure, startup instructions, durable operating rules, major capabilities, limitations, or cross-cutting behavior changes. Post-specific data belongs in the logs and post records.

### Fresh-chat preservation prompt

Every fresh chat should treat the following as a standing instruction after reading this repository:

> **Use this repository as the durable source of truth for the ERC Academy Instagram content system. Read and follow README.md, FRESH_CHAT_WORKFLOW.md and START_HERE.md before doing production work. Do not make me re-teach information already stored here or re-upload reference assets merely because a text-oriented GitHub connector cannot decode PNG bytes; use the repository-first visual-reference rule. Before image generation, determine whether I want a test generation or the next official sequential Aprender con ciencia post. Inspect the brand rules and accessible visual references before generating. When I provide a new link, research source, file, content idea, visual reference, approval, publication result, workflow change, or other durable project information, persist it to the correct repository log/document instead of leaving it only in chat history. Check existing logs before creating content so topics, sources and post numbers are not accidentally repeated. At the end of meaningful work, reconcile the repository so the next fresh chat can continue from it without depending on this conversation.**

This instruction is part of the repository's operating contract and should remain present when the documentation is revised.

### Current completeness / known historical gap

The system is ready for continued production and currently preserves the brand system, presenter references, sample-post visual language, content strategy, source/idea memory, numbering state, publishing workflow and fresh-chat handoff behavior.

The known historical gap is that posts **#102–138 are reserved in `POST_LOG.md` but are not all individually reconstructed as files under `posts/`**. Their numbers must not be reused. This gap does not block continuation of the sequence. Backfill those individual historical records only when reliable source material is available; do not invent missing details.

---

## Clone / new-project reset command — portable template mode

This repository may be cloned or copied for a **different project, brand, content series, or Instagram account**. To make that safe and reusable, the following explicit keyword is reserved:

> **REINITIALIZE_PROJECT**

When the user enters **REINITIALIZE_PROJECT** in a chat working from a clone/copy of this repository, treat it as a request to enter **template reconfiguration mode**.

### What the command means

Do **not** assume the ERC Academy identity, `@erc.nic`, the Aprender con ciencia numbering, existing post history, presenter identity, links, or publishing account should carry into the new project.

Instead:

1. Confirm the repository being edited is the intended **clone/copy/new project**, not the canonical ERC Academy production repository.
2. Ask for only the missing new-project values needed to initialize it: project/brand name, Instagram account, website/links if applicable, series name, desired starting post number, visual identity/reference assets, language/tone, and publishing configuration.
3. Reconfigure the canonical documentation and logs for the new project.
4. Reset numbering to the user-selected starting number. If no starting number is specified, ask rather than guessing.
5. Clear or archive inherited post/idea history so ERC Academy history cannot be mistaken for the new project's history.
6. Replace inherited account-specific links, handles, presenter rules and publishing metadata with the new project's values.
7. Preserve the **generic workflow architecture**: README onboarding, fresh-chat workflow, source/idea logging, anti-repetition checks, post records, reference manifest, publishing-state tracking and repository-maintenance contract.
8. Update README and the relevant canonical files so future chats immediately recognize the new project rather than ERC Academy.
9. Never publish, delete remote assets, or modify an external account merely because this keyword was entered. Publishing/account actions still require the normal authorization/workflow.

### Safety lock for the canonical ERC Academy repository

**REINITIALIZE_PROJECT must never silently reset this canonical repository: `CarlosMElliot/ERC-Academy-Instagram-Content-System`.**

If the keyword is entered while working in the canonical ERC Academy repository, first require explicit confirmation that the user intentionally wants to repurpose the canonical repository itself. Prefer using the command on a clone/new repository so ERC Academy history remains intact.

### Optional one-line configuration

The keyword can include configuration in the same message, for example:

> **REINITIALIZE_PROJECT — Brand: Example Academy; Instagram: @example; Series: Learning Lab; Start number: 1; Language: Spanish**

Use supplied values directly and ask only for information that is genuinely missing.

This makes the repository architecture reusable without hard-locking future clones to ERC Academy's account, numbering, visual model or historical content.

---

## Repository structure

```text
ERC-Academy-Instagram-Content-System/
│
├── README.md
├── FRESH_CHAT_WORKFLOW.md
├── START_HERE.md
│
├── brand/
│   ├── BRAND_GUIDE.md
│   ├── IMAGE_GENERATION_SPEC.md
│   └── POST_TEMPLATE.md
│
├── references/
│   ├── REFERENCE_ASSET_MANIFEST.md
│   ├── REFERENCE_ASSET_MANIFEST.json
│   ├── full-body/
│   │   └── 25 presenter reference PNGs
│   └── sample-posts/
│       └── 10 ERC Academy Instagram sample PNGs
│
├── content/
│   └── aprender-con-ciencia/
│       ├── SERIES_SPEC.md
│       ├── CONTENT_STRATEGY.md
│       ├── CONTENT_IDEA_LOG.md
│       ├── POST_LOG.md
│       ├── HISTORICAL_CONTEXT.md
│       └── posts/
│           └── 139.md
│
├── publishing/
│   ├── ACCOUNT_AND_LINKS.md
│   ├── INSTAGRAM_WORKFLOW.md
│   └── PUBLISHER_DIAGNOSTIC_2026-09-28.md
│
└── handoff/
    └── CONVERSATION_HANDOFF_2026-09-29.md
```

---

## What each root file does

### `FRESH_CHAT_WORKFLOW.md`
The **operating procedure**. It tells a fresh chat what to do from the moment it opens the repository through topic selection, generation, review, publishing and updating the logs.

This is the best first file for a model that needs to **do work**.

### `START_HERE.md`
The **context handoff**. It tells a new model what must be read, how to use the image references, the test-vs-official-post rule, current sequence state, production defaults and portability expectations.

### `README.md`
The **map of the repository**. It explains what every folder/file is for and where a human or model should begin.

---

## `brand/` — What ERC content should look and sound like

### `brand/BRAND_GUIDE.md`
Defines the ERC Academy visual/editorial identity: dark navy/royal-blue environment, electric blue/cyan accents, restrained gold, typography hierarchy, CTA/footer behavior, tone, Nicaraguan voseo and caption philosophy.

### `brand/IMAGE_GENERATION_SPEC.md`
Defines the image-production rules and quality checks: default 4:5 feed format, visual skeleton, restrained lighting, copy density, continuity requirements and pre-approval checks.

### `brand/POST_TEMPLATE.md`
Reusable structure for an Aprender con ciencia post: number, topic, source, headline, explanation, visual concept, PROBALO, CTA, footer, caption and generation notes.

---

## `references/` — What the established brand actually looks like

### `references/REFERENCE_ASSET_MANIFEST.md`
Explains what the image collections contain, why they exist and how they should be used.

### `references/REFERENCE_ASSET_MANIFEST.json`
Machine-readable index of all 35 canonical visual assets. It stores stable repository paths, raw GitHub URLs, GitHub page URLs, SHA values, roles and reference priorities so image-capable environments can attempt direct remote-reference loading without asking the user to re-upload assets.

### `references/full-body/`
Contains **25 presenter reference PNGs**. Use them for continuity of the recurring presenter: appearance, proportions, clothing fit, posture, viewing angles and pose possibilities.

They are **references, not pose templates**. New artwork should preserve continuity while creating fresh compositions.

### `references/sample-posts/`
Contains **10 ERC Academy Instagram sample PNGs**. These are the strongest concrete references for layout, colors, lighting, typography hierarchy, PROBALO treatment, CTA placement and overall ERC visual language.

When a written description is too abstract to settle a visual choice, inspect these examples.

---

## `content/aprender-con-ciencia/` — What to post and what has already been used

This is the **content-memory system** for the numbered Aprender con ciencia series.

### `SERIES_SPEC.md`
Defines what an Aprender con ciencia post is: one science-informed learning idea, concise explanation, practical exercise, CTA, source context and corresponding Spanish caption.

### `CONTENT_STRATEGY.md`
Defines **where new ideas come from and how to develop them**.

Sources can include learning science, second-language acquisition research, ERC Academy methodology, real learner problems, extensions of earlier themes and material supplied directly by the user.

It also defines the anti-repetition process and research standards.

### `CONTENT_IDEA_LOG.md`
The persistent **idea and source backlog/history**.

If the user supplies a URL, paper, article, book, quote, video, uploaded document or other source for a possible post, it should be recorded here—even when the post will be created later.

Ideas remain recorded as `INBOX`, `RESEARCHING`, `READY`, `USED`, `MERGED`, `REJECTED` or `HOLD`. Used/rejected ideas are retained so future chats can avoid repeating the same teaching point.

### `POST_LOG.md`
The canonical **official numbering and publication-history log**.

Read it before assigning a number. Never reuse a number merely because its publishing state is uncertain.

### `HISTORICAL_CONTEXT.md`
Recovered context from older ERC Academy conversations, including earlier topics, visual decisions, caption conventions and portability goals.

### `posts/`
Permanent detailed records for individual official posts.

For example, `posts/139.md` stores the recovered #139 topic, source context, artwork direction, CTA, caption and historical publication state.

As new official posts are produced, their detailed records should be added here.

---

## `publishing/` — How approved content reaches Instagram

### `publishing/ACCOUNT_AND_LINKS.md`
Reference for the target Instagram account and ERC Academy's other known social/web destinations.

### `publishing/INSTAGRAM_WORKFLOW.md`
The safe publishing procedure for **@erc.nic**: verify state, prepare/upload, publish only when authorized, protect against duplicates and record the result.

### `publishing/PUBLISHER_DIAGNOSTIC_2026-09-28.md`
Historical technical record of the temporary Cloudflare/DNS image-transfer failure encountered during the #139 publishing attempt. It exists so future chats do not misdiagnose that old infrastructure problem as an Instagram-account problem.

---

## `handoff/` — What changed most recently

### `handoff/CONVERSATION_HANDOFF_2026-09-29.md`
Records important migration/session decisions that may be newer than older historical documents: repository/public-reference decisions, test-vs-sequence behavior, current continuation state and portability goals.

Future handoffs can be added here when a conversation introduces significant system-level decisions that need to survive into another chat.

---

## How new content is created

A new post should not be invented only from a random motivational phrase.

The content engine is:

> **Candidate idea/source → log source → compare against prior ideas/posts → research/verify → identify one distinct teaching point → translate it into practical English-learning behavior → PROBALO → CTA → visual concept → Spanish caption → review → publish when authorized → update idea/post records.**

If the user supplies a link or other reference as the basis for a future post, preserve it in `CONTENT_IDEA_LOG.md` so it remains available across chats.

---

## Anti-repetition memory

The repository uses three levels of memory:

1. **`CONTENT_IDEA_LOG.md`** — remembers candidate ideas and supplied sources, including ideas never published.
2. **`POST_LOG.md`** — remembers official numbered posts and publishing status.
3. **`posts/[NUMBER].md`** — preserves the detailed record of each official post.

Before choosing a new topic, compare the candidate against prior **topic, central claim, learner problem, exercise, source, headline concept and visual metaphor**. A new title alone does not make a repeated idea new.

---

## Current continuation point

At the latest recorded handoff:

- Series reached **#139**.
- **#140** is the intended next official number unless `content/aprender-con-ciencia/POST_LOG.md` has since changed.
- Before image generation, confirm whether the user wants a **test generation** or the **next official sequential post**.
- A test does not consume a series number unless the user explicitly makes it official.

---

## Public repository / reference authorization

This repository is intentionally public. The user explicitly authorized the included ERC Academy visual-reference assets to be stored here.

Repository: `CarlosMElliot/ERC-Academy-Instagram-Content-System`
