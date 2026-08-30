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

`flashcards.txt` — 25 cards, tab-separated (question `\t` answer), ready to import into **Anki** (free, no daily limits, works offline — better fit for daily spaced repetition than querying an AI tool each time):

1. Install Anki (anki.web / App Store / Play Store — free).
2. Create a deck, e.g. "Python Foundations."
3. File → Import → select `flashcards.txt` → map the two columns to Front/Back.
4. Review a few minutes a day going forward; Anki schedules the repetition for you.

## 4. Listen (optional, lightweight)

If you want an audio recap: drop **just `cheat-sheet.pdf`** into your self-hosted Open Notebook instance and generate a podcast/audio overview. Since it runs on your own API key, there's no vendor daily cap to worry about — use it as much or as little as you want. Skip this entirely if you don't want it; it's not required. See `phase-0/learning-workflow.md` for setup.

## 5. Build

`project-brief.md` — the **Regulatory Deadline Tracker**, a small CLI script that classifies and reports on compliance deadlines. Uses only what's in this lesson (variables, data types, operators, control flow). It's also the first thread of the flagship RegCopilot project's world, at the smallest possible scale.

Build it in your `python-foundations-lab` repo, commit it, and report back.

---

**Done when:** the project runs correctly, you've been through the flashcards at least once, and you can explain the "Common Pitfalls" section of the cheat sheet in your own words without looking at it. Report back (or say "too easy, give me more") and Lesson 2 gets built next.
