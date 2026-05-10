# Linux Command Line Fundamentals

**Category:** Computing & Technology
**Source:** Community-authored BOSC guide
**Format:** Guide
**Language:** English
**Added:** 2026-05-10
**License:** Apache 2.0

---

## What Is the Command Line?

The command line is a text-based way to interact with a computer. Instead of clicking through menus, users type commands into a terminal to navigate folders, inspect files, install tools, and automate repeated tasks.

For open-source contributors, the command line is especially useful because many development tools are designed to run from a terminal.

---

## Essential Concepts

| Concept | Meaning |
|---------|---------|
| **Terminal** | The application used to type and run commands |
| **Shell** | The program that reads and executes commands |
| **Directory** | A folder in the filesystem |
| **Path** | The location of a file or directory |
| **Home directory** | The user's main personal directory |
| **Current directory** | The directory where commands are currently running |

---

## Basic Commands

```bash
# Show the current directory
pwd

# List files
ls

# Change directory
cd resources

# Create a directory
mkdir notes

# Copy a file
cp source.md copy.md

# Move or rename a file
mv old-name.md new-name.md

# Remove a file
rm old-file.md
```

Use removal commands carefully. Deleted files may not be recoverable unless they are tracked in version control or backed up elsewhere.

---

## Reading Files

```bash
# Show a short file
cat README.md

# Page through a longer file
less README.md

# Show the first lines of a file
head README.md

# Search text in files
grep "license" README.md
```

---

## Good Habits

1. Run `pwd` before changing or deleting files.
2. Use `ls` to confirm what is in the current directory.
3. Prefer copying important files before experimenting.
4. Read command help with `command --help` when unsure.
5. Keep project work in a version-controlled repository.

---

## Further Reading

- [Linux Journey](https://linuxjourney.com/)
- [The Linux Command Line](https://linuxcommand.org/tlcl.php)
- [Ubuntu Command Line for Beginners](https://ubuntu.com/tutorials/command-line-for-beginners)

---

*This resource is part of the [BOSC Community Library](../../README.md) | [Back to Computing](README.md) | [Back to Index](../index.md)*
