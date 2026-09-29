# Aprender con ciencia — Content Strategy

This file defines **where new ERC Academy post ideas come from, how ideas are developed, and how the system prevents topic repetition over time**.

It complements `FRESH_CHAT_WORKFLOW.md`:
- `FRESH_CHAT_WORKFLOW.md` = how a fresh chat operates.
- This file = how a new content idea is selected, researched, transformed and recorded.
- `POST_LOG.md` = canonical history of numbered posts and publication state.

## Content foundations

New posts may be developed from:

1. **Learning science** — memory, retrieval practice, spacing, attention, cognitive load, feedback, deliberate practice, sleep/rest and related evidence.
2. **Second-language acquisition and language-learning research** — listening, pronunciation, vocabulary, comprehensible input, speaking practice, interaction, fluency, corrective feedback and related areas.
3. **ERC Academy methodology and teaching practice** — practical exercises and teaching principles that fit the academy's established methodology. Clearly distinguish an ERC adaptation from a direct research finding.
4. **Real English-learner problems** — difficulty understanding native speech, translating mentally, fear of speaking, pronunciation problems, forgetting vocabulary, inconsistent study, weak retrieval, limited listening exposure, etc.
5. **Previously approved content themes** — extend a useful theme with a genuinely different learning point rather than repeating the same claim.
6. **User-supplied source material** — a research paper, article, book excerpt, quote, video, webpage, social post, uploaded file, URL or other reference supplied by the user can become the starting point for a new post.

## Topic families

Rotate across themes rather than repeatedly choosing the same category:

- Listening and auditory discrimination
- Pronunciation and articulation
- Retrieval and active recall
- Memory and forgetting
- Vocabulary and contextual learning
- Speaking and fluency
- Confidence, beliefs and learner behavior
- Attention and distraction
- Spaced/repeated practice
- Feedback and error correction
- Deliberate practice
- Study planning and habit design
- CEFR/communicative abilities
- Multimodal learning and gestures
- Sleep, rest and consolidation
- Conversation/interaction
- Comprehension strategies
- Learning autonomy/metacognition

This list can grow. Add new families when the series expands.

## New-post development pipeline

Before proposing an official numbered post:

1. Read `POST_LOG.md`.
2. Read `CONTENT_IDEA_LOG.md`.
3. Search the individual records under `posts/` when relevant.
4. Identify candidate topic/source.
5. Compare the candidate against previous topics, claims, exercises and headlines.
6. If substantially repetitive, reject it or deliberately choose a different scientific angle.
7. Verify the source/evidence when the post makes a research-based claim.
8. Reduce the idea to **one clear learning point**.
9. Translate that point into a practical English-learning behavior.
10. Create a simple `PROBALO` activity.
11. Create a learner-facing CTA.
12. Develop a fresh visual metaphor/composition.
13. Prepare the Spanish caption with appropriate source context.
14. Record the idea/source in the content logs.
15. When it becomes an official numbered post, update `POST_LOG.md` and its individual post record.

## Anti-repetition rule

Avoid repeating not only exact titles but also the same **core teaching claim**.

For every candidate, compare:
- topic family;
- central claim;
- learner problem;
- practical exercise;
- source/research basis;
- headline concept;
- visual metaphor.

Two posts may belong to the same broad category if they teach meaningfully different things.

Example: several listening posts are acceptable if one addresses multi-talker variability, another auditory discrimination, another reduced speech and another focused listening. Repeating the same “listen more to improve listening” message with different wording is not sufficient novelty.

## User-supplied links and references

When the user provides a URL, paper, article, book, quote, video, uploaded document or other source and asks to build a post from it:

1. Read/research the supplied source as permitted by available tools.
2. Record it in `CONTENT_IDEA_LOG.md` even if the idea remains a draft.
3. Preserve the original URL or a stable source identifier when available.
4. Record the date supplied, proposed topic, source type and status.
5. Note whether the source was used, rejected, merged with another idea or remains queued.
6. If it becomes an official post, connect the source entry to the post number and individual post record.
7. Do not silently lose a supplied source merely because the post is created in a later chat.

If a supplied source cannot be verified/read, record that limitation rather than inventing its contents.

## Research discipline

Research is used to support a teaching point, not to decorate a motivational claim.

- Do not overstate causality or certainty.
- Distinguish research findings from ERC Academy's practical adaptation.
- Prefer credible primary/academic sources when feasible.
- Keep the poster concise; put nuance and source context in the caption/post record.
- Do not reproduce long copyrighted passages from a source.
- A book/quote can inspire a topic, but the resulting educational claim should be framed accurately.

## Idea status lifecycle

Use these statuses in `CONTENT_IDEA_LOG.md`:

- `INBOX` — source/idea captured but not evaluated.
- `RESEARCHING` — being checked/developed.
- `READY` — sufficiently distinct and supported for production.
- `USED` — converted into an official post.
- `MERGED` — incorporated into another idea/post.
- `REJECTED` — not suitable, repetitive or insufficiently supported.
- `HOLD` — intentionally saved for later.

Never delete an idea simply because it was rejected or used. Keeping the history is what prevents accidental repetition.

## Relationship between logs

### `CONTENT_IDEA_LOG.md`
Tracks the **idea pipeline and supplied sources**, including ideas that never become posts.

### `POST_LOG.md`
Tracks **official numbered series history and publishing state**.

### `posts/[NUMBER].md`
Stores the detailed permanent record for an individual official post.

Together these form the series memory.
