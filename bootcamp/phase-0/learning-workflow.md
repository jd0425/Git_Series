# Optional Deepening Tools: Obsidian + NotebookLM

**This is optional.** The primary delivery model is the per-topic Lesson Kit (see `docs/syllabus.md` Section 6 and `lessons/`) — each kit already ships its own flashcards (Anki) and cheat sheet PDF, so you don't need to build or maintain this workflow yourself. Use this only if you want to go deeper on your own beyond what a lesson kit provides — e.g. capturing your own notes on something a kit didn't cover in enough depth.

Two tools, two different jobs. Don't blend them — the split is what makes this work.

## Obsidian — raw capture (what you already have)
- PDF markup and annotation of course slides/materials.
- Verbatim notes, lecture excerpts, code snippets you want to keep.
- Your permanent, private, fully-owned vault — nothing here depends on a vendor staying in business.

## NotebookLM — active synthesis, not passive rereading (new)
Free (Google account, no trial clock, no cost). One notebook per phase/topic — e.g. "Phase 1 — Python Fundamentals," "RegCopilot Project," "AWS SAA Cert."

**Feed it real sources**, not vague prompts: exported Obsidian notes, the Ahmed course's slide PDFs if available, official docs, even this repo's `syllabus.md`. Everything it generates stays grounded in what you actually fed it — this is what makes it useful as a comprehension check instead of just another chat window.

**Use it to create, not just read:**
1. **Study guide / FAQ / briefing doc** after finishing a course section — forces synthesis instead of "I watched it, I know it."
2. **Grounded Q&A** when something's confusing — ask it directly against your sources; if it can't answer from what you gave it, that's a signal your notes have a gap, which is useful information on its own.
3. **Quiz / self-test questions** generated from the material — you answering questions is real retrieval practice; rereading isn't.
4. **Audio overview** — listen passively during downtime (the "on the go" reinforcement you wanted, ahead of any dedicated app). This is spaced repetition that doesn't require sitting at a desk again.

**Close the loop:** whenever NotebookLM produces something genuinely good (a clean summary, a sharp quiz), save it back into Obsidian. NotebookLM notebooks are a synthesis workspace, not your permanent knowledge base — Obsidian is.

## Per-session loop
1. Work through a chunk of the Ahmed course (or any material).
2. Drop your raw notes/markup into Obsidian as you go.
3. At a natural stopping point, feed that chunk's material into the matching NotebookLM notebook.
4. Generate a study guide + a handful of quiz questions. Answer them cold before checking.
5. Save the good output back into Obsidian.
6. Optional: generate the audio overview for a passive re-listen later that day/week.

This is also, incidentally, a working prototype of the kind of tool you eventually want to build and sell — treat what actually gets used here as signal for what's worth productizing later, rather than guessing upfront.
