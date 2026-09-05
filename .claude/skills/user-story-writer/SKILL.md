---
name: user-story-writer
description: Turn a feature idea, PRD excerpt, or rough notes into Jira-style user story tickets with acceptance criteria. Use this skill whenever the user asks to write, draft, or break down user stories, tickets, backlog items, or acceptance criteria — even if they just describe a feature and ask "can you turn this into tickets for the team" or "break this down into stories." Also use it when a Product Owner shares a feature description and wants it split into engineering-ready work items.
---

# User Story Writer

Product Owners often go from a feature idea straight to "I need tickets for the sprint." Your job is to produce tickets an engineer could pick up and know exactly what to build and how to tell it's done — without you inventing scope the PO never asked for.

## Deciding: one ticket or several

Look at what's being asked:

- **One clear, small ask** ("let users reset their password from settings") → produce a single ticket.
- **A feature with multiple distinct pieces of work** (a PRD excerpt, a multi-step flow, something spanning frontend/backend/notifications) → split into multiple tickets, each independently shippable or testable where possible. Don't split for the sake of it — a ticket that can't stand alone as a unit of work isn't a good split.

When splitting, briefly list the tickets you're proposing first (a one-line title for each) so the user can sanity-check the breakdown before you write out full detail for each one. If the split is obvious and small (2-3 tickets), it's fine to just write them all out directly.

## Ticket format

Use this structure for every ticket:

```markdown
### [Ticket Title — short, action-oriented, e.g. "Add saved shipping addresses to checkout"]

**Story:**
As a [user type], I want to [action], so that [benefit].

**Acceptance Criteria:**
- [ ] Specific, testable condition
- [ ] Specific, testable condition
- [ ] Specific, testable condition (include edge cases: empty states, errors, permissions — whatever's relevant)

**Priority:** [High / Medium / Low — infer from context if stated, otherwise omit rather than guess]
**Size:** [rough T-shirt size (S/M/L) only if you have enough detail to estimate honestly — otherwise omit]
```

Leave out Priority or Size entirely rather than filling them with a guess dressed up as an estimate — an omitted field is honest; a made-up "Medium" or "M" is not.

## Writing good acceptance criteria

This is the part that actually makes a ticket useful, more than the story format. Each criterion should be something a tester could check off as true or false — not vague ("works well on mobile") but specific ("form fields stack vertically below 480px width" or "shows an inline error if the field is empty on submit"). Think through:

- The happy path
- At least one edge case (empty input, no results, permission denied, network failure — whatever applies)
- Anything explicitly mentioned as a constraint in the input (a specific platform, a specific user role, a performance requirement)

If the input doesn't give you enough to write a real acceptance criterion for something important (e.g., no mention of what happens on error), either infer a sensible default and note it's assumed, or add a criterion phrased as a question for the PO to resolve — don't silently skip it and don't invent overly specific behavior that wasn't implied.

## Where the input is thin

If given only a one-line feature name with no other context ("ticket for dark mode"), do your best with a minimal but honest ticket, and ask the user directly for the specifics you're missing (which screens, any existing design, is this a toggle or system-preference-based) rather than padding the ticket with invented detail.

## Output

Write tickets as Markdown so they can be pasted directly into Jira, Linear, or GitHub Issues (all render this reasonably). If multiple tickets are produced, separate them clearly with `---` between each. After producing the ticket(s), ask if the split, sizing, or acceptance criteria need adjusting — this is a first pass for the PO to refine, not a final answer.
