# Bootcamp Syllabus (v1 — Locked)
## Track: Software Engineering → AI Solutions Architect / Forward Deployed Engineer

**Status: v1 locked, Phase 0 underway.** Still a living document — amend Section 10 anytime scope, pacing, or sequencing needs to change. See `learner-profile.md` for the background this plan is built against.

---

## 1. Target Outcome

- **Primary target roles:** Solutions Architect, Forward Deployed Engineer, Customer/Field Engineer — roles that implement AI solutions directly with enterprise clients — at major cloud/tech companies (AWS, Google Cloud, Databricks, Meta, Palantir-style orgs).
- **Explicitly not targeting:** Core FAANG Software Engineer IC roles. Ruled out for this timeline — see learner profile for why.
- **Level ambition:** Mid-to-upper level, leveraging 10+ years of professional seniority. I will flag in real time when entry/associate-level competency is reached so we can decide whether to start applying early, and the resume gets rebuilt at each checkpoint (entry → mid → upper), not just once at the end.
- **Certification path:** AWS Certified Solutions Architect – Associate first (matches the target title directly, broadly recognized) → AWS Certified AI Practitioner and/or AWS Certified Machine Learning Engineer – Associate → stretch goal: AWS Certified Machine Learning – Specialty.
- **Flagship project — "RegCopilot":** An AI compliance/governance assistant — RAG over policy and regulatory documents, automated risk flagging, audit-ready summarization — built incrementally from a script to a deployed cloud system across the whole program. Directly reuses the OCC/MRA/FDA regulatory background as the project's premise, which is also the interview story.

---

## 2. What We're Not Re-Teaching (your existing strength)

- **SQL** across Snowflake/Postgres/SQL Server, data modeling, star schema, warehousing.
- **BI/data storytelling** (Power BI, Tableau, Qlik) — reused for project demos and stakeholder communication practice, not retaught from scratch.
- **Git/GitHub basics** — confirmed via your practice repo. We build on it (branch workflows, PRs, project structure, commit discipline) rather than starting at "what is a commit."
- **Stakeholder management, executive communication, regulatory domain knowledge** — this is arguably your biggest edge for FDE-style roles and gets deliberately exercised throughout, not treated as a soft-skill afterthought.

## 3. What We're Building From Near-Zero

- Hands-on Python (real, multi-file projects — not scripts)
- CS fundamentals reactivation (data structures/algorithms at a Solutions-Architect-appropriate depth — not a full LeetCode grind)
- Cloud infrastructure (AWS primary)
- AI/LLM engineering: embeddings, vector databases, RAG, evals, agentic/tool-use patterns
- Software engineering practice: testing, packaging, CI/CD basics, code review habits
- Technical interviewing calibrated to this specific track (not generic SWE interview prep)

---

## 4. Time Commitment

- **Cadence:** 5 days/week, 6–8 hrs/day (~30–40 hrs/week)
- **Total duration:** ~18–20 weeks (~4.5–5 months) to mid-level interview-ready, with an entry/associate-level checkpoint around **week 8–10**.
- This is a plan, not a contract. We adjust weekly based on actual pace — tell me immediately if something is too easy (I'll escalate difficulty) or too slow (we'll cut scope, not quality).

---

## 5. Phase-by-Phase Breakdown

### Phase 0 — Diagnostic & Setup (Week 1)
- Environment setup (Python, VS Code, virtual envs, terminal fluency check) on the MacBook Pro; confirm Dell VDI role/limits.
- Python diagnostic exercise (calibrate real starting point regardless of self-report).
- Light math/stats diagnostic (probability, basic linear algebra intuition) — identifies gaps, not a full course.
- Obsidian vault set up for raw note-taking/PDF markup; NotebookLM (free, Google) set up as the active-synthesis layer on top of it — see `phase-0/learning-workflow.md`.
- **AWS account creation deliberately deferred to the start of Phase 2** (see trial-period rule, Section 7) — the free tier's 12-month clock starts at account creation, so creating it now would burn runway during Phases 0–1 when it isn't needed yet. Free AWS *learning content* (AWS Skill Builder, which only needs a no-cost AWS Builder ID, not a billed account) can be started anytime without triggering that clock.

