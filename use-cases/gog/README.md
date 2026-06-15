# gog — Google Workspace for OpenClaw

Part of the **myopenclaw** use-case catalog. Each entry is a ready-to-install capability for
your OpenClaw: a few Markdown files that tell you what it does, what you need, and the exact
prompts to give OpenClaw to set it up.

This entry gives your OpenClaw control of your **Google Workspace** through the
[`gog`](https://gogcli.sh) CLI — so you can ask it, in plain language, to read and send Gmail,
check and create Calendar events, search Drive, look up Contacts, and read/update Sheets and Docs.

A natural way to use it: a **daily 7:00 AM agenda brief** — every morning OpenClaw reads today's
calendar and your important unread email and sends you one short brief.

## What's in this folder

| File | What it covers |
|------|----------------|
| [`README.md`](README.md) | This overview |
| [`SKILL.md`](SKILL.md) | What the `gog` skill is, with the full command reference |
| [`INSTALL.md`](INSTALL.md) | Copy-paste prompts to tell OpenClaw to install it, connect your Google account, and schedule the brief |
| [`PROMPTS.md`](PROMPTS.md) | A prompt for every Gmail / Calendar / Drive / Docs use case |
| [`requirements.md`](requirements.md) | What you need before installing |

## The quick version

1. Have OpenClaw set up, plus your **Gmail address** and a Google OAuth **`client_secret.json`**
   file ready (see [`requirements.md`](requirements.md)).
2. Copy the **single setup prompt** at the top of [`INSTALL.md`](INSTALL.md), put your email in,
   and paste it to OpenClaw.
3. OpenClaw installs everything, tells you where to save `client_secret.json`, authorizes your
   account, and confirms when it's done — then just ask it about your mail, calendar, and files,
   or get a 7:00 AM agenda brief every day.

## Source

The CLI is maintained upstream: <https://gogcli.sh> · ClawHub:
<https://clawhub.ai/steipete/gog> (by [@steipete](https://github.com/steipete)). This catalog
only points to it and shows you how to wire it into OpenClaw.
