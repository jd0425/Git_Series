# Project: Regulatory Deadline Tracker

**Why this project:** it's small enough to finish with only Lesson 1's material (variables, data types, operators, control flow), and it's the first thread of the "RegCopilot" flagship project's world — you're building the same kind of thing you'll manage for real clients later, just at the smallest possible scale today.

## The task

You've got a hardcoded list of compliance items (a stand-in for what would later come from a real database or document). Write a script that produces a status report from it.

Starter data — put this at the top of your script, don't overthink it, the data is given:

```python
compliance_items = [
    {"name": "OCC Q3 Risk Report", "days_until_due": 5, "status": "in_progress"},
    {"name": "FDA Device Attribute Review", "days_until_due": -3, "status": "in_progress"},
    {"name": "Vendor Access Recertification", "days_until_due": 12, "status": "not_started"},
    {"name": "SOC 2 Evidence Collection", "days_until_due": 0, "status": "in_progress"},
    {"name": "Annual Policy Attestation", "days_until_due": 30, "status": "complete"},
]
```

## Requirements

Your script must:

1. **Classify each item** based on `days_until_due`:
   - Negative → `"OVERDUE"`
   - `0` → `"DUE TODAY"`
   - `1`–`7` → `"DUE THIS WEEK"`
   - `8+` → `"UPCOMING"`
   - (Regardless of days, if `status == "complete"`, classify it as `"COMPLETE"` instead — completion overrides the date.)

2. **Print a formatted report**, one line per item, like:
   ```
   [OVERDUE]       FDA Device Attribute Review          (3 days overdue, in_progress)
   [DUE TODAY]     SOC 2 Evidence Collection             (due today, in_progress)
   [DUE THIS WEEK] OCC Q3 Risk Report                    (5 days left, in_progress)
   [UPCOMING]      Vendor Access Recertification         (12 days left, not_started)
   [COMPLETE]      Annual Policy Attestation             (30 days left, complete)
   ```
   Exact spacing/formatting is up to you — the point is it's readable, not that it matches character-for-character.

3. **Print a summary count** at the end: how many items in each category (`OVERDUE`, `DUE TODAY`, `DUE THIS WEEK`, `UPCOMING`, `COMPLETE`).

4. **Sort the report** so `OVERDUE` items appear first, then `DUE TODAY`, then `DUE THIS WEEK`, then `UPCOMING`, then `COMPLETE` — not in the original list order.

## Stretch goals (optional, only if the core felt easy)

- Take `compliance_items` in as a function argument instead of a global, and write a `classify(item) -> str` function you can reason about independently.
- Add a `owner` key to each item and group the summary by owner as well as by status.
- Handle a malformed item gracefully (e.g. missing `days_until_due`) without crashing the whole report.

## What "done" looks like

- Runs with `python project.py` (or similar) and produces correct output for the sample data above.
- Uses `if`/`elif`/`else` for the classification logic — no hardcoding the answer.
- Uses a loop to process the list — no copy-pasted per-item code.
- Committed to your `python-foundations-lab` repo with a short README section describing what it does.

If this felt genuinely easy and fast, say so — that's the signal to skip ahead rather than grind more lessons at this level.
