# Lesson 1: Python Foundations — Variables, Data Types & Control Flow

Phase 1, Week 2. This is a complete lesson kit — everything you need is in this folder or linked below. You execute; the curation is done.

## 1. Watch (you likely already have this — treat as consolidation)

You're ~26% into **"Python 3 Programming: Beginner to Pro Masterclass"** (Ryan Ahmed) on your personal Udemy — that's almost certainly already covered the setup, variables/data types, operators, and control flow (if/elif/else, for/while loops) sections. This lesson treats that as **done**, not new material.

- If any of the cheat sheet below (Section 2) looks unfamiliar, go back and rewatch just that specific sub-topic in the course — don't rewatch the whole thing.
- Optional alternate explanation if something didn't land: Corey Schafer's free "Python Tutorial for Beginners" playlist on YouTube covers the same ground with different framing.
- **One thing to send me:** a screenshot of the course's actual "Course content" section list (like you did for the Udemy library search) — once I have the real section titles, future lesson "Watch" assignments can point to exact sections instead of topic descriptions.

## 2. Read

`cheat-sheet.pdf` in this folder — one page, covers data types, operators, control flow syntax, truthy/falsy rules, and the specific pitfalls that trip people up at this stage (mutability, `==` vs `is`, `/` vs `//`).

## 3. Reinforce (flashcards)

`flashcards.txt` — 25 cards, tab-separated (question `\t` answer). For right now, just self-quiz from the raw file (cover the answer column, go down the list) — no app needed yet. **This exact file becomes the input data for Lesson 2's project**, so don't throw it away.

## 4. Build

`project-brief.md` — the **Regulatory Deadline Tracker**, a small CLI script that classifies and reports on compliance deadlines. Uses only what's in this lesson (variables, data types, operators, control flow). It's also the first thread of the flagship RegCopilot project's world, at the smallest possible scale.

Build it in your `python-foundations-lab` repo, commit it, and report back.

---

**Coming in Lesson 2:** you'll build **LearnLoop v0.1** — your own CLI flashcard reviewer that reads `flashcards.txt` (yes, this exact file), quizzes you, and re-shows what you get wrong sooner. This replaces needing Anki or any other third-party flashcard app — it's the first version of the personal learning tool you asked me to design as a project instead of pointing you at existing software. It grows into a full AI-powered notebook app (RAG, embeddings, your own API key) by Phase 3.

**Done when:** the project runs correctly, you've self-quizzed from the flashcards at least once, and you can explain the "Common Pitfalls" section of the cheat sheet in your own words without looking at it. Report back (or say "too easy, give me more") and Lesson 2 gets built next.
