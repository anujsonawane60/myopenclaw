# Install & schedule — just talk to OpenClaw

You don't run any commands yourself. Open a chat with **OpenClaw** and paste the prompts below.
OpenClaw installs the skill and sets up the 7:00 AM morning brief for you.

> Replace the **topics in brackets** with what you actually want to follow — a company, a
> person, a product, your competitors, a technology, anything.

---

## Step 1 — Tell OpenClaw to install the skill

> **Paste this:**
>
> ```
> Install the "last30days" skill from this GitHub repository:
> https://github.com/mvanhorn/last30days-skill
>
> It researches any topic across Reddit, X, YouTube, TikTok, Hacker News, Polymarket
> and GitHub, scored by real engagement. Set it up in my OpenClaw and confirm it.
> ```

OpenClaw will install it from <https://github.com/mvanhorn/last30days-skill>
(`clawhub install last30days-official` under the hood) and run a test.
Reddit, Hacker News, Polymarket and GitHub work immediately — no API keys needed.

---

## Step 2 — Tell OpenClaw to schedule a 7:00 AM morning brief

> **Paste this:**
>
> ```
> Every day at 7:00 AM, run last30days on these topics for me:
> [AI coding tools], [my company name], [my main competitor].
> Summarize what's new in the last 30 days — the most engaged Reddit threads, X posts,
> YouTube videos and any market-moving news — and send it to me as a short "Morning Brief"
> I can read in two minutes. Keep it punchy, lead with the single biggest thing, and link sources.
> ```

OpenClaw schedules a recurring 7:00 AM job and delivers the brief to you each morning.

---

## Optional — tweak the brief

Just tell OpenClaw in plain language, for example:

> ```
> Change my morning brief to 6:30 AM and only include the top 5 items.
> ```

> ```
> Add [my product] to my morning brief topics and drop [old topic].
> ```

> ```
> Unlock X and YouTube for my morning brief — walk me through adding the keys.
> ```

---

## What you'll get

A short daily brief that looks roughly like:

```
🌅 Morning Brief — last 30 days
Topic: AI coding tools

1. Biggest thing: <one-line headline>  (Reddit, 1.2k upvotes)
2. <headline>  (X, 4.5k likes)
3. <headline>  (YouTube, 200k views)
...
Sources: <links>
```
