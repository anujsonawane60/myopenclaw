# OpenClaw Use Cases

A catalog of ready-to-use **OpenClaw** use cases. Each entry is a small folder of Markdown that
tells you what a capability does, what you need, and the **exact prompts to paste to OpenClaw** to
set it up. You don't run commands yourself — you talk to OpenClaw, and it installs and schedules
things for you.

> Come to this repo, find a use case, copy the prompts, paste them to OpenClaw. Done.

## Catalog

| Use case | What it does | Based on | Entry |
|----------|--------------|----------|-------|
| **last30days** | Daily 7:00 AM morning brief: what people said about your topics in the last ~30 days, scored by real engagement (Reddit/X/YouTube/TikTok/Polymarket/…) | [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) (MIT) | [`use-cases/last30days/`](use-cases/last30days/) |
| **gog** | Google Workspace from OpenClaw — Gmail, Calendar, Drive, Contacts, Sheets, Docs in plain language; optional 7:00 AM agenda brief | [gogcli.sh](https://gogcli.sh) · [clawhub.ai/steipete/gog](https://clawhub.ai/steipete/gog) | [`use-cases/gog/`](use-cases/gog/) |

Full index: [`use-cases/`](use-cases/).

## How to use a use case

1. Make sure your **OpenClaw is set up** (that's usually the only requirement).
2. Open the use case's folder and read its `README.md`.
3. Copy the prompts from its `INSTALL.md` and paste them to OpenClaw.
4. OpenClaw installs the skill, connects any accounts, and schedules the task for you.

Every prompt lives in a fenced code block, so on GitHub each has a one-click **copy** button.

## Layout

```
.
├── use-cases/             # The catalog — one folder per use case
│   ├── README.md          #   index of all use cases + how to add one
│   ├── last30days/        #   daily morning brief of any topic
│   └── gog/               #   Google Workspace (Gmail/Calendar/Drive/Docs)
└── README.md              # This file
```

## Anatomy of a use case

Each `use-cases/<name>/` folder contains:

| File | What it's for |
|------|---------------|
| `README.md` | What it does, when to use it, the quick version |
| `SKILL.md` | What the underlying skill actually is (and the artifact, if small) |
| `INSTALL.md` | Copy-paste prompts to give OpenClaw — install, connect, schedule |
| `requirements.md` | What you need first (usually just OpenClaw set up) |
| `PROMPTS.md` | *(optional)* a prompt for every individual use case, e.g. [`gog`](use-cases/gog/PROMPTS.md) |

## Add a new use case

1. Create `use-cases/<name>/`.
2. Add `README.md`, `SKILL.md`, `INSTALL.md`, and `requirements.md` (and `PROMPTS.md` if the
   skill has many distinct actions).
3. Put every prompt the user should copy inside a fenced ```` ``` ```` code block.
4. Add a row to the catalog tables in this file and in [`use-cases/README.md`](use-cases/README.md).

See [`use-cases/`](use-cases/) for the conventions and the existing entries as examples.
