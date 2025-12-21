# Workflow

The development process from start to finish.

---

## Core Concepts

**Git** is the source of truth — it tracks every change to the codebase.

**GitHub** is the collaboration layer — it hosts the remote repo and provides tools for code review, issues, and project management.

**Local vs Remote:**

- Your **local repo** is your working copy on your machine
- The **remote repo** (origin) is the shared copy on GitHub
- Keep them in sync with `git pull` and `git push`

---

## The Golden Rules

1. **Never commit directly to `main` or `dev`**
2. **Always pull before you branch**
3. **One branch = one task** — keep it focused
4. **Branches are short-lived** — merge frequently, don't let them grow stale
5. **Pull often** — stay in sync with the team

---

## Step-by-Step

### 1. Sync Before Starting

Always start with the latest code:

```bash
git checkout dev
git pull origin dev
```

### 2. Create a Feature Branch

One branch per issue or task — keep it focused:

```bash
git checkout -b feature/short-description
```

### 3. Make Small, Clear Commits

Commit often with meaningful messages:

```bash
git add .
git commit -m "feat: add user login form"
```

### 4. Stay in Sync While Working

If others are merging to `dev`, pull periodically:

```bash
git checkout dev
git pull origin dev
git checkout feature/your-branch
git merge dev
```

### 5. Push Your Branch

```bash
git push -u origin feature/your-branch
```

### 6. Open a Pull Request

- Go to GitHub → **Compare & pull request**
- Target branch: `dev`
- Fill out the PR template
- Request a reviewer

### 7. After Your PR is Merged

Update your local repo and clean up:

```bash
git checkout dev
git pull origin dev
git branch -d feature/your-branch
```

---

## Merging Dev to Main

When `dev` is stable and tested, the team lead merges to `main`:

```bash
git checkout main
git pull origin main
git merge dev
git push origin main
```

---

## Handling Merge Conflicts

Conflicts happen when two people edit the same lines. This is normal.

### Why Conflicts Occur

- Two branches modify the same file/lines
- One branch is merged first
- The second branch now conflicts with the updated code

### How to Avoid Conflicts

- **Pull frequently** — sync with `dev` often
- **Keep branches short-lived** — less time for conflicts to build up
- **Communicate** — let the team know what files you're working on
- **Merge one PR at a time** — first person merges, others pull and resolve

### How to Resolve Conflicts

When Git reports a conflict:

- Pull latest dev

```bash
git checkout dev
git pull origin dev
```

- Merge dev into your branch

```bash
git checkout feature/your-branch
git merge dev
```

- Git marks conflicts in the file like this:

```md
<<<<<< HEAD
your changes
=======
their changes
>>>>>> dev
```

- Edit the file to keep what you need, remove the markers
- Stage and commit the resolution

```bash
git add .
git commit -m "fix: resolve merge conflict in login.py"
```

- Push your branch

```bash
git push origin feature/your-branch
```

---

## Quick Reference

| Action | Command |
|--------|---------|
| Sync with remote | `git pull origin dev` |
| Create branch | `git checkout -b feature/name` |
| Stage changes | `git add .` |
| Commit | `git commit -m "type: message"` |
| Push branch | `git push -u origin feature/name` |
| Delete local branch | `git branch -d feature/name` |
