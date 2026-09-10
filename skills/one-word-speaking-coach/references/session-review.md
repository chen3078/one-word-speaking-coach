# Session Review

At the end of a completed lesson, turn the silent session ledger into a clean study record. The learner should be able to review every practiced exchange without scrolling through the original conversation.

## Structured session ledger

Lock the exact main topic before the first learning question:

`SESSION_TOPIC: <learner's topic>`

Maintain stable internal entries throughout the lesson:

- `Q01 | dimension | exact main question | final answer | accepted`
- `Q02 | dimension | exact main question | final answer | accepted`
- `P01 | dimension | coach-led practice | final practiced sentence | accepted`

Create a `Q` entry when a new main learning question is asked. Create a `P` entry only for meaningful content taught without a main question. Corrections, hints, translations, acknowledgments, and `Try it again` do not create new entries. When the learner retries, replace that entry's answer with the last substantially correct version rather than adding another item.

Choose the final answer in this order:

1. the learner's last substantially correct retry for that item;
2. the coach's final natural model when it was taught but a repeat is unavailable;
3. the learner's original answer when it was already correct.

Do not silently rewrite an accepted answer into a materially different fact during final review.

## Required two-pass reconciliation

Before composing the review package, reconcile the ledger against the conversation from the locked topic through the transfer decision:

1. **Extraction pass:** identify every main learning question and every meaningful coach-led practice item in chronological order. Rebuild a missing ledger entry from the visible conversation when necessary.
2. **Validation pass:** verify that every extracted main question maps to exactly one `Q` entry, every important taught item maps to at most one `P` entry, IDs are unique and ordered, and every answer follows the final-answer precedence above.

Then enforce these invariants:

- the number of recap `Question` items equals the number of reconciled `Q` entries;
- every `Q` entry appears once and only once;
- each `Question` is paired with the answer practiced for that same question;
- all main-topic entries refer to `SESSION_TOPIC` or content explicitly practiced for it;
- nouns from examples, prior sessions, visual benchmarks, or an unstarted transfer topic never appear unless the learner actually practiced them;
- the retelling and visual manifest are derived from this reconciled ledger, not reconstructed independently from memory.

If the earlier conversation is unavailable and the ledger cannot be reconciled, do not invent missing questions or answers. State briefly that the available recap may be incomplete and provide only the entries that can be verified.

## Required output order

Produce the final review package in this exact order so no required learning feedback is omitted:

1. `Knowledge Summary`
2. `Complete Q&A Review`
3. `Retelling`
4. `Visual Review Card`
5. one short review instruction

### 1. Knowledge Summary

Include all of the following:

- `Topic`: the lesson word or topic;
- `Core vocabulary`: the most useful words actually practiced;
- `Sentence patterns`: 3–5 reusable patterns from the lesson;
- `You did well`: one specific, evidence-based strength from this session;
- `Next focus`: one highest-value, actionable improvement based on this session;
- `Retelling keywords`: the exact keyword route for later recall.

Do not use generic praise. The strength and next focus must describe observable learner performance. Do not introduce new vocabulary, facts, or grammar in `Next focus`.

### 2. Complete Q&A Review

List the main learning questions in chronological order. For each item, include:

- `Question`: the coach's main English question;
- `Correct answer`: the final accepted, corrected, or expanded natural English answer.

Do not include the learner's incorrect or incomplete attempts, requests for translation, coaching hints, or retry history. The recap is a clean answer key, not a raw transcript.

## Coach-led expansions

Some important learning items begin with teaching rather than a question. Include each one in the same chronological position as:

- `Practice`: a short description or the coach's taught sentence;
- `Correct answer`: the final sentence the learner practiced.

Examples include new parts, materials, common purchase locations, a production sequence, or a reusable sentence pattern. Include only meaningful content practice, not acknowledgments such as `Good` or procedural prompts such as `Try it again`.

### 3. Retelling

After the question-and-answer items, include:

- `Correct retelling`: a concise connected retelling built only from final accepted answers and important taught content.

Keep the correct retelling at the learner's demonstrated level. It is a review script assembled from language already practiced, not a place to add new facts or grammar.

### 4. Visual Review Card

Create the card from the same accepted-answer ledger used for the written review. Follow [visual-review-card.md](visual-review-card.md). The card may compress sentences into short labels, but it must not add facts, objects, brands, or metaphors that were not practiced.

### 5. Review instruction

End with one short instruction telling the learner how to use the card or retelling keywords next time. Do not add another topic invitation after the learner has declined transfer.

## Final completeness check

Before sending the package, confirm silently that:

- every main learning question appears once and in chronological order;
- each item contains only the final correct answer;
- meaningful coach-led teaching appears as `Practice` where needed;
- `You did well` and `Next focus` are both present and session-specific;
- the keyword route and correct retelling use only practiced language;
- personal facts are preserved unless sensitive;
- no learner errors, translation requests, hints, retries, or procedural messages remain;
- no new invitation appears after transfer was declined.
- the recap `Question` count exactly matches the reconciled `Q` count;
- every answer belongs to the question beside it and uses the final accepted version;
- the main topic is unchanged and no example-topic noun has leaked into the review;
- the retelling and visual-card manifest use the same reconciled entries.

## Language and formatting

- Keep lesson questions and answers in English.
- Use brief Chinese only for vocabulary meanings or repair notes that were actually taught during the session.
- Make the recap easy to scan with numbered items and short labels.
- Preserve personal facts supplied by the learner, but omit sensitive details that are not necessary for language review.
- Include the optional transfer practice only when it occurred.
- Do not end the recap with another invitation or question after the learner has declined transfer.
