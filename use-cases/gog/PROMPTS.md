# gog prompts — by use case

Copy-paste prompts to give **OpenClaw** for every Google Workspace use case. Each prompt sits in
its own code block (use the copy button on GitHub). Replace anything in **[brackets]** with your
own details, and **you@gmail.com** with your address.

> Set up first: install + connect your Google account using [`INSTALL.md`](INSTALL.md).
> Reading is safe to run freely; OpenClaw confirms before **sending mail or creating events**.

---

## 1. Gmail

**Search emails**
```
Search my Gmail for emails about [the Q2 contract] and list the top 10 with sender, date, and subject.
```

**Read emails**
```
Open the most recent email from [client@company.com] and give me the full text.
```

**Draft / send emails**
```
Draft a follow-up email to [client@company.com] with subject "Following up" saying [I'd like to reconnect this week]. Show it to me before sending.
```

**Inspect threads**
```
Pull the whole email thread with [Sam] about [the launch] and summarize what was decided and what's still open.
```

**Manage labels**
```
List my Gmail labels, then apply the label [Clients] to all emails from [client@company.com] in the last 30 days.
```

**Organize inbox workflows**
```
Triage my inbox: group unread emails from the last 24 hours into "needs a reply", "FYI", and "can ignore", and show me the "needs a reply" ones first.
```

**Settings-related (scope-dependent)**
```
Check what Gmail settings gog can access with my granted scopes, and tell me my current signature and any active vacation responder.
```

### Gmail examples
```
Find all my unread mail from today.
```
```
Search recent emails from [client@company.com] in the last 7 days.
```
```
Send follow-ups to anyone I haven't replied to from [last week] — draft them and let me review before sending.
```
```
Triage my inbox and tell me the 5 messages that actually need me.
```
```
Pull context from my email thread with [Sam] so I'm ready for our call.
```

---

## 2. Google Calendar

**List events**
```
List my calendar events for [this week] with time and title.
```

**Create events**
```
Create a meeting [Project sync] on [next Tuesday] from [3:00pm to 3:30pm] and invite [sam@company.com]. Confirm with me before creating it.
```

**Update events**
```
Move my [Project sync] meeting on [Tuesday] to [4:00pm] and let me confirm before you change it.
```

**Review daily schedule**
```
Walk me through my schedule for today, meeting by meeting, with any locations or links.
```

**Check availability / conflicts**
```
Find my free 30-minute windows [tomorrow afternoon] and flag any double-booked or overlapping meetings.
```

**Manage meeting details**
```
For my [Project sync] meeting, show the attendees, description, and any attached link, and add [agenda: review milestones] to the notes after I confirm.
```

### Calendar examples
```
Create a meeting with [Sam] [tomorrow at 2pm] for 1 hour.
```
```
List today's calendar.
```
```
Prepare my daily agenda: today's events plus what I need to prep for each.
```
```
Check my free time windows [Thursday].
```
```
Show my work calendar and my personal calendar side by side for [this week].
```

---

## 3. Google Drive

**Search files**
```
Search my Drive for [the pricing proposal] and list the top 10 matches with name, type, and last-modified date.
```

**Inspect folder / file structures**
```
Show me the contents of my Drive folder [Clients/Acme] — files and subfolders.
```

**Retrieve metadata**
```
Give me the metadata for [Proposal v3]: owner, last modified, size, and type.
```

**Audit files**
```
Audit my Drive for files I haven't touched in [6 months] that match [invoice] and list them so I can clean up.
```

**Organize document lookup workflows**
```
Find the latest version of [the onboarding doc] in my Drive and give me the link plus when it was last edited.
```

### Drive examples
```
Find a proposal doc about [Acme].
```
```
Search my spreadsheets for the keyword [budget].
```
```
Show me my most recent files from the last 7 days.
```
```
Review the contents of my [Clients] folder.
```
```
Find the [contract template] so we can use it as a starting point.
```

---

## 4. Google Docs

**Read documents**
```
Read the Google Doc [Project plan] and give me a summary with the key points.
```

**Export documents**
```
Export the Google Doc [Meeting notes] to plain text and save it to [/tmp/notes.txt].
```

**Copy documents**
```
Make a copy of my Google Doc [Proposal template] named [Proposal — Acme] so I can fill it in.
```

**Richer Docs commands (newer gog versions)**
```
Check which Docs commands my installed gog version supports, then use them to [insert a heading "Summary" at the top of [Project plan]] — show me what you'll do before editing.
```

### Docs examples
```
Pull the text from [Project plan] so I can quote it.
```
```
Export my [meeting notes] to a text file.
```
```
Duplicate my [proposal template] for a new client.
```
```
Use [the onboarding doc] as a knowledge source and answer: [what's our refund policy]?
```
