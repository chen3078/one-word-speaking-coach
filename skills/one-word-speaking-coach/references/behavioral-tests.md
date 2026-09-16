# Behavioral Regression Tests

Use these scenarios only to audit a new or modified version of the skill. They are not lesson scripts and their nouns must never leak into a real learner session.

## 1. Fragment requires a full model and retry gate

Prompt: topic `key`; coach asks quantity; learner says `two`.

Required behavior: give a complete natural sentence such as `I usually carry two keys.` and request repetition. Do not ask the next question in the same turn. After a successful retry, ask exactly one next question.

## 2. Correction cannot skip ahead

Learner asks how to say `公交站` during a bus lesson.

Required behavior: teach a complete sentence containing `bus stop`, request repetition, and keep the item pending. Do not move to payment or another bus question until the retry passes.

## 3. Teacher expands beyond volunteered content

Learner gives only one personal kind, use, or purchase place.

Required behavior: preserve that fact, then later teach useful alternatives and at least one missing process, part, care, problem, or access dimension. Require practice of the new language. Do not let the entire lesson become follow-up questions about only the volunteered fact.

## 4. Realtime ambiguity and duplication

Transcript plausibly confuses `red` with `right`, or repeats the same utterance twice.

Required behavior: ask for clarification rather than assuming a fact. Process duplicated transcript content once and do not advance twice.

## 5. Meta-interruption preserves pending state

While a retry is pending, learner asks in Chinese whether the skill is being followed.

Required behavior: answer the meta-question briefly, acknowledge any real process violation, and resume the same pending retry. Do not create a learning entry or ask a different question.

## 6. Exact complete recap

A supermarket lesson contains the practiced sentence `People use a basket to carry their shopping.` and the exact time `between seven and nine in the evening`.

Required behavior: the recap includes the basket question and answer exactly once and preserves seven-to-nine. It must not omit the basket item or change the time to six-to-nine.

## 7. Topic and image lock

A `key` lesson uses umbrella, computer, cup, and backpack cards as visual references.

Required behavior: the generated mind map uses their art direction and layout only. It contains no umbrella, coffee, cup, backpack, or computer content unless the key lesson itself practiced one of those items.

## 8. Early summary

Learner requests a direct summary before retelling.

Required behavior: stop asking questions, reconcile all completed items, label the review partial when appropriate, preserve every verified fact, and do not invent unpracticed coverage to make the result look complete.

## 9. Pending teacher expansion outranks an older question

Sequence:

1. Coach asks `What are your boots made of?`
2. Learner practices and successfully repeats `My boots are made of leather.`
3. Coach teaches `Boots have soles, and some boots have laces.` and requests repetition.
4. Learner repeats `Boots have soles, and some boots have laces.`

Required behavior: mark the teacher-led parts item accepted and keep the material question in `COMPLETED_IDS`. Do not ask about leather again, do not say the learner answered the wrong dimension, and do not consume the repetition twice.

## 10. Evidence-based state recovery

Learner reports that a question was already completed and supplies a screenshot or quoted sequence.

Required behavior: compare the evidence with the recent dialogue, repair pending and completed IDs, state the corrected sequence clearly, and pause or continue from the first genuinely unfinished item. Never defend an inconsistent internal state or make the learner repeat an already accepted sentence solely to repair the coach's mistake.

## 11. Voice startup requires a selected topic

Sequence: the learner explicitly invokes the skill, then says `Talk about a topic`. The coach suggests a topic, and the learner says it has already been practiced or asks for a different real object.

Required behavior: remain in `SETUP`; ask for the learner's chosen word or offer one concrete candidate and wait for acceptance. Do not treat a suggestion as accepted, ask a learning question about it, or keep switching between unaccepted topics. Once a topic is selected, lock it until the learner explicitly changes it.

## 12. A meaning request does not advance the lesson

Sequence: during a selected-topic voice lesson, the learner asks what an unfamiliar word in the current question means, then asks for Chinese.

Required behavior: give a short Chinese meaning on the first request and repeat the same pending English question. Do not give a long English definition, open a different topic, or advance as though the learner had answered.

## 13. Professional teacher-led expansion

The learner gives correct but narrow personal answers about one familiar object.

Required behavior: select 3-6 accurate, high-utility additions that fill genuine coverage gaps and give the learner useful beginner language. Proactively gloss likely unfamiliar teacher-introduced terms in Chinese, teach one short micro-unit at a time, require the complete model sentence, and record only successful retries. Do not lecture, dump vocabulary, introduce uncertain trivia, or add unpracticed facts directly to the review.

## 14. Written and visual review package

A completed lesson has 12 summary items, 5 sentence patterns, and 10 reconciled Q&A pairs whose exact text will not fit comfortably on one phone card.

Required behavior: provide the complete written `Knowledge Summary` and written `Complete Q&A Review`, then generate illustrated 9:16 `Topic Review` pages and exactly one 9:16 topic-decomposition mind map. The first image may place `Knowledge Summary` above the opening Q&A items. Continue onto as many pages as readability requires; preserve every item and pair exactly, keep pairs intact, and use comfortable phone-sized text with generous whitespace. Never crowd content, impose a fixed page count, or replace the written review with images.

## 15. Proactive Chinese gloss for a new word

During a beginner cup lesson, the coach wants to introduce `ceramic` before the learner has used or asked about the word.

Required behavior: first give a concise gloss such as `ceramic（陶瓷的）`, then give one natural English model sentence and require repetition. Record the glossary pair and include it in the bilingual `Knowledge Summary`. Do not wait for the learner to ask `什么意思？`.

## 16. Grammatical but indirect answer needs a natural recast

Coach asks `How do you clean your cup?` Learner says `I use water and soap.`

Required behavior: do not accept and advance merely because the sentence is grammatical. Say that a more direct natural answer is `I clean my cup with water and soap.`, require a retry, and keep the same question pending. Preserve the learner's facts and do not invent a brush or another cleaning step.

## 17. Systematic concrete-object coverage

A learner supplies short personal facts about a familiar manufactured object.

Required behavior: follow a coherent object-question spine covering identity, looks, material, parts, kinds, use, frequency or occasion, keeping or location, care or operation, access, making or mechanism, and preference when natural. General knowledge gaps are taught and practiced inside the relevant question. Do not produce a lesson made mostly of reactive follow-ups or add those dimensions for the first time in the final image.
