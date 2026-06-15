# What the `last30days` skill actually is

`last30days` is an open-source ([MIT](https://github.com/mvanhorn/last30days-skill)) AI agent
skill that works as a **search engine for the last ~30 days of any topic** — scored by what real
people engage with (upvotes, likes, views, money), not by editors.

When you run it on a topic, the skill's AI agent:

1. **Searches many platforms in parallel** — Reddit (including comments), X/Twitter, YouTube
   (transcripts), TikTok, Instagram, Threads, Hacker News, Polymarket, GitHub, Bluesky,
   TruthSocial, Pinterest, and the web.
2. **Scores results by real engagement** — Reddit upvotes, X likes, YouTube views, TikTok
   engagement, Polymarket odds (real money) — so the loudest, most-validated signal rises.
3. **Synthesizes one cited brief** — an AI judge clusters, de-dupes, and ranks everything into a
   single readable summary with source links.

## Why it's different from a normal search

Google aggregates editors and old pages. Each social platform is a walled garden with its own
API and auth. `last30days` bridges them: it brings your own keys/browser sessions so one agent
can search Reddit comments, X posts, YouTube transcripts and TikTok engagement **at once** and
score them against each other. No single mainstream AI or search engine can see all of these
together.

## What you use it for

- Prep before a sales call, meeting, or interview — the recent truth about a person or company.
- Track a fast-moving topic (AI tooling, a product, a market) the way the community already sees it.
- Find what problems people are actually hitting before you build something.

## How it's invoked

```
/last30days Peter Steinberger
/last30days nvidia earnings reaction
/last30days what users want in react
```

In this catalog we wrap that into a **daily 7:00 AM morning brief** via OpenClaw — see
[`INSTALL.md`](INSTALL.md).

## Key facts

| | |
|---|---|
| Source | <https://github.com/mvanhorn/last30days-skill> |
| License | MIT — Matt Van Horn ([@mvanhorn](https://github.com/mvanhorn)) |
| Out-of-the-box (no keys) | Reddit + comments, Hacker News, Polymarket, GitHub |
| Optional (your keys) | X, YouTube, TikTok, Instagram, Threads, Pinterest, Bluesky, TruthSocial, Perplexity, web search |
| Under the hood | Python + a vendored Node search client (OpenClaw runs it for you) |

> This is a written description, not the runnable skill. OpenClaw installs the real skill from
> the upstream repo when you follow [`INSTALL.md`](INSTALL.md).
