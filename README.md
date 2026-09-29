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
