# Visual Review Card

Create a visual topic decomposition card after the main lesson when the environment supports image or visual-artifact generation. The card is a retrieval aid: it should help the learner reconstruct the lesson without reading a paragraph.

## Content rules

- Use English only inside the visual. Do not include Chinese translations.
- Include only facts, words, and processes actually practiced during the session.
- Put the target word and a clear illustration at the center or left-center, with the learning branches arranged clearly around or beside it.
- Use 6–9 surrounding branches selected from the lesson's natural coverage dimensions.
- Keep labels short, usually 1–5 words.
- Prefer concrete nouns, adjectives, short verb phrases, and arrow sequences.
- Use exact spelling and natural English.
- Do not include full model paragraphs, grammar explanations, scores, brand names that were not needed, or decorative filler.
- Every illustration and icon must directly depict the target topic, a practiced part or item, a practiced action, or a practiced place. Do not use unrelated visual metaphors, mascots, characters, animals, or decorative objects to represent an idea such as size or convenience.

Typical branches:

- `What it is`
- `Looks`
- `Parts / Ingredients`
- `Taste / Feel`
- `Kinds / States`
- `When`
- `Where`
- `How to use / eat / drink`
- `From / Grows / Made`

Rename or omit branches to fit the topic naturally.

## Visual design

- Use a clean educational mind-map or labeled-object style.
- Make it portrait or square and easy to read on a phone.
- Prefer a hand-drawn watercolor-and-colored-pencil look with soft paper texture, matching the approved benchmark.
- For a portrait card, use curved hand-drawn branches leading to stacked, numbered learning sections when that fits the topic.
- Use high contrast, generous spacing, and one clear visual hierarchy.
- Connect each label visibly to the central subject or relevant illustrated part.
- Use a limited friendly color palette and simple illustrations.
- Avoid tiny text, crowded backgrounds, watermarks, logos, unnecessary decoration, and Chinese characters.

## Approved visual benchmark

Use [`../assets/coffee-review-card-example.png`](../assets/coffee-review-card-example.png) as the user-approved benchmark for future review cards. Match its hand-drawn watercolor-and-colored-pencil feel, portrait branching layout, short English labels, friendly educational tone, and moderate information density.

Treat the benchmark as a style and composition reference only. Do not copy its coffee content into another topic. Build every branch, illustration, and label from the current lesson's practiced material.

## Generation strategy

Before generation, build a content manifest containing:

- the exact center word;
- 6–9 exact branch headings;
- every permitted English label, written verbatim;
- the permitted objects, actions, and places for each branch.

If a raster image-generation tool is available, classify this as a `scientific-educational` or `infographic-diagram` image. Include the approved benchmark as a style and layout reference when the tool supports reference images. Supply the complete content manifest in the prompt.

Inspect the result against the manifest. Reject it and make one targeted correction pass when any of these conditions occurs:

- required text is missing, misspelled, duplicated, or attached to the wrong object;
- an unpracticed fact, unrelated object, mascot, character, animal, logo, brand, or Chinese text appears;
- a required branch is missing or two branches are accidentally merged;
- labels are too small, crowded, or low-contrast for phone review;
- the central topic or a practiced part, action, or place is illustrated inaccurately.

Do not accept a card merely because its overall style matches the benchmark. Content accuracy and direct visual relevance are required.

If the targeted correction still cannot produce reliable exact text, use a code-native SVG, HTML, canvas, slides, or diagram layout that preserves every label exactly. If no visual tool is available, output a compact English-only text mind map and state that it is the fallback, not an image.

## Example content specification: coffee

Center:

`COFFEE`

Possible practiced branches:

- `dark drink`
- `coffee beans`
- `bitter`
- `hot or iced`
- `morning or afternoon`
- `home / café / store`
- `milk or sugar`
- `roast → grind → brew`

Use only the branches actually taught. Do not add this entire example automatically.

## Review instruction

After displaying the card, say only one short instruction such as:

`Next time, look at this picture and talk about the topic without reading a script.`
