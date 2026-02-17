# RepoScout Report — delegate
URL: https://github.com/nikhilgarg28/delegate
Date: 2026-02-17 16:57 UTC

Cloned: False (already exists)
Stack: python, node
License: MIT
Stars: 14
Forks: 0
Open issues: 1
Last push: 2026-02-17T05:29:32Z

## README (first 30 lines)
<p align="center">
  <img src="branding/logo.svg" alt="delegate" height="40">
</p>

<p align="center">
  <strong>Not a copilot. A team that ships.</strong><br>
  <sub>AI agents that plan, code, review each other's work, and merge — running locally on your machine.</sub>
</p>

<p align="center">
  <a href="https://pypi.org/project/delegate-ai/"><img src="https://img.shields.io/pypi/v/delegate-ai" alt="PyPI"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT License"></a>
  <a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/python-3.12+-blue" alt="Python 3.12+"></a>
</p>

---

Delegate creates a persistent team of AI agents on your local machine. Describe what you want in plain English — Delegate breaks it into tasks, assigns them to agents, manages code reviews between them, and merges the result. You watch it all happen in a real-time web UI, or check in later. The team remembers your codebase across tasks.

> **Note:** Delegate currently works with **local git repositories** — agents commit directly to branches on your machine. Support for remote repositories (GitHub, GitLab), external tools (Slack, Linear), and CI/CD integrations is coming soon - stay tuned!

## Tests
Command: `bash -lc 'source /home/node/.openclaw/.openclaw/workspace/.venv/bin/activate && pytest -q'`
Result: exit=0

### STDOUT (tail)
817 passed, 146 skipped, 11 warnings in 81.25s (0:01:21)

## Hands‑on notes
- ✅ Test suite runs cleanly (warnings are about missing pytest-asyncio markers).
- 🔧 Requires Python 3.12+ and Anthropic key for actual agent runs.
- ⚠️ Local‑repo only (no GitHub PRs yet).

## How we tried it
- Ran unit tests locally via pytest.
- Next step would be `delegate start` (needs ANTHROPIC_API_KEY) to exercise UI/workflow.

## How we'd use it
- Long‑running agent teams for repo maintenance, QA, and batch refactors.
- Best fit when you want **multi‑agent workflows + review gates** locally.
