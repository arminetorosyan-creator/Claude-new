---
name: prd-writer
description: Turn rough notes, a feature idea, a Slack thread, or a one-line pitch into a structured Product Requirements Document (PRD). Use this skill whenever the user asks to write, draft, structure, or clean up a PRD, product requirements doc, product spec, one-pager, or feature brief — even if they don't say the word "PRD" explicitly, e.g. "can you turn this into a proper doc for engineering" or "write up the requirements for X." Also use it when a Product Owner or PM shares messy notes about a feature and asks for something they can share with a team.
---

# PRD Writer

Product Owners rarely start with clean input — usually it's a voice memo transcript, a half-formed Slack message, a bullet list from a meeting, or just "we should build X because Y." Your job is to turn that into a PRD that an engineering team, designer, and stakeholder could all read and understand what's being built and why.

## Default template

Unless the user has told you their team uses a different format, structure the PRD with these sections, in this order:

```markdown
# [Feature/Product Name] — PRD

## Problem / Background
What problem exists today? Who has it, and how do we know? Include any
data, user feedback, or context the input mentions. If the input doesn't
explain *why* this matters, say so as an open question rather than
inventing a justification.

## Goals
What does success look like? 2-5 bullet points, outcome-oriented (what
changes for the user or business), not implementation-oriented.

## Non-Goals
What is explicitly out of scope for this version? This is often more
useful than the goals section for preventing scope creep — call out
adjacent things people might assume are included but aren't.

## User Stories
"As a [user type], I want to [action], so that [benefit]." Cover the
main flows implied by the input. Keep each story testable.

## Requirements
Functional requirements, grouped logically (not just a flat list if
there's a natural grouping like "Onboarding," "Settings," "Notifications").
Mark anything inferred rather than stated as (assumed).

## Success Metrics
How will we know this worked? Prefer specific, measurable signals over
vague ones ("increase activation by X%" beats "improve activation").
If the input gives no metrics, propose 1-2 reasonable candidates and
flag them as suggestions.

## Open Questions
Anything unresolved: decisions the team still needs to make, information
you didn't have, or risks worth flagging. This section is a feature, not
a gap — a PRD that pretends everything is known is less useful than one
that's honest about what isn't.
```

## How to work from messy input

The core skill here is inference without fabrication:

- If the input clearly implies something (e.g., notes mention "mobile app users complain about X" — that's your Problem/Background), use it directly.
- If something is missing but reasonably inferable from context (e.g., no explicit goal stated, but the notes are clearly about reducing support tickets), write it in and note it's inferred only if there's real ambiguity.
- If something is genuinely unknown (success metrics, target launch date, which platforms), do not invent specifics — put a clearly-marked placeholder or question in Open Questions instead. A PRD with fabricated metrics is worse than one that asks the right question.
- If the input is too thin to fill a section meaningfully (e.g., zero information about scope), say so briefly under that heading rather than padding it with generic filler.

## When the team has its own template

If the user mentions their team has a specific PRD format (sections, tone, required fields like "Rollout Plan" or "Dependencies"), use their structure instead of the default above. Ask them to paste an example or describe the sections if they mention a custom format but haven't shared it yet.

## Output

Write the PRD as clean Markdown so it can be pasted into Confluence, Notion, Google Docs, or a `.md` file. Use `##` for section headers as shown above, and keep language direct and skimmable — engineers and stakeholders are scanning this, not reading it start to finish. Avoid marketing language ("revolutionary," "seamless") in favor of concrete, specific statements.

After producing the PRD, briefly ask the user what's missing or wrong rather than assuming it's final — the first draft is a starting point for their review, not a finished spec.
