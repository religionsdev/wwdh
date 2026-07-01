# Chapter 5: Ubuntu Fundamentals

## Introduction

Ubuntu is more than an operating system—it is the foundation of your development environment. While Windows remains your primary desktop operating system, Ubuntu provides the tools and environment used to build, test, and maintain modern web applications.

This chapter introduces the essential concepts of Ubuntu that every developer should understand before installing development tools.

In this chapter, we shift from installation to understanding Linux. Chapter 5, Ubuntu Fundamentals, is one of the most important chapters in the handbook because it explains how Linux works, not just how to use it. A solid understanding of the contents of this chapter will make everything that follows—Git, Node.js, Cursor, and your web development stack—much easier to grasp.

---

## What Is Ubuntu?

Ubuntu is a Linux distribution developed by Canonical Ltd. It combines the Linux kernel with a large collection of software packages into a complete operating system.

Ubuntu is widely used by:

- Software developers
- Universities
- Businesses
- Cloud providers
- Data centers
- Scientific researchers

Its stability and extensive documentation make it an excellent choice for professional web development.

---

## The Linux File System

Unlike Windows, Linux does not organize storage using drive letters such as **C:** or **D:**.

Instead, everything begins from a single root directory:

```text
/
```

From this root directory, the operating system is organized into a series of standard folders.

Some of the most important are:

| Directory | Purpose |
|-----------|---------|
| `/` | Root of the file system |
| `/home` | User home directories |
| `/etc` | System configuration files |
| `/usr` | Installed applications and libraries |
| `/var` | Logs and variable data |
| `/tmp` | Temporary files |
| `/mnt` | Mounted file systems, including Windows drives |

Understanding these directories will make Linux much easier to navigate.

---

## Your Home Directory

After logging in, Ubuntu places you in your home directory.

Example:

```text
/home/rowan
```

This directory belongs to you.

Here you can safely create:

- Development projects
- Documents
- Scripts
- Configuration files

Throughout this handbook, nearly all of your work will occur within your home directory.

---

## Recommended Folder Structure

Create a dedicated folder for your development work.

For example:

```text
/home/rowan/

code/
projects/
reference/
templates/
downloads/
archive/
```

The exact organization may evolve over time, but separating active projects from reference material makes navigation much easier.

---

## Files and Directories

Linux distinguishes between files and directories.

Examples:

```text
notes.md      ← file

projects/     ← directory
```

Directories may contain additional directories, forming a hierarchical structure.

---

## File Names

Linux filenames are case-sensitive.

These are considered different files:

```text
Project.md

project.md

PROJECT.md
```

For consistency, this handbook recommends:

- lowercase letters
- hyphens between words
- descriptive names

Example:

```text
wsl-web-development-handbook.md
```

---

## Hidden Files

Linux stores many configuration files as hidden files.

Examples:

```text
.gitconfig

.bashrc

.profile
```

These files begin with a period (`.`).

Most are important and should not be modified without understanding their purpose.

---

## Absolute and Relative Paths

Linux supports two kinds of file paths.

### Absolute path

Begins at the root directory.

Example:

```text
/home/rowan/code/project
```

### Relative path

Begins from your current location.

Example:

```text
code/project
```

Both forms are useful and are used throughout this handbook.

---

## File Permissions

Linux protects files through permissions.

Every file has:

- an owner
- a group
- permissions

Permissions determine who may:

- read
- write
- execute

This security model is one reason Linux is highly reliable.

---

## The Command Prompt

Ubuntu is controlled primarily through the terminal.

A prompt similar to the following indicates that Ubuntu is ready to receive commands.

```text
rowan@ubuntu:~$
```

Although graphical applications exist, the terminal remains the primary interface for development work.

---

## Best Practices

- Keep development work inside your home directory.
- Use descriptive filenames.
- Use lowercase names whenever practical.
- Learn the standard Linux directory structure.
- Avoid modifying system folders unnecessarily.

---

## Common Mistakes

- Storing projects in system directories.
- Confusing Windows paths with Linux paths.
- Ignoring case sensitivity.
- Deleting hidden configuration files.
- Working as the root user unnecessarily.

---

## Chapter Checklist

Before continuing, confirm that you understand:

- [ ] The purpose of Ubuntu.
- [ ] The Linux directory structure.
- [ ] Your home directory.
- [ ] The difference between files and directories.
- [ ] Absolute and relative paths.
- [ ] Basic Linux file permissions.

---

## Looking Ahead

The next chapter explains how Windows and Linux work together within WSL. You will learn how the two operating systems share files, when they should remain separate, and why storing development projects in the Linux file system results in better performance and fewer problems. 