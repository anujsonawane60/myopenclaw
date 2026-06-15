# Install & connect — just talk to OpenClaw

You don't run these commands yourself. Open a chat with **OpenClaw** and paste the prompts below.
OpenClaw installs `gog`, walks you through connecting your Google account, and sets up the
7:00 AM agenda brief.

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
