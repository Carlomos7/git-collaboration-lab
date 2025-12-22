# Git Collaboration Lab

[![Open Issues](https://img.shields.io/github/issues-raw/Carlomos7/git-collaboration-lab?labelColor=303446&style=for-the-badge)](https://github.com/Carlomos7/git-collaboration-lab/issues)
[![Closed Issues](https://img.shields.io/github/issues-closed-raw/Carlomos7/git-collaboration-lab?labelColor=303446&style=for-the-badge)](https://github.com/Carlomos7/git-collaboration-lab/issues?q=is%3Aissue+is%3Aclosed)
[![Repo Size](https://img.shields.io/github/repo-size/Carlomos7/git-collaboration-lab?labelColor=303446&style=for-the-badge)](https://github.com/Carlomos7/git-collaboration-lab)
[![Milestones](https://img.shields.io/github/milestones/all/Carlomos7/git-collaboration-lab?labelColor=303446&style=for-the-badge)](https://github.com/Carlomos7/git-collaboration-lab/milestones)

A hands-on workshop for learning Git workflows, code reviews, and agile project management.

---

## Getting Started

Clone the repository and switch to the development branch before starting any work.

```bash
git clone https://github.com/Carlomos7/git-collaboration-lab.git
cd git-collaboration-lab
git checkout dev
```

All feature work should be done on a branch created from `dev`.

## Quick Links

| Topic | Description |
|-------|-------------|
| [Workflow](docs/workflow.md) | Development process, syncing, and merge conflicts |
| [Branching](docs/branching.md) | Branch strategy and naming conventions |
| [Pull Requests](docs/pull-requests.md) | PRs, code reviews, and commit hygiene |
| [Issues & Projects](docs/issues-and-projects.md) | Issue templates and Kanban board setup |
| [Agile Basics](docs/agile-basics.md) | Milestones, user stories, and iterations |
| [Team Kanban Board](https://github.com/users/Carlomos7/projects/10/views/1) | Track issues across Backlog, In Progress, In Review, and Done |

---

## Exercise 1: Add Yourself to the Roster

Complete this task to practice the core workflow:

1. **Create an issue** using the User Story template
2. **Create a feature branch** from `dev`:

   ```bash
   git checkout dev
   git pull origin dev
   git checkout -b feature/add-yourname
   ```

3. **Add your name** to the Team Roster below
4. **Commit and push**:

   ```bash
   git add README.md
   git commit -m "feat: add [Your Name] to team roster"
   git push -u origin feature/add-yourname
   ```

5. **Open a Pull Request** targeting `dev`
6. **Request a review** from a teammate
7. **Review someone else's PR** — practice giving constructive feedback

---

## Team Roster

| Name | Role | GitHub |
|------|------|--------|
| Carlos Segarra | Developer | [Carlomos7](https://github.com/Carlomos7) |
|Hayden Ferguson |Developer |[Hayden-Ferguson](https://github.com/Hayden-Ferguson) |

---

## Exercise 2: Add Your Print Statement

Practice the workflow with a code file:

- **Create an issue** using the User Story template
- **Create a feature branch** from `dev`:

```bash
   git checkout dev
   git pull origin dev
   git checkout -b feature/hello-yourname
```

- **Add a print statement** to `hello.py`:

```python
   print("Hello, I'm [Your Name]!")
```

- **Commit and push**:

```bash
   git add hello.py
   git commit -m "feat: add [Your Name] print statement"
   git push -u origin feature/hello-yourname
```

- **Open a Pull Request** targeting `dev`
- **Request a review** from a teammate
