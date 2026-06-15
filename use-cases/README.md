# Use Cases

A catalog of ready-to-install OpenClaw use cases. Each entry is a small folder of Markdown that
tells you what the use case does, what you need, and the exact prompts to give OpenClaw to set
it up. You don't run commands yourself — you talk to OpenClaw.

## How an entry is structured

```
use-cases/<name>/
  README.md        # what it does, when to use it
  SKILL.md         # what the underlying skill actually is
  INSTALL.md       # copy-paste prompts to give OpenClaw (install + schedule)
  requirements.md  # what you need (usually just OpenClaw set up)
```

## Catalog

| Use case | What it does | Based on | Entry |
|----------|--------------|----------|-------|
| **last30days** | Daily 7:00 AM morning brief: what people said about your topics in the last ~30 days, scored by real engagement (Reddit/X/YouTube/TikTok/Polymarket/…) | [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) (MIT) | [`last30days/`](last30days/) |
| **gog** | Google Workspace from OpenClaw — Gmail, Calendar, Drive, Contacts, Sheets, Docs in plain language; optional 7:00 AM agenda brief | [gogcli.sh](https://gogcli.sh) · [clawhub.ai/steipete/gog](https://clawhub.ai/steipete/gog) | [`gog/`](gog/) |

## Adding a new use case

1. Create `use-cases/<name>/`.
2. Add `README.md` (what + when), `SKILL.md` (what the underlying skill is),
   `INSTALL.md` (the OpenClaw prompts), and `requirements.md`.
3. Add a row to the **Catalog** table above.
