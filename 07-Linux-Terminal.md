# Chapter 7: The Linux Terminal

## Introduction

The Linux terminal is the primary interface used by software developers. While Ubuntu provides a graphical desktop, nearly every modern development tool is designed to be used from the command line.

Learning the terminal is one of the most valuable investments a web developer can make. It provides speed, precision, automation, and access to thousands of development tools.

Fortunately, only a relatively small number of commands are needed for everyday work.

---

## What Is a Terminal?

A terminal is a program that allows you to communicate directly with the Linux operating system by typing commands.

Rather than clicking icons and menus, you tell the operating system exactly what you want it to do.

For example:

```bash
pwd
```

asks Ubuntu to display your current working directory.

---



## Understanding the Prompt

A typical prompt looks like this:

```text
rowan@ubuntu:~$
```

Each part has meaning.


| Component | Meaning             |
| --------- | ------------------- |
| `rowan`   | Current user        |
| `ubuntu`  | Computer name       |
| `~`       | Home directory      |
| `$`       | Ready for a command |


Whenever the prompt appears, Ubuntu is waiting for your next command.

---



## The Current Working Directory

Linux always keeps track of your current location.

To display it:

```bash
pwd
```

Example output:

```text
/home/rowan
```

Think of this as your current location on the file system.

---



## Listing Files

To display the contents of the current directory:

```bash
ls
```

To display additional information:

```bash
ls -l
```

To include hidden files:

```bash
ls -la
```

These are among the most frequently used Linux commands.

---



## Changing Directories

Move into another directory with:

```bash
cd directory-name
```

Example:

```bash
cd code
```

To return to your home directory:

```bash
cd
```

To move up one level:

```bash
cd ..
```

---



## Creating Directories

Create a new directory:

```bash
mkdir projects
```

Create multiple nested directories:

```bash
mkdir -p code/tutorials/react
```

---



## Creating Files

Create an empty file:

```bash
touch notes.md
```

Although many files are created using an editor such as Cursor, the `touch` command is useful for quickly creating new files.

---



## Copying Files

Copy a file:

```bash
cp source.txt destination.txt
```

Copy an entire directory:

```bash
cp -r source-directory destination-directory
```

---



## Moving and Renaming Files

Move a file:

```bash
mv report.md archive/
```

Rename a file:

```bash
mv old-name.md new-name.md
```

Linux uses the same command for moving and renaming.

---



## Removing Files

Delete a file:

```bash
rm filename.txt
```

Delete a directory and everything inside it:

```bash
rm -r directory-name
```

Use these commands carefully.

Linux generally does not provide a recycle bin for terminal commands.

---



## Viewing File Contents

Display an entire text file:

```bash
cat filename.txt
```

Display one page at a time:

```bash
less filename.txt
```

For long files, `less` is usually the better choice.

---



## Command History

Ubuntu remembers previously entered commands.

Use the:

- ↑ Up Arrow
- ↓ Down Arrow

to browse earlier commands.

This feature saves considerable time during development.

---



## Tab Completion

One of the most useful terminal features is tab completion.

Instead of typing an entire filename:

```text
development-project
```

type:

```text
dev
```

and press **Tab**.

Ubuntu completes the remainder automatically whenever possible.

Always use tab completion when available.

---



## Canceling a Command

If a command is taking too long or appears to be running incorrectly:

Press:

```text
Ctrl + C
```

This safely interrupts most terminal programs.

---



## Clearing the Screen

To clear the terminal window:

```bash
clear
```

or simply press:

```text
Ctrl + L
```

---



## Essential Commands

The following commands are used daily by most developers.


| Command | Purpose                |
| ------- | ---------------------- |
| `pwd`   | Show current directory |
| `ls`    | List files             |
| `cd`    | Change directory       |
| `mkdir` | Create directory       |
| `touch` | Create file            |
| `cp`    | Copy                   |
| `mv`    | Move or rename         |
| `rm`    | Remove                 |
| `cat`   | Display file           |
| `less`  | View large files       |
| `clear` | Clear screen           |


Mastering these commands provides an excellent foundation for Linux development.

---



## Best Practices

- Learn a few commands thoroughly before learning many commands.
- Use tab completion whenever possible.
- Keep your terminal organized.
- Read command output carefully before entering another command.
- Think before using `rm`.

---



## Common Mistakes

- Running commands from the wrong directory.
- Deleting files accidentally with `rm`.
- Forgetting that Linux filenames are case-sensitive.
- Typing long filenames instead of using tab completion.
- Working too quickly without reading error messages.

---



## Chapter Checklist

Before continuing, confirm that you can:

- [ ] Display your current directory.
- [ ] List files.
- [ ] Change directories.
- [ ] Create directories.
- [ ] Create files.
- [ ] Copy files.
- [ ] Rename files.
- [ ] Delete files.
- [ ] View file contents.
- [ ] Use tab completion.
- [ ] Cancel a running command.

---



## Looking Ahead

The next chapter introduces Git, the version control system used throughout this handbook. You will learn why every professional developer uses Git, how it works, and how to configure it for daily development.