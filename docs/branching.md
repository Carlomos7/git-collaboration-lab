# Branching Strategy

How to organize branches to keep the codebase stable and history readable.

---

## Branch Structure

```mint
main ← production-ready, protected
  └── dev ← integration branch, protected
        ├── feature/add-login
        ├── feature/update-readme
        └── bugfix/fix-typo
```

| Branch | Purpose | Merges Into |
|--------|---------|-------------|
| `main` | Production-ready code | — |
| `dev` | Integration branch | `main` |
| `feature/*` | New work | `dev` |
| `bugfix/*` | Bug fixes | `dev` |

---

## Key Principles

### One Branch = One Task

Each branch should represent a single, focused piece of work:

- One issue, one branch
- Don't mix unrelated changes
- Makes code review easier
- Keeps history clean

**Good:** `feature/add-user-auth` contains only auth-related changes

**Bad:** `feature/various-updates` with auth, styling, and bug fixes mixed together

### Branches Are Short-Lived

Merge early and often:

- Aim to merge within a few days
- Long-lived branches accumulate conflicts
- Smaller PRs are easier to review
- Incremental integration reduces risk

### Feature Isolation

Your branch is your sandbox:

- Experiment without affecting others
- Break things safely
- Only tested code gets merged to `dev`
- Only stable code gets merged to `main`

---

## Rules

1. **Never commit directly to `main` or `dev`**
2. **Always branch from `dev`**, not `main`
3. **Pull latest `dev` before creating a branch**
4. **Delete branches after merging**

---

## Naming Conventions

Format: `type/short-description`

| Prefix | Use For | Example |
|--------|---------|---------|
| `feature/` | New functionality | `feature/user-auth` |
| `fix/` | Fixing defects | `fix/login-redirect` |
| `docs/` | Documentation | `docs/update-readme` |
| `refactor/` | Code restructure | `refactor/extract-utils` |

**Tips:**

- Use lowercase and hyphens
- Keep it short but descriptive
- *Optionally* include issue number: `feature/42-add-search`

---

## Common Commands

- Start new work (always sync first!):

```bash
git checkout dev
git pull origin dev
git checkout -b feature/your-branch
```

- Stay up to date while working:

```bash
git checkout dev
git pull origin dev
git checkout feature/your-branch
git merge dev
```

- After your PR is merged:

```bash
git checkout dev
git pull origin dev
git branch -d feature/your-branch
```
