# Chapter 4: Installing Ubuntu

## Introduction

Ubuntu is the Linux operating system used throughout this handbook. It provides a stable, well-documented, and widely supported environment for modern web development. Once installed, Ubuntu becomes the home for your source code, development tools, package managers, and local development servers.

This chapter walks through the initial Ubuntu setup and prepares the system for future development work.

---

## Why Ubuntu?

Many Linux distributions are excellent choices for development. This handbook uses **Ubuntu Long-Term Support (LTS)** because it offers:

- Long-term stability
- Excellent documentation
- Broad community support
- Strong compatibility with development tools
- Predictable update cycles

The goal is to build a dependable environment that can remain in service for years with minimal maintenance.

---

## First Launch

After WSL has been installed successfully, Ubuntu will launch automatically the first time.

During the initial startup, Ubuntu completes its internal configuration and prepares the Linux environment.

This process normally takes only a few minutes.

---

## Creating Your Linux Account

Ubuntu will prompt you to create two items:

### Linux Username

Example:

```text
rowan
```

This username becomes the owner of your Linux files and folders.

Choose a simple username using only lowercase letters.

---

### Linux Password

Ubuntu will also ask you to create a password.

Unlike Windows, Linux does **not** display any characters while you type your password. The cursor will not move. This behavior is normal.

Choose a strong password and store it in your password manager.

---

## The Linux Home Folder

After signing in, Ubuntu places you in your home directory.

Example:

```text
/home/rowan
```

This becomes your personal workspace.

Throughout this handbook, nearly all development work will occur somewhere beneath this directory.

---

## Updating Ubuntu

Before installing any development software, update the operating system.

Run:

```bash
sudo apt update
sudo apt upgrade -y
```

These commands:

- Refresh the package list.
- Install the latest security updates.
- Upgrade installed software.

Keeping Ubuntu current helps ensure a secure and reliable development environment.

---

## Restarting Ubuntu

Unlike Windows, Ubuntu rarely requires a restart after routine updates.

If a restart is recommended, simply close the Ubuntu window and reopen it, or restart WSL if necessary.

---

## Understanding `sudo`

Linux protects important system files by requiring administrator privileges for certain tasks.

The `sudo` command temporarily grants administrative permissions.

Example:

```bash
sudo apt update
```

Whenever Ubuntu requests your password after using `sudo`, enter your Linux password.

---

## Best Practices

- Use Ubuntu LTS.
- Update Ubuntu before installing development tools.
- Keep your Linux username simple.
- Store your password securely.
- Avoid changing system settings unless you understand their purpose.

---

## Common Mistakes

- Forgetting the Linux password.
- Interrupting Ubuntu during its first startup.
- Skipping system updates.
- Confusing the Linux password with the Windows password.
- Attempting to perform development work before Ubuntu has been updated.

---

## Chapter Checklist

Before continuing, confirm that:

- [ ] Ubuntu launches successfully.
- [ ] A Linux username has been created.
- [ ] A Linux password has been created.
- [ ] Ubuntu reaches the command prompt without errors.
- [ ] `sudo apt update` completes successfully.
- [ ] `sudo apt upgrade -y` completes successfully.

---

## Looking Ahead

The next chapter introduces the Ubuntu operating system in greater detail. You will learn how the Linux file system is organized, where development projects should be stored, and how to navigate the operating system with confidence before installing additional development tools.