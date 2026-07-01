# Style Guide

## Purpose

This style guide establishes the editorial standards for the WSL Web Development Handbook. Every chapter should follow these standards to ensure the handbook reads as though it were written by a single author.

---

# Audience

The handbook is written for:

- Beginning to intermediate web developers
- Developers using Windows 11 Professional
- Developers learning Linux through WSL
- Individual developers and small teams

Assume the reader has little or no prior Linux experience.

---

# Writing Style

Write in a clear, professional, instructional style.

The tone should be:

- Friendly
- Precise
- Concise
- Encouraging
- Technically accurate

Avoid slang, unnecessary humor, and overly casual language.

---

# Voice

Write in the active voice whenever practical.

Prefer:

> Install Ubuntu.

Instead of:

> Ubuntu should be installed.

---

# Tense

Use the present tense whenever possible.

Example:

> Ubuntu stores user files in the home directory.

Avoid unnecessary future tense.

---

# Headings

Use this hierarchy:

```text
# Chapter Title

## Major Section

### Subsection

#### Rarely Needed
```

Avoid deeper heading levels.

---

# Paragraphs

Keep paragraphs relatively short.

One idea per paragraph.

Avoid large blocks of text.

---

# Lists

Use bullet lists when sequence does not matter.

Use numbered lists only when order matters.

---

# Commands

Place every command inside its own fenced code block.

Example:

```bash
sudo apt update
```

Always identify the language when possible.

---

# File Names

Show filenames using inline code.

Example:

`README.md`

---

# Directory Names

Show directories using inline code.

Example:

`/home/rowan/code`

---

# Keyboard Keys

Use bold text.

Example:

**Enter**

**Ctrl+C**

---

# Notes

Important information should appear under a short heading.

Example

> **Note**
>
> Ubuntu does not display passwords while typing.

---

# Tips

Helpful suggestions should appear separately.

Example

> **Tip**
>
> Restart Windows whenever prompted during WSL installation.

---

# Warnings

Warnings should clearly describe potential problems.

Example

> **Warning**
>
> Do not store active Node.js projects under `/mnt/c`.

---

# Screenshots

Screenshots should:

- Show only relevant information.
- Be cropped tightly.
- Include captions.
- Use arrows only when necessary.

---

# Diagrams

Prefer simple diagrams over complex illustrations.

Use diagrams only when they improve understanding.

---

# Terminology

Use these names consistently.

| Preferred | Avoid |
|------------|-------|
| Windows Terminal | Terminal App |
| Ubuntu | Linux OS |
| WSL | Linux Emulator |
| Project | App Folder |
| Repository | Repo Folder |

---

# Chapter Structure

Most chapters should follow this structure.

1. Introduction
2. Main Sections
3. Best Practices
4. Common Mistakes
5. Chapter Checklist
6. Looking Ahead

Installation chapters may include:

- Prerequisites
- Installation Steps
- Verification
- Troubleshooting

---

# Code Examples

Code examples should:

- Be complete.
- Be correct.
- Be tested whenever possible.
- Include only relevant commands.

---

# Consistency

Throughout the handbook:

- Use Ubuntu LTS consistently.
- Recommend storing projects inside Linux.
- Prefer stability over novelty.
- Explain *why*, not just *how*.

---

# Revision Policy

Update this handbook as tools evolve.

Do not rewrite chapters unnecessarily.

Revise only when changes improve clarity, accuracy, or current best practices.