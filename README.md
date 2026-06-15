# OpenClaw Agents

Central repository for **OpenClaw** agent definitions. Every agent is a single
Markdown file (`*.agent.md`) with YAML frontmatter for metadata and a Markdown
body for the system prompt / instructions.

## Layout

```
.
├── agents/                # Agent definitions, grouped by role
│   ├── orchestrator/      #   coordinator agents that delegate work
│   ├── gateway/           #   OpenClaw Gateway entry-point agents
│   └── workers/           #   task-focused agents doing the actual work
├── use-cases/             # Catalog of installable use cases (pointers to upstream skills)
├── skills/                # Reusable, composable skills agents can load
├── workflows/             # Multi-agent pipelines (which agents run, in what order)
├── shared/                # Content reused across agents
│   ├── prompts/           #   prompt fragments / partials
│   └── context/           #   shared domain context, glossaries, policies
├── registry/              # Machine-readable index of all agents
├── docs/                  # Authoring guides and conventions
└── .templates/            # Templates for new files
```

## Quick start

1. Copy `.templates/agent.template.md` into the right `agents/<role>/` folder.
2. Rename it `<name>.agent.md` (kebab-case).
3. Fill in the frontmatter and the prompt body.
4. Add a row to `registry/agents.md`.

See [`docs/CONVENTIONS.md`](docs/CONVENTIONS.md) for the full spec.

## Use-case catalog

Want a ready-made capability for your OpenClaw? Browse [`use-cases/`](use-cases/) — each entry
is a small pointer (what it does, how to install, what keys it needs) to an upstream skill you
can drop in. First entry: [`use-cases/last30days/`](use-cases/last30days/).

## File naming

| Kind      | Pattern                | Example                          |
|-----------|------------------------|----------------------------------|
| Agent     | `<name>.agent.md`      | `code-reviewer.agent.md`         |
| Skill     | `<name>.skill.md`      | `web-search.skill.md`            |
| Workflow  | `<name>.workflow.md`   | `pr-review.workflow.md`          |
| Prompt    | `<name>.prompt.md`     | `safety-preamble.prompt.md`      |
