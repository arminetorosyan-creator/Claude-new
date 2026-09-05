# Claude-new

No application code has been added to this repository yet. It currently
holds Claude Code configuration only — skills for a Product Owner's
workflow.

## Status

- No build system, language, or framework has been chosen yet.
- No tests or lint commands exist yet.

## What's here

- `.claude/settings.json` — baseline permissions (safe read-only tools and
  git commands allowed without prompting).
- `.claude/skills/prd-writer/` — turns rough notes/ideas into a structured PRD.
- `.claude/skills/user-story-writer/` — turns a feature idea into Jira-style
  tickets with acceptance criteria.
- `.claude/skills/meeting-notes-summarizer/` — turns a transcript or notes
  into a short summary paragraph.

## For Claude

When application code is added to this repo, update this file with:
- The project's purpose and tech stack
- Build/test/lint commands
- Any architectural conventions specific to this repo

Until then, treat this as a blank slate for application code: confirm the
intended stack with the user before scaffolding a new project structure.
The PO skills above are unrelated to that and should stay as-is.
