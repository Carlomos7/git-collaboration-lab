# Agile Basics

A lightweight introduction to agile concepts.

---

## Key Terms

| Term | Definition |
|------|------------|
| **User Story** | A small piece of work described from the user's perspective |
| **Sprint/Iteration** | A fixed time period (1-2 weeks) to complete work |
| **Milestone** | A goal or release made up of related issues |
| **Backlog** | The list of work items not yet started |

---

## User Stories

User stories describe *what* to build and *why* it matters.

**Format:**

```md
As a [type of user]
I want [some feature]
So that [benefit/reason]
```

**Example:**

```md
As a new team member
I want clear documentation on our Git workflow
So that I can contribute without asking basic questions
```

**Good stories are:**

- Small enough to complete in a few days
- Testable — you know when it's done
- Independent — not blocked by other work

---

## Milestones

Milestones group related issues into a release or goal.

**How to use them:**

1. Create a milestone: **Issues → Milestones → New milestone**
2. Set a due date (optional)
3. Assign issues to the milestone
4. Track progress as issues close

**Example milestones:**

- `v1.0 - Initial Release`
- `Sprint 1 - Core Features`
- `Onboarding Improvements`

---

## Simple Flow

Keep it lightweight:

1. **User stories** are the primary work items
2. **Tasks** can be added as checkboxes within a story if needed
3. **Milestones** group stories into iterations
4. **Kanban board** shows current status

No need for story points, velocity tracking, or ceremonies beyond a quick sync.

---

## Tips

- Keep stories small — if it takes more than a few days, break it down
- Write acceptance criteria — how do you know it's done?
- Finish work in progress before starting new work
- Review and update the board regularly

---

## Example User Story Issue

```md
Title: US-01: Add team member to roster

## Description

**As a** new team member  
**I want** to add my name and GitHub profile to the README  
**So that** the team knows who's contributing

## Acceptance Criteria

- [ ] Name appears in Team Roster table
- [ ] Role is filled in
- [ ] GitHub profile is linked correctly

## Tasks

- [ ] Create feature branch from `dev`
- [ ] Edit README.md with name, role, and GitHub link
- [ ] Commit with `feat:` prefix
- [ ] Push branch and open PR
- [ ] Request review from teammate
```
