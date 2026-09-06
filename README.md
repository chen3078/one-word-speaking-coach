# One Word Speaking Coach

One Word Speaking Coach is a skills-only ChatGPT and Codex plugin for adult English beginners. It turns one familiar word or everyday topic into a guided speaking lesson.

## Learning flow

1. Choose one word or topic.
2. Answer one A1-level question at a time.
3. Repeat concise corrections before moving on.
4. Learn useful missing vocabulary and real-world content.
5. Retell the topic from a keyword route.
6. Choose whether to transfer the same patterns to a related word.
7. Review the lesson with an English-only visual decomposition card when image generation is available.

The coach defaults to English and uses brief Chinese only for genuinely new content or after repeated misunderstanding.

## Plugin structure

```text
one-word-speaking-coach/
├── .codex-plugin/
│   └── plugin.json
└── skills/
    └── one-word-speaking-coach/
        ├── SKILL.md
        ├── agents/
        ├── assets/
        └── references/
```

This plugin contains no MCP server, external connector, tracking code, or account authentication.

## Start a lesson

After installing the plugin, start a new ChatGPT conversation, select the skill with `@one-word-speaking-coach`, and say:

```text
My topic is coffee. Start at A1 and ask me one question at a time.
```

Start voice chat in the same conversation to practice speaking aloud.

## Reference implementation

The included coffee review card is the approved visual benchmark for future end-of-lesson cards. It is a style and layout reference; each lesson must generate labels from content the learner actually practiced.
