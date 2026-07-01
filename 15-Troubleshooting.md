# Chapter 15: Troubleshooting

## Introduction

Even a well-designed development environment will occasionally experience problems. Software updates, network interruptions, configuration errors, and hardware changes can all affect the behavior of Windows, WSL, Ubuntu, or development tools.

The purpose of this chapter is not simply to solve individual problems, but to teach a systematic approach to troubleshooting. Careful diagnosis is usually faster and more reliable than guessing or repeatedly reinstalling software.

---

## A Troubleshooting Philosophy

When something goes wrong:

1. Do not panic.
2. Do not immediately reinstall software.
3. Read the complete error message.
4. Change only one thing at a time.
5. Verify each change before making another.
6. Document both the problem and the solution.

Most problems have simple causes once they are understood.

---

## Understanding Error Messages

Error messages should be treated as valuable information rather than obstacles.

When an error occurs:

- Read the entire message.
- Identify the command that failed.
- Note filenames and directories.
- Look for permission errors.
- Look for network-related messages.

Never ignore the first error in a series of errors.

---

## Windows Problems

Common Windows issues include:

- Windows Update failures
- Driver conflicts
- Missing optional features
- Network problems
- Firewall configuration

Before investigating WSL, confirm that Windows itself is functioning correctly.

---

## WSL Problems

Examples include:

- WSL will not start.
- Ubuntu does not launch.
- Distribution not found.
- Missing Linux kernel.
- Virtualization errors.

Begin troubleshooting by running:

```powershell
wsl --status
```

Then:

```powershell
wsl --list --verbose
```

These commands provide valuable diagnostic information.

---

## Ubuntu Problems

Common Ubuntu issues include:

- Package installation failures
- Broken dependencies
- Incorrect permissions
- Full disk
- Corrupted package cache

Begin by updating package information:

```bash
sudo apt update
```

If necessary:

```bash
sudo apt upgrade
```

---

## Git Problems

Common issues include:

- Authentication failures
- SSH key problems
- Merge conflicts
- Repository configuration errors

Before assuming Git is broken, verify:

- Repository location
- Current branch
- Remote configuration
- Internet connection

---

## Node.js Problems

Common problems include:

- Incorrect Node version
- npm installation failures
- Missing packages
- Dependency conflicts

When using NVM, verify the active version:

```bash
node --version
npm --version
```

---

## Cursor Problems

Common issues include:

- Cannot connect to WSL
- Missing extensions
- Terminal problems
- Project not opening
- Indexing delays

Restarting Cursor often resolves temporary issues.

If problems continue:

- Restart WSL.
- Reopen the project.
- Verify the project resides inside the Linux file system.

---

## Network Problems

Many installation failures are caused by unreliable network connections.

Symptoms include:

- Downloads stopping unexpectedly
- Package installation failures
- Git clone failures
- npm timeouts

Verify Internet connectivity before troubleshooting development tools.

---

## Permission Problems

Linux permissions protect the operating system.

Avoid solving permission problems by repeatedly using `sudo`.

Instead:

- Determine who owns the file.
- Verify directory permissions.
- Understand why permission was denied.

Using administrative privileges unnecessarily can create additional problems.

---

## Recovery Strategy

If troubleshooting does not resolve the issue:

1. Review recent changes.
2. Restore from backup if appropriate.
3. Reinstall the affected software.
4. Rebuild the development environment only as a last resort.

A documented installation process makes rebuilding straightforward.

---

## Lessons Learned

During the development of this handbook, several practical lessons emerged:

- Stable network connectivity is essential during installation.
- WSL installation should always be performed from an Administrator terminal.
- Restart Windows whenever prompted during WSL installation.
- Verify Windows features before assuming WSL is at fault.
- Solve the underlying problem instead of repeatedly reinstalling software.

These lessons reflect real-world experience and should help prevent common installation difficulties.

---

## Best Practices

- Read error messages carefully.
- Change one thing at a time.
- Keep backups current.
- Record solutions for future reference.
- Verify assumptions before making changes.

---

## Common Mistakes

- Guessing instead of diagnosing.
- Running commands without understanding them.
- Ignoring error messages.
- Reinstalling software unnecessarily.
- Making multiple changes simultaneously.

---

## Chapter Checklist

Before continuing, confirm that you understand:

- [ ] A systematic troubleshooting process.
- [ ] How to gather diagnostic information.
- [ ] Common Windows problems.
- [ ] Common WSL problems.
- [ ] Common Ubuntu problems.
- [ ] Common Git and Node.js problems.
- [ ] When rebuilding the environment is appropriate.

---

## Looking Ahead

The final chapter explores advanced topics that extend beyond a basic WSL installation. These include Docker, Dev Containers, SSH, remote development, cloud development environments, and artificial intelligence coding tools. Together, these technologies build upon the foundation established throughout this handbook.