# RepoScout Use Case Run — delegate (E2E)
Date: 2026-02-17 19:32 UTC

## Use case
**Goal:** Spin up a local multi‑agent team and confirm the system boots end‑to‑end.

## Setup
- Installed Claude CLI (required by Delegate)
- Exported ANTHROPIC_API_KEY
- Created a local git repo: `/tmp/delegate-demo`

## Command
```
delegate start --foreground
```

## Result (highlights)
- ✅ Created team `delegate-demo` with delegate + 5 agents
- ✅ Default workflow registered
- ✅ Repo detected and registered
- ✅ Server started on **http://0.0.0.0:3548**
- ✅ Frontend build completed
- ✅ Daemon loop started

## Output (excerpt)
```
Delegate v0.2.5

[*] Auth: API key (sk-a...)
[*] Created team 'delegate-demo' with delegate + 5 agents (botchi)
[*] Registered default workflow
[*] Detected and registered repo: delegate-demo
[*] Starting delegate on port 3548...
... Frontend build complete
... Daemon loop started — polling every 1.0s
Uvicorn running on http://0.0.0.0:3548
```

## Time & Cost
- Boot time: ~5–10s to ready
- Cost: minimal (no agent tasks run yet)

## Value
- Confirms full local orchestration bootstraps correctly.
- Establishes base environment for task execution.

## Next
- Trigger a real task (e.g., create a small file, run tests) and observe review/merge flow.
