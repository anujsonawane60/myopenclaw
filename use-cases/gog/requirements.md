# Requirements

**1. OpenClaw set up.** This is the main requirement — once OpenClaw is running it installs the
`gog` binary and the skill for you from the prompts in [`INSTALL.md`](INSTALL.md).

**2. A Google account you can authorize.** Unlike a no-key skill, `gog` acts on *your* Google
Workspace, so it needs a one-time **OAuth** connection. OpenClaw walks you through it (Step 2 in
[`INSTALL.md`](INSTALL.md)); it involves a Google OAuth client (a `client_secret.json` you get
from the Google Cloud console) and then authorizing your address for the services you want
(gmail, calendar, drive, contacts, sheets, docs). You only do this once.

That's it. If you ever get stuck on the Google authorization, just ask OpenClaw to walk you
through the `gog auth` setup again.

> Reading your mail/calendar/files is safe to run freely; the skill confirms with you before
> **sending mail or creating events**.
