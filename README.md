# One Word Speaking Coach

One Word Speaking Coach is a skills-only ChatGPT and Codex plugin for adult English beginners. It turns one familiar word or everyday topic into a guided speaking lesson.

## Learning flow

1. Choose one word or topic.
2. Answer one A1-level question at a time.
3. Repeat concise corrections before moving on.
4. Learn useful missing vocabulary and real-world content.
5. Retell the topic from a keyword route.
6. Choose whether to transfer the same patterns to a related word.
7. Review every question with only its final correct, natural answer.
8. Review the lesson with an English-only visual decomposition card when image generation is available.

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

The latest packaged release in this repository is `one-word-speaking-coach-plugin-1.0.4.zip`.

## Platform scope

This repository is a local Codex plugin package for desktop and CLI testing. Making the GitHub repository public does not automatically publish the plugin to the ChatGPT plugin directory or make it available across a ChatGPT account.

ChatGPT mobile can use plugins that are available to the user's account on supported Chat and Work surfaces. Account-wide distribution requires the applicable ChatGPT plugin publishing or submission process. Codex voice runs in the ChatGPT desktop app; paired iOS remote access is separate from standalone mobile use.

## Start a lesson locally

After installing the plugin in Codex, start a new conversation, select the skill with `@one-word-speaking-coach`, and say:

```text
My topic is coffee. Start at A1 and ask me one question at a time.
```

In the ChatGPT desktop app, start Codex voice in the same conversation to practice speaking aloud.

Official platform references: [ChatGPT plugins](https://learn.chatgpt.com/zh-Hans/docs/plugins) and [Codex voice](https://learn.chatgpt.com/pt-BR/docs/features/voice).

## Reference implementation

The included coffee review card is the approved visual benchmark for future end-of-lesson cards. It is a style and layout reference; each lesson must generate labels from content the learner actually practiced.
