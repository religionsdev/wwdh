# Chapter 8: Git

## Introduction

Git is the world's most widely used version control system. It allows developers to track changes to their work, recover previous versions, collaborate with others, and maintain a complete history of every project.

Although Git was originally designed for large software teams, it is equally valuable for individual developers. Even when working alone, Git provides a reliable safety net that protects your work and makes experimentation much less risky.

This chapter introduces Git, explains why it is essential, and walks through its installation and initial configuration.

---

## What Is Version Control?

Version control is the process of recording changes to files over time.

Instead of saving files such as:

```text
chapter1-final.md
chapter1-final-final.md
chapter1-final-final-revised.md
```

Git maintains a complete history automatically.

You simply save your work normally and tell Git when you have reached an important milestone.

---

## Why Every Developer Uses Git

Git provides several important advantages.

- Complete history of every project.
- Ability to restore previous versions.
- Safe experimentation.
- Easy synchronization with GitHub.
- Professional development workflow.
- Reliable project backup.

Even a one-person project benefits greatly from version control.

---

## Installing Git

Ubuntu makes installing Git simple.

First, update the package list.

```bash
sudo apt update
```

Then install Git.

```bash
sudo apt install git -y
```

Verify the installation.

```bash
git --version
```

Ubuntu should display the installed Git version.

---

## Configuring Git

Git records the name and email address associated with each commit.

Configure your name.

```bash
git config --global user.name "Rowan Crews"
```

Configure your email address.

```bash
git config --global user.email "your-email@example.com"
```

Replace the email address with the one associated with your GitHub account.

---

## Set the Default Branch

Modern repositories typically use **main** as the default branch.

Configure Git accordingly.

```bash
git config --global init.defaultBranch main
```

---

## Verify Your Configuration

Display your current configuration.

```bash
git config --list
```

Review the output carefully to ensure everything is correct.

---

## Your First Repository

Create a project directory.

```bash
mkdir hello-git
```

Move into the directory.

```bash
cd hello-git
```

Initialize Git.

```bash
git init
```

Git creates a hidden directory named:

```text
.git
```

This directory contains the complete version history of the project.

Never delete the `.git` directory unless you intentionally wish to remove version control.

---

## Checking Project Status

Display the current status.

```bash
git status
```

This command quickly becomes one of the most frequently used Git commands.

It shows:

- modified files
- new files
- deleted files
- staged files

---

## Staging Files

Suppose you create a file.

```text
README.md
```

Tell Git to begin tracking it.

```bash
git add README.md
```

To stage every modified file:

```bash
git add .
```

The period means "everything in the current directory."

---

## Creating a Commit

A commit records the current state of the project.

Create your first commit.

```bash
git commit -m "Initial commit"
```

A good commit message briefly describes what changed.

Examples:

```text
Initial commit

Added Git configuration

Created project structure

Completed Chapter 1

Installed Node.js
```

---

## Viewing History

Display the project's history.

```bash
git log
```

A simplified view.

```bash
git log --oneline
```

Many developers prefer the shorter format.

---

## Git and GitHub

Git and GitHub are related but different.

**Git**

Version control software installed on your computer.

**GitHub**

An online service that stores Git repositories and allows synchronization between computers.

Git works perfectly well without GitHub.

GitHub simply adds cloud storage and collaboration.

---

## Essential Git Commands

| Command | Purpose |
|----------|---------|
| `git init` | Initialize repository |
| `git status` | Show repository status |
| `git add` | Stage changes |
| `git commit` | Record changes |
| `git log` | Show history |
| `git config` | Configure Git |
| `git --version` | Display installed version |

These commands form the foundation of daily Git usage.

---

## Best Practices

- Commit frequently.
- Write meaningful commit messages.
- Review `git status` before committing.
- Keep commits focused on a single task.
- Synchronize regularly with GitHub.

---

## Common Mistakes

- Forgetting to commit work.
- Creating overly large commits.
- Writing vague commit messages.
- Ignoring `git status`.
- Deleting the `.git` directory.

---

## Chapter Checklist

Before continuing, confirm that you can:

- [ ] Install Git.
- [ ] Verify the installation.
- [ ] Configure your name.
- [ ] Configure your email address.
- [ ] Initialize a repository.
- [ ] Check repository status.
- [ ] Stage files.
- [ ] Create a commit.
- [ ] View commit history.

---

## Looking Ahead

The next chapter introduces Node.js and the Node Version Manager (NVM). You will learn why Node.js is the foundation of modern JavaScript development, how to install it correctly, and why using NVM provides a more flexible and maintainable development environment.