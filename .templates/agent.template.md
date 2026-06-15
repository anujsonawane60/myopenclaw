---
name: <kebab-case-name>
description: <one line — what this agent does and when to use it>
role: orchestrator | gateway | worker
version: 0.1.0
model: claude-opus-4-8        # or claude-sonnet-4-6 / claude-haiku-4-5
tools:                        # tools this agent may use ("*" for all)
  - read
  - write
skills:                       # skills to preload (see /skills)
  - <skill-name>
owner: <your-name>
status: draft                 # draft | active | deprecated
---

# <Agent Name>

## Purpose
One paragraph describing the agent's job and the boundary of its responsibility.

## System prompt
The actual instructions given to the model. Be explicit about goals,
constraints, tone, and what "done" looks like.

## Inputs
- What the agent expects to receive.

## Outputs
- What the agent is expected to produce.

## Examples
> **User:** ...
> **Agent:** ...

## Notes
Anything maintainers should know (limitations, related agents via [[name]]).
