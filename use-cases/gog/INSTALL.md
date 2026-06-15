# Install & connect — just talk to OpenClaw

You don't run any commands yourself. Open a chat with **OpenClaw** and paste the **one prompt**
below. OpenClaw installs `gog`, tells you where to drop your `client_secret.json`, authorizes
your account, and confirms when it's done.

## ⚡ One prompt — copy, fill in your email, paste to OpenClaw

> Before you start you need two things (details in [`requirements.md`](requirements.md)):
> your **Gmail address** and a **Google OAuth `client_secret.json`** file. OpenClaw will tell
> you the exact path to save the file when it asks.

```
Set up the "gog" Google Workspace tool in my OpenClaw. Follow this guide:
https://github.com/anujsonawane60/myopenclaw/tree/main/use-cases/gog

My Google account: you@gmail.com

Do the whole setup end to end and walk me through it:
1. Install the gog CLI (brew install steipete/tap/gogcli) and the gog skill
   (https://clawhub.ai/steipete/gog).
2. Tell me the exact file path where I should save my Google OAuth client_secret.json,
   then pause and wait until I confirm I've saved it there.
3. Register those credentials and authorize you@gmail.com for gmail, calendar, drive,
   contacts, sheets, and docs.
4. Verify it works by listing my next 3 calendar events, then tell me setup is complete.

Never send email or create calendar events without asking me first.
```

That's the whole setup. **What happens after you paste it:**

1. OpenClaw installs the `gog` CLI + skill.
2. OpenClaw replies with the **exact path** to save your `client_secret.json` → you put the file
   there and tell OpenClaw "done".
3. OpenClaw authorizes your account (a Google sign-in / consent window).
4. OpenClaw lists your next 3 events and confirms **setup complete**. ✅

Then you can schedule a 7:00 AM agenda brief (Step 3 below) or just start asking
([`PROMPTS.md`](PROMPTS.md) has a prompt for every Gmail/Calendar/Drive/Docs action).

---

## Prefer step-by-step? (same thing, broken out)

> Replace **you@gmail.com** with your real Google address, and the **bracketed bits** with what
> you actually want.

---

## Step 1 — Tell OpenClaw to install the skill

> **Paste this:**
>
> ```
> Install the "gog" Google Workspace skill from this source:
> https://clawhub.ai/steipete/gog   (homepage: https://gogcli.sh)
>
> It's a CLI for Gmail, Calendar, Drive, Contacts, Sheets, and Docs. Install the gog
> binary (brew install steipete/tap/gogcli) and set up the skill in my OpenClaw.
> ```

OpenClaw installs the `gog` binary and the skill. Next it needs to connect to your Google account.

---

## Step 2 — Connect your Google account (one-time OAuth)

> **Paste this:**
>
> ```
> Connect my Google account to gog. Walk me through the OAuth setup step by step:
> registering credentials and authorizing you@gmail.com for gmail, calendar, drive,
> contacts, sheets, and docs. Then confirm it works by listing my next 3 calendar events.
> ```

OpenClaw will guide you through the one-time setup (it runs `gog auth credentials …`,
`gog auth add you@gmail.com --services …`, then `gog auth list` under the hood). You only do
this once. See [`requirements.md`](requirements.md) for what the OAuth step needs.

---

## Step 3 — Schedule a 7:00 AM agenda brief

> **Paste this:**
>
> ```
> Every day at 7:00 AM, using gog for you@gmail.com, send me a short "Morning Agenda":
> - today's calendar events (time + title),
> - my important unread emails from the last 24 hours (sender + subject + one-line gist).
> Keep it to a 2-minute read, lead with my first meeting, and don't send any email or
> create any events without asking me first.
> ```

OpenClaw schedules a recurring 7:00 AM job and delivers the agenda to you each morning.

---

## Now just ask, in plain language

Once connected, you don't need commands — talk to OpenClaw. For a prompt covering **every**
Gmail / Calendar / Drive / Docs use case, see [`PROMPTS.md`](PROMPTS.md). A few to start:

> ```
> Search my Gmail for anything about [the invoice] from the last 7 days and summarize it.
> ```

> ```
> Draft a reply to [Sam]'s last email saying I'll have it by Friday — show it to me before sending.
> ```

> ```
> Put [Dentist] on my calendar next Tuesday at 3pm for 30 minutes.
> ```

> ```
> Pull the values from [Budget sheet] tab "Q2!A1:D10" and tell me the total.
> ```

> ```
> Export the Google Doc [Project plan] to text and give me the summary.
> ```

---

## Safety

The skill is set to **confirm with you before sending mail or creating calendar events**, so
OpenClaw won't act on your account without a check. Reading (search, list, export) is safe to
run freely.
