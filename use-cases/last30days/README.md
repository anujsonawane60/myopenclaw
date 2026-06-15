# last30days — Morning Brief use case

Part of the **myopenclaw** use-case catalog. Each entry is a ready-to-install capability for
your OpenClaw: a few Markdown files that tell you what it does, what you need, and the exact
prompts to give OpenClaw to set it up.

This entry turns the [`last30days`](https://github.com/mvanhorn/last30days-skill) skill into a
**daily 7:00 AM morning brief** — every morning OpenClaw researches the topics you care about
across Reddit, X, YouTube, TikTok, Polymarket, Hacker News and more, scores them by what people
actually engage with, and sends you one short brief.

## What's in this folder

| File | What it covers |
|------|----------------|
| [`README.md`](README.md) | This overview |
| [`SKILL.md`](SKILL.md) | What the `last30days` GitHub skill actually is and does |
| [`INSTALL.md`](INSTALL.md) | Copy-paste prompts to tell OpenClaw to install it and schedule the 7:00 AM brief |
| [`requirements.md`](requirements.md) | What you need before installing |

## The quick version

1. Make sure you have OpenClaw set up (see [`requirements.md`](requirements.md)).
2. Copy the **single setup prompt** at the top of [`INSTALL.md`](INSTALL.md), add your topics,
   and paste it to OpenClaw.
3. OpenClaw installs the skill, schedules the job, and confirms — then you get a morning brief at
   7:00 AM every day. No accounts or API keys needed to start.

## Source

The skill itself is maintained upstream: <https://github.com/mvanhorn/last30days-skill>
(MIT, by [@mvanhorn](https://github.com/mvanhorn)). This catalog only points to it and shows
you how to wire it into OpenClaw as a scheduled morning brief.