### Phase 1 — Python & CS Reactivation (Weeks 2–5)
- Python fundamentals through building, not syntax drills: functions, OOP, file I/O, error handling, virtual environments, packaging.
- Testing discipline from day one (pytest) — every exercise ships with a test, not bolted on later.
- Data structures & algorithms refresh: arrays/hash maps/trees/graphs at a working-fluency level, enough for technical screens at this track's bar — not competitive-programming depth.
- Bridge exercise: rebuild a SQL/pandas workflow you already know how to do in Excel/SQL, in Python — reactivates existing data intuition instead of starting cold.
- Milestone: a small multi-file CLI tool, tested, in its own git repo with a real README.

### Phase 2 — Cloud & Data Engineering Foundations (Weeks 6–9)
- **Create the actual AWS free-tier account here** (not in Phase 0) — starts the 12-month free-tier clock right when it'll get used, per the trial-period rule. Set billing alarms immediately on creation.
- AWS core services: IAM, EC2, S3, Lambda, API Gateway.
- Docker basics — containerize something you built in Phase 1.
- CI/CD basics (GitHub Actions) — auto-run tests on push.
- Databases beyond your BI comfort zone: working with Postgres from Python (not just SQL Server/Snowflake via BI tools).
- **AWS Certified Solutions Architect – Associate** exam prep runs in parallel through this phase and into Phase 3.
- Milestone: a small API deployed on AWS, with CI running tests automatically.

