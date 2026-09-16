# Visual Review Package

Create the visual package only after the written ledger has passed reconciliation. The learner must receive both the verified written review and illustrated visual study materials.

## Required deliverables

Generate:

1. one or more illustrated `Topic Review` pages containing the full `Knowledge Summary` and complete Q&A sequence;
2. exactly one illustrated topic-decomposition mind map.

Every output image must be portrait 9:16. The first `Topic Review` page may place `Knowledge Summary` in the upper section and the opening Q&A items below it. Continue the remaining Q&A on additional pages. There is no fixed page count: split whenever phone-sized text, semantic illustrations, or generous spacing would otherwise be compromised. Never omit, paraphrase, compress, or shrink verified content merely to reduce the number of pages.

## Required reference assets

Use these user-approved examples as actual style-and-layout references for `Topic Review` pages:

- `../assets/reference-review-cup-page-1.png`
- `../assets/reference-review-cup-page-2.png`

Use this user-approved example as the primary mind-map reference:

- `../assets/reference-review-cup-mind-map.png`

The earlier bundled cards may be used as secondary mind-map references when useful:

- `../assets/reference-umbrella.png`
- `../assets/reference-computer.png`
- `../assets/reference-cup.jpg`
- `../assets/reference-backpack.png`

All input images are style and layout references only. Never copy their cup, umbrella, computer, backpack, Hello Kitty, labels, facts, colors, objects, or answers into a different lesson unless those items were genuinely practiced in the current session.

## Shared art direction

- Portrait 9:16 mobile study page with safe margins and generous breathing room.
- Warm off-white watercolor-paper background with subtle visible grain.
- Hand-drawn dark ink lettering and outlines with colored-pencil and light watercolor fills.
- Friendly adult-beginner workbook tone: lively and memorable, not childish or corporate.
- Large hand-lettered topic title, soft pink and blue marker highlights, numbered sections, and clear visual hierarchy.
- Small semantic illustrations beside the exact language they explain; illustrations are part of the teaching, not decoration.
- Topic-derived limited palette, high contrast, and comfortable phone-readable type.
- No photorealism, glossy 3D, plain spreadsheet-like cards, generic corporate UI, dense grids, long unbroken paragraphs, tiny type, unrelated decoration, watermarks, or signatures.

## Topic Review pages

### First page

Prefer this structure when it fits comfortably:

1. large title such as `<TOPIC> REVIEW · 1`;
2. `Knowledge Summary` in the upper section;
3. opening part of `Complete Q&A Review` in the lower section.

The `Knowledge Summary` must contain:

- exact topic;
- 12-20 useful practiced words or chunks;
- a concise Chinese meaning in parentheses beside every practiced teacher-introduced unfamiliar word, for example `ceramic（陶瓷的）` or `rinse（冲洗）`;
- 4-6 reusable practiced sentence patterns;
- `You did well`, `Next focus`, and retelling keywords when space permits without crowding.

Use a few clear, topic-specific illustrations to anchor meaning. Do not turn the page into a plain typographic list.

### Q&A continuation

Reproduce every reconciled `Question` with its one final `Correct answer`, in chronological order. Keep each pair together. Use alternating pink and blue hand-drawn accents, continuous numbering across pages, short separators, and a relevant mini-illustration for the question whenever it clarifies meaning.

Allow the final answer to contain teacher-taught knowledge only when the learner successfully practiced that answer under the same question. Do not show an incorrect attempt, hint trail, skipped question, or unpracticed fact.

The number of Q&A items per page is determined only by readability. Add another 9:16 page instead of shrinking the text, removing illustrations, or compressing vertical spacing.

## Topic-decomposition mind map

Generate exactly one 9:16 hand-drawn mind map after the review pages.

Build its manifest from the reconciled ledger:

- exact `SESSION_TOPIC` as the large title;
- 8-11 numbered branches chosen from practiced dimensions;
- concise English labels written verbatim;
- an object, action, person, place, part, material, or process illustration that directly explains each label;
- all protected values copied from `FACT_LOCKS`.

For a familiar object, prefer branches such as `What it is`, `Looks`, `Material & Parts`, `Kinds`, `Use`, `Keep & Clean`, `Buy`, `Made`, and `Why I like it` when those dimensions were practiced. Do not create an unpracticed branch merely to match the reference.

Place one large topic illustration on the left or lower-left, with thin curved muted-red branches leading to well-spaced numbered sections. Use process arrows for meaningful sequences such as cleaning, operating, buying routes, or making. Keep the mind map visually rich but readable; use short labels rather than full Q&A sentences.

## Prompt contract

Give every generated page its own exact text-and-illustration manifest. Include these invariants:

```text
Format: portrait 9:16 with generous whitespace and phone-readable text.
References: style and layout only; never reuse their topic content.
Text: render only the supplied title, headings, glossary pairs, questions, answers, and labels verbatim.
Illustrations: every image must directly explain adjacent practiced content; no decorative filler.
Facts: preserve all numbers, ranges, colors, names, places, preferences, ownership, and negatives.
Pagination: create additional pages instead of crowding, shrinking, paraphrasing, or omitting content.
```

## Inspection and repair

Inspect every image before presenting it:

- correct 9:16 orientation, title, page number, and section order;
- complete bilingual glossary with correct Chinese meanings;
- every required item present once and correctly spelled;
- Q&A order and pairing preserved with no pair split across pages;
- meaningful illustrations aligned with their adjacent language;
- protected facts unchanged;
- comfortable margins, readable type, clear grouping, and no crowding;
- no topic leakage from examples, references, or earlier lessons;
- exactly one mind map, regardless of the number of review pages.

If text or layout fails, make one targeted revision naming the defect and repeating the invariants. A second targeted revision is allowed. If a page remains crowded, split it. Do not replace the illustrated workbook style with a plain corporate text card merely to make rendering easier. Never claim that an image passed when its wording, facts, glossary, or semantic illustrations do not match the verified written review.

After displaying the complete package, give only one short instruction such as: `Next time, look at the pictures and talk about the topic without reading a script.`
