# skills

Small, honest agent skills I actually use. Each one lives in its own repo so it can
be installed, versioned and criticised on its own.

| skill | what it does | works with |
|---|---|---|
| **[progress-brief](https://github.com/ming-coal/progress-brief)** | Hands a project to the next chat window in 30 seconds: scans the repo, writes a converged `PROGRESS.md`, lints it, and tells you when to restart the conversation. | OpenCode · Claude Code · Cursor · Codex · any agent with a shell |

---

## Installing one

```bash
git clone https://github.com/ming-coal/progress-brief
python3 progress-brief/scripts/install.py
```

See each repo's README for the other targets (`--target claude`, `--agents-md`, `--prompt`).

## Why separate repos

Different audiences, different release cadences. A single monorepo would force one
description and one topic list onto unrelated tools; an index is enough to browse them.

MIT licensed, no dependencies, no telemetry.
