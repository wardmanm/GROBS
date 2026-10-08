@AGENTS.md

## Claude Code notes

Shared rules live in `AGENTS.md` (imported above) so every agent reads the same instructions. Only Claude-specific notes go in this file.

### Maintaining agent instructions

How the instruction files are layered, so they stay small and don't contradict each other:

- **`AGENTS.md`** is the source of truth at each level (repo root, each tool). **`CLAUDE.md`** starts with `@AGENTS.md` and adds only Claude-specific notes. Never copy rules between the two; import them.
- **Nested files add to the root; they don't replace it.** Write a tool's own CLAUDE.md as additions to this one.
- **Keep each `CLAUDE.md`/`AGENTS.md` under ~200 lines.** Anything longer belongs somewhere else:
  - Multi-step procedures go in a skill: `.claude/skills/<name>/SKILL.md`, at the repo root.
  - Rules that only matter for certain files go in `.claude/rules/<topic>.md`, with `paths:` globs in the frontmatter so they load only when matching files are read.
  - Reference material stays in the tool's wiki and gets linked, never `@`-imported. Imports load into every session.
- **`CLAUDE.local.md`** is for personal notes and is gitignored. The `@AGENTS.md` import keeps shared rules loading even if one exists.
- Run `/doctor prompt-audit` to catch stale or conflicting instructions after large edits.
