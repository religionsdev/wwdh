# Chapter 14: Maintenance and Backup

## Introduction

A professional development environment is not complete when the installation is finished. It must also be maintained, protected, and capable of being restored quickly after hardware failure, software corruption, or accidental deletion.

This chapter presents a practical maintenance strategy for Windows, WSL, Ubuntu, and development projects. The objective is to minimize downtime while preserving the integrity of your work.

---

## The Maintenance Philosophy

Good maintenance is proactive rather than reactive.

Instead of waiting for problems to occur, establish simple routines that keep the development environment healthy.

The goals are:

- Maintain system reliability.
- Keep software current.
- Protect source code.
- Preserve important configuration.
- Simplify recovery after failures.

---

## What Should Be Backed Up?

Not everything on a development computer needs to be backed up.

Priority should be given to:

- Source code
- Git repositories
- Markdown documentation
- Configuration files
- SSH keys
- Package configuration files
- Environment configuration

Installed software can always be reinstalled.

Your work cannot.

---

## GitHub Is Your First Backup

Every active project should be stored in a Git repository and pushed regularly to GitHub.

Benefits include:

- Version history
- Protection from hardware failure
- Easy collaboration
- Access from multiple computers

Commit early and commit often.

---

## Backing Up WSL

WSL distributions can be exported to a backup file.

Example:

```powershell
wsl --export Ubuntu ubuntu-backup.tar
```

This creates a complete backup of the Ubuntu distribution.

Store backup files on another drive or external storage.

---

## Restoring a WSL Backup

A previously exported distribution can be imported.

Example:

```powershell
wsl --import Ubuntu D:\WSL\Ubuntu ubuntu-backup.tar
```

This restores the Linux environment from the backup archive.

---

## Updating Windows

Keep Windows current by:

- Installing Windows Updates.
- Restarting when required.
- Updating device drivers when appropriate.

Avoid installing optional drivers unless there is a clear benefit.

---

## Updating Ubuntu

Regularly update Ubuntu.

```bash
sudo apt update
sudo apt upgrade -y
```

Security updates should not be postponed indefinitely.

---

## Updating Development Tools

Review updates for:

- Cursor
- Git
- Node.js
- npm
- Development extensions

Update intentionally rather than immediately.

Allow new releases time to mature before adopting them in a production development environment.

---

## Cleaning the System

Occasionally remove software that is no longer needed.

Examples include:

- Old Node versions
- Unused npm packages
- Temporary files
- Obsolete projects

A clean system is easier to maintain.

---

## Document Important Changes

Whenever you make significant changes to your environment, record them.

Examples include:

- Installing new development tools.
- Changing project locations.
- Updating major software versions.
- Replacing hardware.

Documentation reduces future troubleshooting time.

---

## Recovery Planning

Assume every computer will eventually fail.

A recovery plan should answer:

- Where is the latest source code?
- Where are WSL backups stored?
- How is Ubuntu reinstalled?
- How are SSH keys restored?
- How long will recovery take?

A documented recovery process reduces stress during unexpected failures.

---

## Maintenance Schedule

### Weekly

- Push projects to GitHub.
- Install security updates.
- Review backup status.

### Monthly

- Update Ubuntu.
- Review Windows updates.
- Remove unnecessary files.
- Verify project backups.

### Quarterly

- Export the WSL distribution.
- Review installed software.
- Test the recovery process.
- Update documentation.

---

## Best Practices

- Push code to GitHub frequently.
- Export WSL before major system changes.
- Keep multiple copies of important work.
- Maintain current documentation.
- Test backups periodically.

---

## Common Mistakes

- Assuming GitHub replaces all backups.
- Forgetting to back up SSH keys.
- Delaying operating system updates.
- Ignoring documentation.
- Discovering backup problems only after a failure.

---

## Chapter Checklist

Before continuing, confirm that:

- [ ] All projects are stored in Git.
- [ ] GitHub contains current copies of active projects.
- [ ] A WSL backup strategy has been established.
- [ ] Windows and Ubuntu update procedures are understood.
- [ ] A recovery plan has been documented.

---

## Looking Ahead

The next chapter addresses common problems encountered when working with Windows, WSL, Ubuntu, Git, Node.js, and Cursor. It presents systematic troubleshooting techniques designed to identify and resolve issues efficiently while minimizing disruption to your development work.