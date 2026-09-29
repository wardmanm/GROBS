# GROBS — agent instructions

GROBS (Grand Raggidy OBS) is a monorepo of independent tools that make streaming roller derby easier. This file is the shared source of truth for AI coding agents (Claude Code, Codex, Cursor, Copilot, …) and applies to human contributors too.

## Repository map

| Path | What it is | Tech | Instructions |
|---|---|---|---|
| `obs-producer/` | LAN-hosted app for OBS overlays, producer dashboards, OBS control, and read-only CRG scoreboard integration | TypeScript, React, Node | [obs-producer/AGENTS.md](obs-producer/AGENTS.md) |
| `simple-ip-camera-controls/` | Single-file PTZ controls for AXIS (VAPIX) IP cameras, usable as an OBS dock | Plain HTML/JS, no build | [SICC-README.md](simple-ip-camera-controls/SICC-README.md) |

## Repo-wide rules

- **Tools are independent.** A change to one tool never edits another tool's files. There is no shared code between tools.
- **Read the tool's own instructions first.** Before working inside a tool folder, read its `AGENTS.md` (or README if it has none).
- **Keep the root README current.** Adding, renaming, or retiring a tool means updating the table above and [README.md](README.md).

## Git workflow

- Work on a branch; don't commit directly to `main`. Name branches `<type>/<short-topic>`, e.g. `feat/team-builder`, `docs/obs-producer-wiki`.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/) scoped to the tool: `feat(obs-producer): add team import`, `fix(sicc): preset colors`, `docs(obs-producer): ADR for storage`.
- Reference issues in the commit or PR that completes them: `Closes #12`.
- Release tags are `<tool>-v<semver>` (e.g. `obs-producer-v0.2.0`), and only that tool's release workflow creates them. Releases are always deliberate; see the [obs-producer releasing guide](obs-producer/docs/guides/releasing.md).
- Don't push, open PRs, or rewrite published history unless asked.
