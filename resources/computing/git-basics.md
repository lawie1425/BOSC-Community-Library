# Version Control with Git

**Category:** Computing & Technology
**Source:** Git Project / GitHub Docs
**Format:** Tutorial
**Language:** English
**Added:** 2026-05-09
**License:** CC BY 4.0

---

## What Is Version Control?

Version control is a system that records changes to a file or set of files over time, allowing you to recall specific versions later. It is an essential tool for any collaborative project — software or otherwise.

**Git** is the world's most widely used distributed version control system, created by Linus Torvalds in 2005 for managing the Linux kernel source code.

---

## Core Git Concepts

| Concept | Definition |
|---------|-----------|
| **Repository (Repo)** | A directory tracked by Git, containing your project files and full history |
| **Commit** | A snapshot of your changes at a point in time |
| **Branch** | An independent line of development |
| **Merge** | Combining changes from one branch into another |
| **Remote** | A version of your repo hosted on a server (e.g., GitHub) |
| **Clone** | A local copy of a remote repository |
| **Pull Request (PR)** | A request to merge your branch changes into the main branch |

---

## Essential Git Commands

### Setting Up

```bash
# Configure your identity (required for commits)
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Initialize a new repository
git init

# Clone an existing repository
git clone https://github.com/username/repository.git
```

### Daily Workflow

```bash
# Check the status of your working directory
git status

# Stage changes for commit
git add filename.md         # Stage a specific file
git add .                   # Stage all changes

# Commit staged changes
git commit -m "feat: add introduction to OSS resource"

# Push commits to the remote repository
git push origin main

# Pull latest changes from remote
git pull origin main
```

### Branching

```bash
# List all branches
git branch

# Create and switch to a new branch
git checkout -b feat/new-feature

# Switch between branches
git checkout main

# Merge a branch into current branch
git merge feat/new-feature

# Delete a branch after merging
git branch -d feat/new-feature
```

### Inspecting History

```bash
# View commit history
git log --oneline

# See changes in a specific commit
git show <commit-hash>

# Compare differences between branches
git diff main..feat/new-feature
```

---

## The Git Workflow (Feature Branch Model)

```
main ──────────────────────────────────────────►
         │                         ▲
         │ git checkout -b         │ git merge
         ▼                         │
     feature-branch ──────────────►
         (make commits here)
```

1. **Never commit directly to `main`**
2. Create a **feature branch** for each piece of work
3. **Commit early, commit often** with clear messages
4. **Open a Pull Request** for review before merging
5. **Delete the branch** after a successful merge

---

## Writing Good Commit Messages

Follow the **Conventional Commits** format:

```
<type>: <short description>

[optional body]
```

**Types:** `feat`, `fix`, `docs`, `refactor`, `chore`, `test`

| ✅ Good | ❌ Bad |
|--------|--------|
| `feat: add Swahili translation for OSS intro` | `update` |
| `fix: correct broken link in resource index` | `fixed stuff` |
| `docs: update contributing guide with branch naming` | `changes` |

---

## Further Reading

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Learn Git Branching (Interactive)](https://learngitbranching.js.org/)
- [Conventional Commits Specification](https://www.conventionalcommits.org/)

---

*This resource is part of the [BOSC Community Library](../../README.md) | [Back to Computing](README.md) | [Back to Index](../index.md)*
