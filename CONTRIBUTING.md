# Contributing to BOSC Community Library

Thank you for your interest in contributing to the **BOSC Community Library**! 🎉

This document provides comprehensive technical instructions for external contributors. Please read it carefully before submitting your first contribution.

---

## 📋 Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [How to Contribute](#how-to-contribute)
3. [Development Workflow](#development-workflow)
4. [Types of Contributions](#types-of-contributions)
5. [Commit Message Standards](#commit-message-standards)
6. [Pull Request Process](#pull-request-process)
7. [Issue Reporting Guidelines](#issue-reporting-guidelines)
8. [Style Guide](#style-guide)
9. [Community & Communication](#community--communication)

---

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing. All interactions must be respectful, constructive, and inclusive.

---

## How to Contribute

### Prerequisites

Before you begin, ensure you have the following installed:
- **Git** (v2.30 or higher) — [Download Git](https://git-scm.com/)
- **A GitHub account** — [Create one here](https://github.com/join)
- **A text editor** — We recommend [VS Code](https://code.visualstudio.com/)
- **Markdown preview** — Use VS Code's built-in preview or [Typora](https://typora.io/)

### First-Time Setup

```bash
# 1. Fork the repository on GitHub
# (Click the "Fork" button at the top-right of the repo page)

# 2. Clone YOUR fork locally
git clone https://github.com/YOUR-USERNAME/BOSC-Community-Library.git
cd BOSC-Community-Library

# 3. Add the upstream remote (the original repo)
git remote add upstream https://github.com/lawie1425/BOSC-Community-Library.git

# 4. Verify your remotes
git remote -v
# Expected output:
# origin    https://github.com/YOUR-USERNAME/BOSC-Community-Library.git (fetch)
# origin    https://github.com/YOUR-USERNAME/BOSC-Community-Library.git (push)
# upstream  https://github.com/lawie1425/BOSC-Community-Library.git (fetch)
# upstream  https://github.com/lawie1425/BOSC-Community-Library.git (push)
```

---

## Development Workflow

We follow a **feature branch workflow**. Never commit directly to `main`.

### Step-by-Step Process

```bash
# Step 1: Sync your fork with the latest upstream changes
git checkout main
git fetch upstream
git merge upstream/main
git push origin main

# Step 2: Create a feature branch for your contribution
# Branch naming convention: type/short-description
git checkout -b feat/localization-swahili
# or
git checkout -b fix/broken-resource-link
# or
git checkout -b refactor/reorganize-computing-section

# Step 3: Make your changes
# (edit files, add resources, fix issues)

# Step 4: Stage and commit your changes
git add .
git commit -m "feat: add Swahili localization for OSS introduction resource"

# Step 5: Push your branch to YOUR fork
git push origin feat/localization-swahili

# Step 6: Open a Pull Request on GitHub
# Go to https://github.com/lawie1425/BOSC-Community-Library
# Click "Compare & pull request"
```

### Branch Naming Conventions

| Prefix | Use Case | Example |
|--------|----------|---------|
| `feat/` | New feature or resource addition | `feat/french-localization` |
| `fix/` | Bug or broken link fix | `fix/broken-index-link` |
| `refactor/` | Code/structure reorganization | `refactor/flatten-resources` |
| `docs/` | Documentation updates | `docs/update-contributing-guide` |
| `chore/` | Maintenance tasks | `chore/update-gitignore` |

---

## Types of Contributions

### 📚 Adding Resources
- Place new resources in the appropriate subfolder under `resources/`
- Always update `resources/index.md` with the new entry
- Include: Title, Source, Format, Language, and Link
- Ensure the resource is **freely accessible** (no paywalls)
- Verify all links are working before submitting

### 🐛 Fixing Bugs
- Broken links, incorrect metadata, or logic errors in index files
- Open an issue first using the **Bug Report** template
- Reference the issue number in your PR (e.g., `Fixes #12`)

### 🌐 Localization
- Add translations to the `resources/localization/` directory
- Name files using ISO 639-1 language codes (e.g., `oss-intro-sw.md` for Swahili)
- Update the localization tracker in `resources/index.md`

### ✨ Feature Enhancements
- Discuss the feature in an issue before building it
- Use the **Feature Request** template
- Large features should be discussed and approved before implementation begins

### 🔧 Refactoring
- Structural changes require an issue and maintainer approval before starting
- Preserve all existing content — refactoring should not delete resources

---

## Commit Message Standards

We follow the **Conventional Commits** specification. This ensures a clean, readable git history.

### Format

```
<type>(<scope>): <short description>

[optional body — explain WHY, not WHAT]

[optional footer — e.g., Fixes #12]
```

### Types

| Type | Meaning |
|------|---------|
| `feat` | A new feature or resource |
| `fix` | A bug fix |
| `docs` | Documentation-only changes |
| `refactor` | Code/structure change that is not a fix or feature |
| `chore` | Maintenance (e.g., updating .gitignore) |
| `test` | Adding or updating tests |

### Examples

```bash
# Good
git commit -m "feat(localization): add Swahili translation of OSS introduction"
git commit -m "fix(index): correct broken link to Linux CLI resource"
git commit -m "docs(contributing): add branch naming conventions section"
git commit -m "refactor(resources): reorganize computing section by difficulty level"

# Bad — too vague
git commit -m "update"
git commit -m "fix stuff"
git commit -m "changes"
```

---

## Pull Request Process

1. **One PR per issue** — keep changes focused and reviewable
2. **Fill out the PR template** completely — incomplete PRs will be closed
3. **Reference issues** — use `Fixes #<issue-number>` or `Closes #<issue-number>` in your PR description
4. **Ensure all links work** before submitting
5. **Be responsive** — respond to review comments within 3 business days
6. **Squash commits** if requested by a maintainer before merging

PRs are reviewed by maintainers within **5 business days**. Please be patient.

---

## Issue Reporting Guidelines

Use the appropriate issue template:
- 🐛 **Bug Report** — for broken links, incorrect data, or logic errors
- ✨ **Feature Request** — for new resources, features, or enhancements

**Before opening an issue:**
- Search existing issues to avoid duplicates
- Be as specific as possible in your description
- Include steps to reproduce (for bugs)

---

## Style Guide

### Markdown Standards
- Use ATX-style headings (`#` not underlines)
- Use fenced code blocks with language specifiers (` ```bash `)
- Use reference links for frequently repeated URLs
- Keep lines under 120 characters where possible
- Always include a blank line before and after headings, lists, and code blocks

### Resource Entry Format (in `index.md`)

```markdown
| # | Title | Source | Format | Language | Link |
|---|-------|--------|--------|----------|------|
| N | Full Resource Title | Organization Name | PDF/Guide/Tutorial | English | [filename.md](path/filename.md) |
```

---

## Community & Communication

| Channel | Purpose |
|---------|---------|
| [GitHub Issues](https://github.com/lawie1425/BOSC-Community-Library/issues) | Bug reports, feature requests |
| [GitHub Discussions](https://github.com/lawie1425/BOSC-Community-Library/discussions) | General questions, ideas |
| Pull Request comments | Code review and technical feedback |

---

## Recognition

All contributors are recognized in the project's commit history and will be credited in release notes. Consistent, high-quality contributions may lead to maintainer status.

---

*Thank you for helping make knowledge freely accessible to everyone. Every contribution, no matter how small, makes a difference. 🌍*

*BOSC Community Library — Building Open Source Community*