### Phase 3 — AI/LLM Engineering (Weeks 10–14)
- LLM APIs (Anthropic/OpenAI) — prompting, structured outputs, function/tool calling.
- Embeddings and vector databases: **Pinecone** as the primary tool (industry-standard managed vector DB, free tier covers this phase, paid tier if the project outgrows it) — Chroma/pgvector kept as a free local fallback for quick experiments, not the default.
- RAG architecture end to end: ingestion, chunking, retrieval, generation, citations.
- Evals — how to actually measure whether an AI system is working, not just "it looks right."
- Agentic patterns: tool use, multi-step workflows.
- Optional side-exercise: run a small quantized model locally (Ollama) and compare cost/speed/quality against the cloud API — reinforces the tradeoffs without depending on local hardware you don't have.
- **Checkpoint: entry/associate-level readiness assessment** — expect this to land around week 8–10 as noted above; resume gets its first rebuild pass here if hit.
- Milestone: a working RAG prototype over a small real document set (not yet the flagship project's full scope).

### Phase 4 — Flagship Project: RegCopilot (Weeks 15–18)
- Full build: ingest a realistic set of policy/regulatory documents → RAG pipeline with citations → risk-flagging logic → audit-ready summarization output → deployed on AWS (API Gateway + Lambda/ECS) → simple front end.
- Built in stages that mirror a real client engagement: a simulated "requirements gathering" milestone (using your PMO background deliberately), a "client demo" milestone, an "iterate on client feedback" milestone — not just a linear build.
- Testing, logging, and basic security/data-handling considerations included (this is your regulatory background's moment — treat PII/compliance handling in the project itself as a feature, not an afterthought).
- Where a true enterprise GRC/compliance platform (e.g., Palantir Foundry, OneTrust, ServiceNow GRC) isn't practical to get hands-on with, watch and dissect a real vendor demo/implementation video of that category of tool before designing the equivalent piece of RegCopilot — the goal is architecture informed by how it's actually built in industry, not an invented pattern.
- Milestone: fully deployed, demoable project with a written case-study writeup for your portfolio and interview story bank.

### Phase 5 — Certification, Interview Prep, Resume Iteration (Weeks 17–20, overlapping Phase 4)
- Sit AWS Certified Solutions Architect – Associate exam.
- Begin AI-focused AWS cert prep (AI Practitioner / ML Engineer Associate) if pace allows.
- Interview prep calibrated to this track: light-to-moderate coding screens, SQL (your strength — sharpen, don't rebuild), "design a solution for this client scenario" style system design, and heavy behavioral prep using STAR stories mined from your actual resume history.
- Mock interviews (free peer platforms) on a schedule, not just at the end.
- Resume rebuilt for mid/upper-level target roles, incorporating RegCopilot and cert(s).

### Phase 6 — Job Search Sprint (Week 20+, ongoing)
- Applications targeted at Solutions Architect / FDE / Customer Engineer postings.
- Continued mock interviews and resume iteration per role/company.
- Optional second, smaller project if a specific application calls for it.

---

## 6. Learning Method

**Delivery model: Lesson Kits.** You are not assembling a tool stack or curating your own material — I do that. Every topic ships as a complete kit under `lessons/lesson-NN-<topic>/`:

| Part | What it is |
|---|---|
| **Watch** | Specific video/course assignment — pointed at your existing Udemy courses first, free supplements only where needed |
| **Read** | A one-page PDF cheat sheet I author for that topic — concepts, syntax, real pitfalls |
| **Reinforce** | An Anki-importable flashcard deck (free, offline, no usage caps — the daily spaced-repetition tool) |
| **Listen** *(optional)* | Drop the lesson's PDF into NotebookLM for one audio-overview generation — bounded, not open-ended querying, so it won't burn through daily limits |
| **Build** | A project brief applying the lesson, threaded toward the RegCopilot flagship project where possible |

Obsidian/NotebookLM are optional deepening tools if you want to go further on your own (see `phase-0/learning-workflow.md`) — not required infrastructure. The lesson kit is self-contained.

- **Build-first, always.** Minimal theory before touching code/tools; reflect after doing, not before.
- **Real, regulated-industry-flavored scenarios** wherever possible, to keep leveraging your background.
- **Simulated on-the-job feedback**, written like a manager reviewing an employee's work, starting once entry-level competency is reached (Phase 3 checkpoint onward) — not from day one, since it wouldn't mean anything yet.
- **Gamification** (streaks, XP, levels) — tracked manually for now. A dedicated mobile/gamified companion app is a **later product phase**, once this curriculum is validated by actually going through it — not a blocker to starting.
- **Escalation on demand:** if something feels too easy, say so immediately and the difficulty goes up — no coasting. Report back after each lesson kit; the next one is built based on how that one went, not on a fixed calendar.
- **Industry-standard first.** When a real industry-standard tool matters for credibility (interviews, portfolio), use it even if it costs money — budget is not free-only. When the true industry tool genuinely isn't practical to get hands-on with (enterprise-only, prohibitively expensive, access-gated), the fallback is a video walkthrough of a real industry implementation of that category of tool, not a silent downgrade to a toy substitute.
- **Gamification stays deferred** — confirmed later-phase, not a Phase 0–6 deliverable.

---

## 7. Tools & Resources (free-first)

| Need | Resource |
|---|---|
| Notes / PDF markup | **Obsidian** (free, cross-platform, PDF annotation plugin) — raw capture only |
| AI notebook / synthesis / spaced repetition | **Google NotebookLM** (free, no trial clock) — source-grounded study guides, quizzes, and audio overviews generated from your own notes/course material; see `phase-0/learning-workflow.md` |
| Python fundamentals | **"Python 3 Programming: Beginner to Pro Masterclass"** (Ryan Ahmed) — already owned on personal Udemy, in progress (26%), chosen as the Phase 1 spine over starting fresh elsewhere. Backup/supplement if more project reps are needed: "100 Days of Code" (Angela Yu), available free via Gale/Ocean County Library. |
| CS fundamentals | **CS50x** (Harvard, free via edX), NeetCode free tier (light DSA reinforcement) |
| Cloud / AWS | AWS Skill Builder free digital training, AWS Solutions Architect – Associate free learning path |
| AI/LLM engineering (Phase 3, later) | Already owned on personal Udemy, parked until Phase 3: "Google Gemini AI with Python API" (64% done), "LangChain — Agentic AI Engineering", "LLMs with Google Cloud and Python". Plus Anthropic documentation & Anthropic Academy, DeepLearning.AI short courses (free). |
| SQL-to-Python bridge | pandas documentation, Kaggle free datasets |
| Two Udemy access points | **Personal Udemy** (owned courses, some in progress — don't expire, no rush to start the rest) and **Gale Presents: Udemy** via Ocean County Library card (free curated catalog, supplemental only for now). |
| Mock interviews | Pramp (free peer mock interviews) |

**Trial-period & spend rule:** budget isn't free-only — paying for a course, exam, or an industry-standard tool (e.g., Pinecone beyond its free tier) is fine when it's worth it, including going past a trial into a paid tier if that's what real industry usage requires. Whenever something is only free for a limited trial (a paid course platform, a software trial, cloud credits with an expiry), the phase that uses it most intensively still gets scheduled to start right when the trial starts, and the start/end date gets logged in the Obsidian vault — never let a trial clock run out unused or auto-renew unnoticed, and never stay stuck on a crippled free tier when the point is to learn the tool the way industry actually uses it.

---

## 8. Assessment & Progression Gates

- Each phase ends with a checkpoint build/challenge — no credit for "watched the video."
- Resume is rebuilt at each readiness milestone (entry-ready, mid-ready, upper-ready), not just at the end.
- You flag when something is too easy; I flag when something is a real gap, even if it's uncomfortable to hear.

---

## 9. Open Items Before Phase 0 Starts

- ~~MacBook Pro chip/RAM + Dell VDI purpose/restrictions~~ **Resolved:** 16" MacBook Pro (2019, Intel i9 8-core, AMD Radeon Pro 5500M, 16GB RAM) is the primary dev machine; Dell Inspiron 3510 is VDI-only, not a dev environment. No Apple Silicon / unified memory, so AI/LLM work defaults to cloud APIs (Anthropic, AWS Bedrock) rather than local inference. Local LLMs (Ollama) are an optional side-exercise limited to small quantized models (~3B–7B params), not the main path — this doesn't change the plan since Phase 2 onward was already AWS-first.
- ~~Confirm which Udemy library~~ **Resolved:** Ocean County Library.
- ~~Confirm rough budget for cert exam fees~~ **Resolved:** OK with ~$150–300/exam and paying for other worthwhile tools/courses — not free-only. See trial-period rule in Section 7.
- **NJIT alumni resources: not counted on** — unsure if anything's still active after time away; plan doesn't depend on it.
- ~~Confirm the companion-app decision above (later phase) still holds.~~ **Confirmed:** gamification/companion app stays deferred.
- Timeline, phase order, and cert order not explicitly pushed back on yet — treating as accepted as drafted unless you say otherwise before Phase 0.

---

## 10. Negotiation Notes

*(Use this section to record what you pushed back on and what changed, so the plan stays a living document instead of getting silently rewritten.)*

- Confirmed: budget covers going beyond a free trial into a paid tier for an industry-standard tool (e.g., Pinecone) when that's how the tool is actually used in industry — not capped at free/trial-only.
- Confirmed: prefer the real industry-standard tool over a free/toy substitute; where hands-on access to the real enterprise tool isn't practical, substitute a video walkthrough of an actual industry implementation rather than skipping the exposure.
- Confirmed: gamification/companion app stays a later phase, not part of Phases 0–6.
- Timeline (~18–20 weeks), phase order (cloud before AI/LLM), RegCopilot scope, and cert order (AWS SAA before AI-specific certs) — no objections raised; standing as drafted.
