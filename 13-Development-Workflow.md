# Chapter 13: Daily Development Workflow

## Introduction

A productive development environment depends as much on good habits as on good software. A consistent workflow reduces mistakes, minimizes distractions, and allows you to focus on solving problems rather than remembering procedures.

This chapter presents the standard daily workflow used throughout this handbook. Although individual projects may differ, the overall process remains the same.

---

## Our Development Philosophy

Throughout this handbook we follow a simple principle:

> **Windows is the workstation. Linux is the workshop.**

Windows provides:

- Cursor
- Microsoft 365
- Outlook
- OneDrive
- Web browsers
- ChatGPT
- Communication tools

Ubuntu provides:

- Source code
- Git
- Node.js
- npm
- Development servers
- Build tools
- Package managers

Each operating system is used for what it does best.

---

## Beginning the Day

A typical development session begins with the following steps.

1. Start Windows.
2. Verify Internet connectivity.
3. Launch Cursor.
4. Open the appropriate project.
5. Open the integrated terminal.
6. Confirm you are in the correct project directory.

Example:

```bash
pwd
```

Example output:

```text
/home/rowan/code/project-monorepo
```

Knowing your current directory helps prevent mistakes.

---

## Update Your Repository

Before beginning work, synchronize your local repository.

```bash
git pull
```

If you are the only developer and are working on a single computer, there may be no changes.

If you work from multiple computers, this step ensures you begin with the latest version.

---

## Install Dependencies (When Needed)

If project dependencies have changed:

```bash
npm install
```

This command installs all packages listed in the project's `package.json` file.

---

## Start the Development Server

Most modern JavaScript projects use a local development server.

Typical command:

```bash
npm run dev
```

The application becomes available through your web browser at a local address such as:

```text
http://localhost:5173
```

The exact address depends on the project.

---

## During Development

As you work:

- Edit code in Cursor.
- Test changes frequently.
- Save your work regularly.
- Read terminal messages carefully.
- Resolve errors as they occur.

Small, incremental progress is generally more reliable than making many large changes at once.

---

## Working with AI

Cursor's AI can assist throughout the development process.

Useful tasks include:

- Explaining unfamiliar code
- Generating boilerplate
- Refactoring functions
- Identifying errors
- Writing documentation
- Reviewing architecture

AI should support your thinking, not replace it.

Always review generated code before accepting it.

---

## Checking Your Work

Before committing changes:

```bash
git status
```

Review:

- Modified files
- New files
- Deleted files

Confirm that only the intended changes will be committed.

---

## Creating a Commit

Stage your changes.

```bash
git add .
```

Create a commit.

```bash
git commit -m "Describe the completed work"
```

Examples:

```text
Completed Chapter 5

Installed Node.js

Added project templates

Updated README
```

A clear commit history becomes invaluable over time.

---

## Uploading Your Work

Push completed commits to GitHub.

```bash
git push
```

This creates an off-site backup and synchronizes your repository.

---

## Ending the Day

Before shutting down:

- Ensure all files are saved.
- Confirm there are no unfinished commits.
- Push completed work to GitHub.
- Stop any running development servers.
- Close Cursor.
- Shut down Windows normally.

A few minutes spent organizing your work at the end of the day often saves much more time the following morning.

---

## Daily Workflow Summary

The complete workflow is:

1. Start Windows.
2. Open Cursor.
3. Open the project.
4. Pull the latest changes.
5. Install dependencies if needed.
6. Start the development server.
7. Write and test code.
8. Review changes.
9. Commit changes.
10. Push to GitHub.
11. Shut down cleanly.

Following the same workflow every day develops productive habits and reduces avoidable errors.

---

## Best Practices

- Work on one task at a time.
- Commit frequently.
- Push changes regularly.
- Test before committing.
- Keep your workspace organized.
- Review AI-generated code carefully.

---

## Common Mistakes

- Forgetting to pull changes.
- Forgetting to push commits.
- Leaving development servers running.
- Working in the wrong project directory.
- Making large, unfocused commits.

---

## Chapter Checklist

Before continuing, confirm that you can:

- [ ] Open a project in Cursor.
- [ ] Use the integrated terminal.
- [ ] Pull the latest repository changes.
- [ ] Install project dependencies.
- [ ] Start a development server.
- [ ] Review repository status.
- [ ] Commit changes.
- [ ] Push changes to GitHub.
- [ ] End a development session cleanly.

---

## Looking Ahead

The next chapter focuses on maintaining your development environment over time. You will learn how to update Ubuntu, Node.js, Git, and other tools, back up your WSL environment, and recover quickly from hardware failures or system problems.