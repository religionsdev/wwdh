# Chapter 6: Windows and Linux in WSL

## Introduction

One of the greatest strengths of the Windows Subsystem for Linux (WSL) is that it combines two operating systems into a single development environment. Windows and Ubuntu run side by side, each performing the tasks for which it is best suited.

Understanding how these two environments interact is essential for building a reliable and efficient workflow. This chapter explains how Windows and Linux coexist, how they share files, and where development projects should be stored.

---

## Two Operating Systems, One Computer

When using WSL, you are working with two operating systems:

**Windows**

- Desktop environment
- Microsoft 365
- Outlook
- OneDrive
- Web browsers
- Device management
- Cursor

**Ubuntu (Linux)**

- Source code
- Git
- Node.js
- npm
- Development servers
- Build tools
- Package managers

Each operating system has its own responsibilities.

---

## Separate File Systems

Windows and Linux each maintain their own file system.

### Windows

Typical locations include:

```text
C:\Users\Rowan\
C:\Program Files\
C:\Windows\
```

### Linux

Typical locations include:

```text
/
├── home
├── etc
├── usr
├── var
└── mnt
```

Although each operating system has its own file system, WSL allows them to access one another when necessary.

---

## Accessing Windows Files from Linux

Windows drives appear under the `/mnt` directory.

Examples:

```text
/mnt/c
/mnt/d
/mnt/e
```

To access your Windows Documents folder:

```text
/mnt/c/Users/Rowan/Documents
```

This allows Ubuntu to read and write Windows files.

---

## Accessing Linux Files from Windows

Windows can also access Linux files.

In File Explorer, enter:

```text
\\wsl.localhost\Ubuntu\
```

or

```text
\\wsl$
```

You can then browse your Linux home directory just as you would any Windows folder.

---

## Where Should Projects Be Stored?

This handbook adopts one important rule.

**Store all active development projects inside the Linux file system.**

Example:

```text
/home/rowan/code
```

Avoid storing active Node.js projects under:

```text
C:\Users\Rowan\
```

or

```text
/mnt/c/Users/Rowan/
```

Running Linux development tools directly against Windows files can reduce performance and occasionally introduce permission or file-watching problems.

---

## Our Standard Project Location

Throughout this handbook, all active projects will be stored here:

```text
/home/rowan/code
```

Examples:

```text
/home/rowan/code/wsl-web-development-handbook

/home/rowan/code/project-monorepo

/home/rowan/code/experiments
```

Using a single location keeps the development environment organized and simplifies backups.

---

## Working with Cursor

Cursor runs as a Windows application but works seamlessly with files stored inside Ubuntu.

The recommended workflow is:

1. Store projects inside Linux.
2. Open the project from Cursor.
3. Edit files normally.
4. Run development commands from the Ubuntu terminal.

This combines the strengths of both operating systems.

---

## Sharing Files

Occasionally you may need to exchange files between Windows and Linux.

Examples include:

- PDF documents
- Images
- Downloads
- Office files

These can easily be copied between the two environments.

Large development projects, however, should remain inside Linux.

---

## Backup Considerations

Treat the Linux file system as the authoritative location for your development projects.

Recommended backup strategies include:

- GitHub repositories
- WSL export
- Regular backups of your home directory

Do not rely solely on Windows backups for Linux development projects.

---

## Best Practices

- Keep active projects inside Ubuntu.
- Use Windows for productivity software.
- Use Linux for development.
- Organize projects under a single `code` directory.
- Back up projects regularly using Git.

---

## Common Mistakes

- Developing Node.js projects directly on the Windows drive.
- Mixing Windows and Linux project folders.
- Forgetting which operating system owns a file.
- Editing Linux system files from Windows without understanding their purpose.
- Keeping multiple copies of the same project.

---

## Chapter Checklist

Before continuing, confirm that you understand:

- [ ] Windows and Ubuntu use separate file systems.
- [ ] Linux can access Windows drives through `/mnt`.
- [ ] Windows can access Linux files through `\\wsl.localhost\Ubuntu`.
- [ ] Active development projects belong inside the Linux file system.
- [ ] Cursor can edit Linux projects while running on Windows.

---

## Looking Ahead

The next chapter introduces the Linux terminal. You will learn the essential commands used every day by web developers, along with practical techniques for navigating directories, managing files, and working efficiently from the command line.