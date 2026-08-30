# Optional Deepening Tool: Obsidian + Open Notebook (self-hosted)

**This is optional.** The primary delivery model is the per-topic Lesson Kit (see `docs/syllabus.md` Section 6 and `lessons/`) — each kit already ships its own flashcards (Anki) and cheat sheet PDF, so you don't need to build or maintain this workflow yourself. Use this only if you want to go deeper on your own beyond what a lesson kit provides — e.g. capturing your own notes on something a kit didn't cover in enough depth.

Two tools, two different jobs. Don't blend them — the split is what makes this work.

## Obsidian — raw capture
- PDF markup and annotation of course slides/materials.
- Verbatim notes, lecture excerpts, code snippets you want to keep.
- Your permanent, private, fully-owned vault — nothing here depends on a vendor staying in business.

## Open Notebook — active synthesis, self-hosted, no restrictions
**Switched from Google NotebookLM to [Open Notebook](https://github.com/lfnovo/open-notebook)** (MIT license, self-hosted via Docker) — no daily usage caps, no vendor lock-in, bring your own Anthropic/OpenAI API key or run fully local via Ollama. See the setup steps in the chat history / repo commit that introduced this, or the project's own README, for the Docker Compose quickstart.

**Bonus:** standing this up is itself real hands-on Docker + LLM-API practice — an informal preview of Phase 2 material, pulled forward because it's motivated by something you actually want to use, not just an assignment.

One notebook per phase/topic — e.g. "Phase 1 — Python Fundamentals," "RegCopilot Project," "AWS SAA Cert."

**Feed it real sources**, not vague prompts: exported Obsidian notes, lesson kit PDFs, official docs, even this repo's `syllabus.md`. Everything it generates stays grounded in what you actually fed it — this is what makes it useful as a comprehension check instead of just another chat window.

**Use it to create, not just read:**
1. **Study guide / FAQ / briefing doc** after finishing a course section — forces synthesis instead of "I watched it, I know it."
2. **Grounded Q&A** when something's confusing — ask it directly against your sources; if it can't answer from what you gave it, that's a signal your notes have a gap, which is useful information on its own.
3. **Multi-speaker podcast / audio overview** — listen passively during downtime (the "on the go" reinforcement you wanted, ahead of any dedicated app).

**Close the loop:** whenever Open Notebook produces something genuinely good (a clean summary, a sharp quiz), save it back into Obsidian. Open Notebook is a synthesis workspace, not your permanent knowledge base — Obsidian is.

**Cost discipline:** it's BYO-API-key, so usage is metered by whichever provider you connect (typically cents to a few dollars/month for personal use at this scale) — set a monthly spend cap/billing alert on the Anthropic (or OpenAI) console, same discipline as the AWS billing alarm.

## Per-session loop
1. Work through a chunk of material (a lesson kit, the Ahmed course, etc.).
2. Drop your raw notes/markup into Obsidian as you go.
3. At a natural stopping point, feed that chunk's material into the matching Open Notebook notebook.
4. Generate a study guide + a handful of quiz questions. Answer them cold before checking.
5. Save the good output back into Obsidian.
6. Optional: generate a podcast/audio overview for a passive re-listen later that day/week.

This is also, incidentally, a working prototype of the kind of tool you eventually want to build and sell — treat what actually gets used here as signal for what's worth productizing later, rather than guessing upfront. It's also a live example of exactly the kind of self-hosted, provider-agnostic AI application architecture the RegCopilot flagship project will formalize later.
