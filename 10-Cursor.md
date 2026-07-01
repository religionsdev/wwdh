# Chapter 10: Cursor

## Introduction

Cursor is the primary integrated development environment (IDE) used throughout this handbook. Built on Visual Studio Code, Cursor combines a familiar editing experience with advanced artificial intelligence tools that assist with writing, understanding, debugging, and refactoring code.

This handbook assumes that Cursor is your primary development environment. Properly configured, it becomes the central workspace for writing code, managing projects, interacting with Git, and working with AI.

---

## Why Cursor?

Many excellent code editors are available, including Visual Studio Code, WebStorm, and Vim. This handbook uses Cursor because it integrates powerful AI capabilities directly into the development workflow.

Cursor provides:

- Intelligent code completion
- AI-assisted programming
- Built-in Git support
- Integrated terminal
- Project-wide code understanding
- Extension compatibility with Visual Studio Code
- Excellent WSL support

For individual developers, Cursor can significantly improve productivity while reducing repetitive work.

---

## Installing Cursor

Download Cursor from the official website.

Install it using the standard Windows installer.

Accept the default installation options unless you have a specific reason to change them.

After installation, launch Cursor.

---

## Signing In

Sign in using your Cursor account.

A paid subscription provides access to advanced AI features and higher usage limits. Throughout this handbook, we assume an active Cursor subscription.

---

## Cursor and WSL

Although Cursor runs as a Windows application, it works exceptionally well with projects stored inside WSL.

Our standard workflow is:

- Cursor runs on Windows.
- Source code resides inside Ubuntu.
- Git runs inside Ubuntu.
- Node.js runs inside Ubuntu.
- Development servers run inside Ubuntu.

This approach combines the strengths of both operating systems.

---

## Opening a Project

Open your project by selecting:

**File → Open Folder**

Navigate to your project stored in WSL.

For example:

```text
\\wsl.localhost\Ubuntu\home\rowan\code\project-monorepo
```

Cursor treats the Linux project as though it were a local Windows folder.

---

## The Cursor Interface

Become familiar with the major areas of the interface.

### Explorer

Displays the project files.

---

### Editor

Displays the currently opened file.

---

### Terminal

Runs Linux commands directly inside your project.

---

### Source Control

Displays Git status and commit history.

---

### AI Chat

Allows you to ask questions about your project, generate code, explain unfamiliar code, and receive development assistance.

---

## Using the Integrated Terminal

Whenever possible, use Cursor's integrated terminal rather than opening a separate terminal window.

Advantages include:

- Immediate access to the project directory
- Consistent environment
- Easier workflow
- Integrated Git commands

Throughout this handbook, terminal commands assume you are working from Cursor's integrated terminal.

---

## Extensions

Cursor supports nearly all Visual Studio Code extensions.

Recommended extensions include:

- ESLint
- Prettier
- EditorConfig
- Markdown All in One
- GitLens
- Error Lens
- Docker (if applicable)

Install only the extensions you actually use.

Too many extensions increase complexity and can reduce performance.

---

## Recommended Settings

Several settings improve the development experience.

Examples include:

- Enable format on save.
- Enable automatic updates.
- Use spaces instead of tabs.
- Display line numbers.
- Enable word wrap for Markdown files.
- Enable autosave if it matches your workflow.

As this handbook progresses, additional recommended settings will be introduced.

---

## AI-Assisted Development

Cursor's AI should be viewed as a development partner rather than an automatic code generator.

Use AI to:

- Explain unfamiliar code.
- Generate boilerplate.
- Refactor existing code.
- Suggest improvements.
- Identify bugs.
- Review architecture.
- Produce documentation.

Always review AI-generated code before accepting it.

Understanding the code remains the developer's responsibility.

---

## Project Organization

Keep each project self-contained.

A typical project might include:

```text
project/

src/
public/
docs/
tests/

package.json
README.md
.gitignore
```

Maintain a consistent organization across all projects.

---

## Best Practices

- Keep projects inside the Linux file system.
- Use the integrated terminal.
- Commit changes frequently with Git.
- Review AI-generated code carefully.
- Keep extensions to a minimum.
- Organize projects consistently.

---

## Common Mistakes

- Opening projects from the Windows file system instead of WSL.
- Installing unnecessary extensions.
- Accepting AI-generated code without review.
- Ignoring Git status.
- Mixing unrelated projects within the same workspace.

---

## Chapter Checklist

Before continuing, confirm that you can:

- [ ] Install Cursor.
- [ ] Sign in to your Cursor account.
- [ ] Open a WSL project.
- [ ] Use the integrated terminal.
- [ ] Use AI Chat effectively.
- [ ] Install useful extensions.
- [ ] Configure basic editor settings.

---

## Looking Ahead

The next chapter introduces GitHub, the cloud-based platform used to store Git repositories, collaborate with other developers, and back up projects. You will learn how GitHub complements Git, how to connect your local repositories, and how to establish a professional workflow for managing your source code.