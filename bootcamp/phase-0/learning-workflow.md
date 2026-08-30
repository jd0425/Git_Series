# Reference Points: Obsidian, Anki, Open Notebook

**Superseded by LearnLoop (see `docs/syllabus.md` Section 5, Companion Project box) as of the "build my own tool, don't install someone else's" correction.** You are not being asked to install and maintain Anki or Open Notebook — you're building your own equivalent, called LearnLoop, as a project that grows with your skill level. This doc stays only as a description of what similar tools look like elsewhere, useful for inspiration/comparison while designing LearnLoop's features, or if you ever want a stopgap before a given LearnLoop version exists.

Obsidian is the one piece still genuinely optional and worth keeping independent of LearnLoop — raw note capture/PDF markup is a different job than an app you're actively building, and there's no reason to make LearnLoop reimplement Obsidian's job.

Two tools, two different jobs, if you use both. Don't blend them.

## Obsidian — raw capture
- PDF markup and annotation of course slides/materials.
- Verbatim notes, lecture excerpts, code snippets you want to keep.
- Your permanent, private, fully-owned vault — nothing here depends on a vendor staying in business.

## Feature inspiration for LearnLoop (not a setup guide)

**[Open Notebook](https://github.com/lfnovo/open-notebook)** (MIT license, self-hosted via Docker, BYO Anthropic/OpenAI API key or fully local via Ollama) is what LearnLoop v2.0 is aiming to functionally match, in your own codebase. Worth knowing what it does so LearnLoop's design has a real target, not because you're expected to run it yourself:

- Ingests sources (PDFs, notes, web pages) and answers questions grounded strictly in them.
- Generates study guides / FAQs / briefing docs on demand — synthesis, not passive rereading.
- Generates multi-speaker podcast/audio overviews for passive listening.
- No vendor usage caps, since it's your own API key — the same design principle LearnLoop v2.0 should follow.

**Anki** (free spaced-repetition app) is the same kind of reference for LearnLoop v0.1/v0.2's flashcard-and-scheduling feature — an existing implementation of "show me the card I'm about to forget," worth understanding before building your own version of it.

**Cost discipline, once LearnLoop v2.0 exists and calls a real LLM API:** set a monthly spend cap/billing alert on the Anthropic (or OpenAI) console, same discipline as the AWS billing alarm — usage at personal scale is typically cents to a few dollars/month, but cap it anyway.

This is, not incidentally, the actual thing you said you want to build and sell eventually — LearnLoop *is* that product's first prototype, developed as you go rather than planned upfront and never started.
