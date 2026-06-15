# What the `gog` skill actually is

`gog` is a **Google Workspace command-line tool**. It gives an agent one consistent way to work
with **Gmail, Calendar, Drive, Contacts, Sheets, and Docs** from the terminal, authenticated to
your own Google account via OAuth. OpenClaw drives `gog` for you, so you talk in plain language
("what's on my calendar today?", "email Sam the notes") and OpenClaw runs the right command.

- **Homepage:** <https://gogcli.sh>
- **ClawHub:** <https://clawhub.ai/steipete/gog>
- **Install:** `brew install steipete/tap/gogcli`
- **Needs:** the `gog` binary + a one-time Google OAuth setup (see [`requirements.md`](requirements.md))

---

The full skill definition below is the actual artifact — you (or OpenClaw) can drop it straight
into a skills folder.

```markdown
---
name: gog
description: Google Workspace CLI for Gmail, Calendar, Drive, Contacts, Sheets, and Docs.
homepage: https://gogcli.sh
metadata: {"clawdbot":{"emoji":"🎮","requires":{"bins":["gog"]},"install":[{"id":"brew","kind":"brew","formula":"steipete/tap/gogcli","bins":["gog"],"label":"Install gog (brew)"}]}}
---

# gog

Use `gog` for Gmail/Calendar/Drive/Contacts/Sheets/Docs. Requires OAuth setup.

Setup (once)
- `gog auth credentials /path/to/client_secret.json`
- `gog auth add you@gmail.com --services gmail,calendar,drive,contacts,sheets,docs`
- `gog auth list`

Common commands
- Gmail search: `gog gmail search 'newer_than:7d' --max 10`
- Gmail send: `gog gmail send --to a@b.com --subject "Hi" --body "Hello"`
- Calendar: `gog calendar events <calendarId> --from <iso> --to <iso>`
- Drive search: `gog drive search "query" --max 10`
- Contacts: `gog contacts list --max 20`
- Sheets get: `gog sheets get <sheetId> "Tab!A1:D10" --json`
- Sheets update: `gog sheets update <sheetId> "Tab!A1:B2" --values-json '[["A","B"],["1","2"]]' --input USER_ENTERED`
- Sheets append: `gog sheets append <sheetId> "Tab!A:C" --values-json '[["x","y","z"]]' --insert INSERT_ROWS`
- Sheets clear: `gog sheets clear <sheetId> "Tab!A2:Z"`
- Sheets metadata: `gog sheets metadata <sheetId> --json`
- Docs export: `gog docs export <docId> --format txt --out /tmp/doc.txt`
- Docs cat: `gog docs cat <docId>`

Notes
- Set `GOG_ACCOUNT=you@gmail.com` to avoid repeating `--account`.
- For scripting, prefer `--json` plus `--no-input`.
- Sheets values can be passed via `--values-json` (recommended) or as inline rows.
- Docs supports export/cat/copy. In-place edits require a Docs API client (not in gog).
- Confirm before sending mail or creating events.
```

> Safety note baked into the skill: it confirms with you before sending mail or creating
> calendar events, so OpenClaw won't act on your account without a check.
