# Day 1 — New Hire Onboarding: Dev Environment

Run this like it's your first day on a real engineering team, not a tutorial. Do each step yourself on the MacBook Pro; don't skip the verification commands even if you're sure something's already installed — a new hire never assumes, they confirm.

## 1. Verify your toolchain
Open Terminal and run each of these. You're looking for a version number, not an error.

```bash
python3 --version      # want 3.10+, ideally 3.11+
pip3 --version
git --version
code --version         # VS Code CLI
```

If `code` doesn't run: open VS Code → Cmd+Shift+P → "Shell Command: Install 'code' command in PATH".

## 2. Confirm your git identity
Any real repo will reject commits without this — and you want commits attributed to you correctly for your portfolio history.

```bash
git config --global user.name
git config --global user.email
```

If either is blank or wrong, set it:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 3. Install the extensions a new engineer installs day one
In VS Code, install:
- **Python** (Microsoft)
- **Pylance**
- **Ruff** — industry-standard fast linter/formatter (replacing older flake8+black combos at a lot of companies now)
- **GitLens** (optional, but genuinely useful for reading history/blame)

## 4. Stand up your own work repo
Your `Git_Series` repo stays as the planning/reference space. Real engineers don't dump every project into one repo — create a dedicated one for this track's hands-on work.

1. On GitHub, create a new repo: `swe-ai-bootcamp` (or a name you prefer) — public if you want it portfolio-visible, private is fine too for now.
2. Clone it locally into a sensible spot:
   ```bash
   mkdir -p ~/dev && cd ~/dev
   git clone git@github.com:<your-username>/swe-ai-bootcamp.git
   cd swe-ai-bootcamp
   ```
3. Scaffold it like a real project on day one:
   ```bash
   mkdir src tests
   touch README.md
   ```
4. Add a Python `.gitignore` (GitHub's template, or `gitignore.io` for "Python" + "VisualStudioCode" + "macOS").

## 5. Create your virtual environment
Every real Python project isolates its dependencies — never install packages globally.

```bash
python3 -m venv .venv
source .venv/bin/activate      # your prompt should now show (.venv)
pip install --upgrade pip
pip install pytest
pip freeze > requirements.txt
```

## 6. Prove the environment works (your first "ticket")
This is the literal exercise a new hire gets handed on day one to prove their laptop is wired correctly before touching real work.

`src/hello_env.py`:
```python
import sys


def python_version() -> str:
    return sys.version.split()[0]


if __name__ == "__main__":
    print(f"Environment OK — running Python {python_version()}")
```

`tests/test_hello_env.py`:
```python
from src.hello_env import python_version


def test_python_version_is_reported():
    version = python_version()
    assert version.startswith("3.")
```

Run it:
```bash
python src/hello_env.py
pytest
```
Both should succeed — a printed version string, and `1 passed`.

## 7. Write the README like a real project, not a placeholder
A one-liner is fine for now, but write it like someone else might land on this repo:
```markdown
# SWE → AI Solutions Architect / FDE Bootcamp Labs

Hands-on exercises and projects for a self-directed bootcamp track,
built alongside the syllabus in jd0425/Git_Series.
```

## 8. First commit
```bash
git add .
git commit -m "Set up project scaffold and verify dev environment"
git push
```

---

**Done when:** `pytest` passes, the commit is pushed, and you can see it on GitHub. That's Day 1. Report back here (or just start Phase 1 material) — no need to wait on anything else.
