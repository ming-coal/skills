# skills

Small, honest agent skills I actually use. Each one lives in its own repo so it can
be installed, versioned and criticised on its own.

| skill | what it does | works with |
|---|---|---|
| **[progress-brief](https://github.com/ming-coal/progress-brief)** | Hands a project to the next chat window in 30 seconds: scans the repo, writes a converged `PROGRESS.md`, lints it, and tells you when to restart the conversation. | OpenCode · Claude Code · Cursor · Codex · any agent with a shell |
| **[infographic-video-engine](https://github.com/ming-coal/infographic-video-engine)** | Renders explainer videos frame by frame with Skia: word-level TTS timelines, 8-way parallel encoding, procedural BGM with ducking, dual-ratio covers. Deep-brown + orange house style. | WorkBuddy · Claude Code · any agent with Python + ffmpeg |
| **[argon-optics-video-engine](https://github.com/ming-coal/argon-optics-video-engine)** | The same pipeline in a deep-space / argon-spectrum palette, plus a physically verified prism model (Snell + Cauchy). Every number on screen is recomputed from `optics_report.json`. | WorkBuddy · Claude Code · any agent with Python + ffmpeg |

---

## Installing one

```bash
# skills CLI (recommended)
npx skills add ming-coal/progress-brief

# or clone + install
git clone https://github.com/ming-coal/progress-brief
python3 progress-brief/scripts/install.py
```

See each repo's README for the other targets (`--target claude`, `--target opencode`,
`--dest`, `--dry-run`).

## A note on dependencies

`progress-brief` runs on a bare shell. The two video engines do not — they need
Python with `skia-python`, `numpy`, `scipy`, plus `ffmpeg` on PATH, and the TTS step
calls a network service. Each repo's README lists exactly what is required and what
breaks without it; neither ships a "no dependencies" claim.

## Why separate repos

Different audiences, different release cadences. A single monorepo would force one
description and one topic list onto unrelated tools; an index is enough to browse them.

MIT licensed. The index itself has no dependencies and no telemetry; each skill declares its own.
