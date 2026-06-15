# Conventions

## Frontmatter (required on every agent)

| Field         | Required | Notes                                            |
|---------------|----------|--------------------------------------------------|
| `name`        | yes      | kebab-case, unique, matches the filename         |
| `description` | yes      | one line; used for discovery/routing             |
| `role`        | yes      | `orchestrator` \| `gateway` \| `worker`          |
| `version`     | yes      | semver                                           |
| `model`       | no       | default model id for this agent                  |
| `tools`       | no       | allowed tools (`*` = all)                        |
| `skills`      | no       | skills to preload                                |
| `owner`       | no       | maintainer                                       |
| `status`      | yes      | `draft` \| `active` \| `deprecated`              |

## Rules

- **One agent per file.** Filename = `<name>.agent.md`, and `name` in
  frontmatter must equal the filename stem.
- **Kebab-case** for all names and filenames.
- **Link related agents** in prose with `[[other-agent-name]]`.
- **Keep shared text in `shared/`** and reference it rather than copy-pasting.
- **Register every agent** in `registry/agents.md` so it is discoverable.
- **Bump `version`** on any behavioral change; set `status: deprecated`
  instead of deleting when retiring an agent.

## Roles

- **orchestrator** — decides which agents/workflows run; delegates, never does
  leaf work itself.
- **gateway** — the OpenClaw Gateway's public entry points; validate and route
  incoming requests.
- **worker** — narrow, task-focused agents that do the real work.
