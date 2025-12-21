# Issues & Projects

How to track work using GitHub Issues and Project boards.

---

## Issue Templates

Templates are used to keep issues consistent:

- **User Story** — Work items describing what to build
- **Bug Report** — Defects and unexpected behavior

When creating an issue, select the appropriate template and fill out all sections.

---

## Kanban Board

The project board has four columns:

| Column | What Goes Here |
|--------|----------------|
| **Backlog** | Ready to be picked up |
| **In Progress** | Actively being worked on |
| **In Review** | PR opened, awaiting review |
| **Done** | Merged and complete |

### Moving Issues

1. **Start work** → Backlog to In Progress
2. **Open PR** → In Progress to In Review
3. **PR merged** → In Review to Done

---

## Setting Up the Board

1. Go to repo → **Projects** tab → **New project**
2. Choose **Board** template
3. Rename columns: Backlog, In Progress, In Review, Done
4. Add existing issues by clicking **+ Add item**

### Automation (Optional)

GitHub can auto-move issues:

- Issue opened → Backlog
- PR opened → In Review  
- PR merged → Done

Set this up in **Project Settings → Workflows**.

---

## Linking Issues to PRs

In Github, you can easily link your pull request to the issue by selecting it from the dropdown.

(OPTIONALLY) In your PR description, write:

```md
Closes #42
```

*Note:* This automatically closes the issue when the PR merges.

---

## Labels

- **Labels quickly describe the type of work**
- They help the team understand *what kind of issue this is* at a glance
- Keep labels simple to avoid process overhead

---

### Examples

| Label         | Purpose                                         | Example                                            |
| ------------- | ----------------------------------------------- | -------------------------------------------------- |
| `bug`         | Something is broken or behaving incorrectly     | Typo, broken link, incorrect instructions          |
| `enhancement` | An improvement or addition to existing behavior | Improve README wording, clarify docs, add examples |
