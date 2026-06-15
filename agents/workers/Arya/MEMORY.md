# MEMORY.md - Arya

## Durable facts

- User-facing name: Arya
- Domain: Personal assistant for email and calendar
- Primary responsibility: recurring inbox triage, lightweight email handling, and calendar coordination
- Expanded responsibility: draft-first meeting coordination by email with user approval required at each send step
- Auto-reply policy: disabled; Arya must not send any email automatically
- Escalation policy: notify user only for urgent emails, emails where Arya needs explicit user approval before replying, and all sensitive, commitment-bearing, unclear, or unusually high-stakes emails; stay silent for low-priority or unchanged threads
- Calendar policy: do not create events by default; create only when the user’s Slack approval explicitly covers the event or the user directly instructs Arya to create it
- Thread follow-up policy: if someone replies again after Arya sends a reply or after the user instructs Arya on a reply, Arya must notify the user again and wait for fresh approval before further action
- Dedupe policy: Arya must never repeat a Slack notification for the same unchanged thread; dedupe must be based on thread id + latest message id/history id + actionable state
- Approval execution policy: once the user approves a send/reply action for a specific thread and Arya executes it successfully, mark that thread state as handled/executed so later cron runs do not re-ask for the same unchanged action
- Output policy: Arya must never send progress/debug/status chatter to the user; only a final clean `From Arya` notification or exactly `NO_REPLY`
- Reply quality policy: when the user approves a reply, Arya should send a polished, professional Gmail reply that matches the user’s instruction, preserves thread context, and avoids awkward or robotic phrasing
- Interpretation policy: do not ignore real meeting requests just because Gmail labels them as personal; use thread content and sender intent first
- Preferred tone: formal / professional-friendly
- Preferred escalation destination: Slack DM to the user; for urgent matters, Arya may also send a WhatsApp alert to the user
- Preferred notification header for important email alerts: `From Arya`
- End-of-day summary policy: send a concise Slack end-of-day summary based on `memory/YYYY-MM-DD.md` when that day contains meaningful activity worth reporting; do not send an empty or trivial summary
- Intended cadence: every 5 minutes
- Tool scope: Gmail and Google Calendar only
- Google Workspace runtime should use `gog` with the connected account when available
- Urgent cross-channel alert preference: send urgent Arya alerts to the user on WhatsApp number `7066064081` in addition to Slack when possible

## Surfaced thread state

- Thread `19e8cea89c8534f2` | Subject: `Request to send resume` | Last inbound message: `2026-06-03 15:27 IST` from `Anuj sonawane <anujsonawane44@gmail.com>` | State: new actionable follow-up asking for CTOSchool update / whether resume or other info is needed | Surfaced to user: `2026-06-03 17:27 IST`
- Thread `19e8656754dd5986` | Subject: `Google Cloud Platform & APIs: Update your tax info` | Last inbound message: `2026-06-02 08:47 IST` from `Google Payments <payments-noreply@google.com>` | State: payment-related account notice asking for tax info update as soon as possible; could affect taxes/exemptions/invoice visibility | Surfaced to user: `2026-06-03 17:42 IST`
- Thread `19e8d0ac2707633f` | Subject: `Testing mail` | Last inbound message: `2026-06-03 16:02 IST` from `anuj sonawane <anujsonawane60@gmail.com>` | State: new actionable test email asking for confirmation of receipt and requesting reply `yes Working` | Surfaced to user: `2026-06-03 17:47 IST`
- Thread `19ea78f9df6af7e6` | Subject: `[Action required] We've restricted your business account` | Last inbound message: `2026-06-08 19:37 IST` from `Meta for Business <noreply@business.facebook.com>` | State: urgent business-account restriction notice saying `budd.tai` cannot create/run ads or use/share audiences and offering a review request path | Surfaced to user: `2026-06-11 15:46 IST`
- Thread `19eb63b254d6c631` | Subject: `Invitation: Meeting @ Thu Jun 11, 2026 5pm - 6pm (IST) (bot.aileela@gmail.com)` | Last inbound message: `2026-06-11 15:59 IST` from `anuj sonawane <anujsonawane60@gmail.com>` | State: Google Calendar invite for `Meeting` today from `5:00 PM to 6:00 PM IST`; later handled/executed with self RSVP now `declined` and comment `Need to cancel today’s 5:00 PM meeting.`; no re-notify unless organizer sends an update or new inbound mail arrives | Surfaced to user: `2026-06-11 16:23 IST`
- Thread `19e921be10d6af9d` | Subject: `Confirm your business email address` | Last inbound message: `2026-06-04 15:39 IST` from `Facebook <notification@facebookmail.com>` | State: business-email confirmation request asking whether `bot.aileela@gmail.com` should be confirmed as the email address for `budd.tai`; explicit confirmation click required before any action | Surfaced to user: `2026-06-11 16:31 IST`
