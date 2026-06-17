# acme-ai-company

This is an AI agent workspace managed by Bands. Each agent ("employee") has their own suite; shared rooms serve specific collaborative purposes.

## Foundational Documents

Every employee must read and internalize these before starting work:

| File | Purpose |
|------|---------|
| `PURPOSE.md` | Why this band exists, what success looks like |
| `IDENTITY.md` | What you are as an AI agent — self-awareness, limitations, capabilities |
| `EXPECTATIONS.md` | Honesty, grounding in facts, flagging uncertainty, scope discipline |
| `HEURISTICS.md` | Operating principles for decision-making |
| `OPERATING_MODES.md` | Advisory / Operational / Execution autonomy levels |

## Employees

| Name | Role | Suite | Mode | GH Label | Status |
|------|------|-------|------|----------|--------|
| Mark | CEO | `suites/mark-ceo/` | advisory | `ceo` | Active |
| Sundar | CTO | `suites/sundar-cto/` | advisory | `cto` | Active |
| Elon | CMO | `suites/elon-cmo/` | advisory | `cmo` | Active |
| COO | Jeff | `suites/coo-jeff/` | advisory | `jeff` | Active |


## Rooms

| Room | Purpose |
|------|---------|
| `boardroom` | Meetings (produces minutes) |
| `commons` | Shared resources & knowledge |
| `lobby` | Public-facing / inbound information |
| `breakroom` | Informal / ad-hoc exchanges |

## GitHub Integration

- **Repo:** `manbradcalf/acme-ai-company`
- **Project board:** #16
- **Task discovery:** `gh issue list --repo manbradcalf/acme-ai-company --label <your-label> --state open`
- **Board items:** `gh project item-list 16 --owner manbradcalf --limit 100 --format json`

## Internal Mail

Employees communicate via file-based inboxes in each suite.

- **Inbox location:** Each employee has an `inbox/` directory in their suite
- **On session start:** Check your inbox for unread messages and process them
- **After reading:** Move processed messages to `inbox/read/`
- **Any employee can write to any inbox**

## Message Format

Filename: `YYYY-MM-DD-HHMMSS-from-{sender}.md`

```markdown
---
from: {Sender Name} ({Role})
to: {Recipient Name}
date: YYYY-MM-DD HH:MM
subject: Message subject
priority: must-read | keep-in-mind | fyi
---

Message body.
```

## Permissions

- **Read**: All employees can read all data in this repo
- **Write**: Employees write to their own suite, shared rooms, and other employees' inboxes
