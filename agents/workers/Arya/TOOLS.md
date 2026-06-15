# TOOLS.md - Arya

## Preferred Email Runtime

- Google Workspace access through `gog`
- Gmail operations should use the authenticated `gog` account environment when available

## Preferred Calendar Runtime

- Google Calendar through `gog`

## Required Runtime Context

For dependable execution, ensure the runtime has:
- `PATH=/home/ubuntu/.local/bin:$PATH`
- `GOG_HOME=/home/ubuntu/.openclaw/workspace/.gog`
- `GOG_KEYRING_BACKEND=file`
- `GOG_KEYRING_PASSWORD` set correctly
- `GOG_ACCOUNT=bot.aileela@gmail.com`

## Delivery Preference

- escalations should be sent to the user on Slack
- concise summary first, recommended action second

## Logging

- Arya durable memory file: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/MEMORY.md`
- Arya daily log folder: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/memory`
- human-readable daily logs should be stored as: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/memory/YYYY-MM-DD.md`
- Arya logs folder: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/logs`
- structured run log file: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/logs/run-log.jsonl`
- human-readable rolling status summary: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/logs/status-summary.md`
- machine state such as dedupe data may live under: `/home/ubuntu/.openclaw/workspace/agents/generated/arya-email-assistant-agent/memory/*.json`
- each Arya run should record lifecycle/status information when possible, including: `run_started`, `completed`, `incomplete`, `blocked`, `failed`, `notified`, and `skipped_duplicate`
- durable policies and cross-run facts belong in `MEMORY.md`; day-wise operational notes belong in `memory/YYYY-MM-DD.md`

## Scheduling Note

- recurring 15-minute checks should eventually be bound to a durable scheduler/runtime rather than ad hoc invocation
