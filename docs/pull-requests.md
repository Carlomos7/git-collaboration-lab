# Pull Requests & Code Reviews

Collaborating through pull requests and maintaining a clean project history.

---

## Commit Hygiene

Good commits make history readable and debugging easier.

### Make Small, Focused Commits

- Each commit should do **one thing**
- If you can't describe it in one line, it's too big
- Easier to review, revert, and understand

### Commit Message Format

```md
type: short description
```

| Prefix | Use For | Example |
|--------|---------|---------|
| `feat:` | New feature | `feat: add login form validation` |
| `fix:` | Bug fix | `fix: resolve null pointer in auth` |
| `docs:` | Documentation | `docs: update API usage examples` |
| `refactor:` | Code restructure | `refactor: extract validation helpers` |
| `style:` | Formatting only | `style: fix indentation in config` |
| `test:` | Adding tests | `test: add unit tests for login` |
| `chore:` | Maintenance | `chore: update dependencies` |

### Why This Matters

- `git log` becomes useful documentation
- Easy to find when a change was introduced
- Simple to revert specific changes
- Makes code review faster

---

## Creating a Pull Request

### Before You Open

- [ ] Pull latest `dev` and resolve any conflicts locally
- [ ] Self-review your changes
- [ ] Verify your code works

### Opening the PR

1. Push your branch to GitHub
2. Click **Compare & pull request**
3. Set **base** to `dev` (not `main`)
4. Fill out the PR template
5. Request a reviewer

### Document Your Changes

Good PRs make the reviewer's job easy. Include:

- **Clear description** — what changed and why
- **Screenshots** — for any UI changes (before/after)
- **Code snippets** — for complex logic, show example input/output
- **Context** — link related issues, mention affected areas

A reviewer shouldn't have to read every line to understand the change.

### Linking Issues (Optional)

If your PR resolves an issue, you can link it:

```md
Closes #42
```

This auto-closes the issue when the PR merges. Use this when it makes sense, but it's not required for every PR.

---

## Merging Safely

### Before Merging

1. Ensure all review comments are addressed
2. Verify CI checks pass (if configured)
3. Pull latest `dev` to check for conflicts:

```bash
git checkout dev
git pull origin dev
git checkout feature/your-branch
git merge dev
# Resolve conflicts if any, then push
git push origin feature/your-branch
```

### Merge Options

- **Merge commit** — preserves full history (default)
- **Squash and merge** — combines all commits into one (cleaner history)
- **Rebase and merge** — linear history, no merge commits

For this workshop, use the default **merge commit**.

### After Merging

- Delete your feature branch (GitHub offers this option)
- Pull latest `dev` locally:

```bash
git checkout dev
git pull origin dev
```

---

## Code Review Guidelines

### As a Reviewer

**Do:**

- Be specific and constructive
- Explain *why*, not just *what*
- Ask questions instead of demanding changes
- Acknowledge good work
- Approve when it's ready (minor suggestions are okay)

**Don't:**

- Be dismissive or condescending
- Block for personal style preferences
- Leave vague comments like "fix this"

### Example Feedback

| Instead of... | Try... |
|---------------|--------|
| "This is wrong" | "This might cause X because Y. Consider Z?" |
| "Fix this" | "Could you add error handling for the null case?" |
| "I don't like this" | "Have you considered X? It might be clearer because..." |

### As the Author

- Respond to all comments (even just "Done" or "Good point")
- Ask for clarification if feedback is unclear
- Don't take feedback personally — it's about the code
- Re-request review after making changes
