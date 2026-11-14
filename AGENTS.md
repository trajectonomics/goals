# AGENTS.md

Instructions for AI coding agents in `trajectonomics/goals`.

## Rules

- `GOALS.md` is the organisation's goals and is read-only for agents. Read it before proposing a new direction; only the owner edits it, and an agent never does.

## Agent skills

The skills an agent uses in this repository live in `.agents/skills/`, the canonical copy, pinned in `skills-lock.json`. `.claude/skills/`, `.grok/skills/` and `.vibe/skills/` each hold one symlink per skill into it (`<name> -> ../../.agents/skills/<name>`); `.vibe/skills/` is the directory Mistral Vibe discovers project skills in, so a skill missing there is invisible to a Vibe session even when it is installed (the pattern from trajectonomics/factory#80). Never edit the skills or those symlinks by hand: add, update and check them with the Vercel `skills` CLI (`npx skills add`, `npx skills update`, `npx skills check`), which writes the lock file.
