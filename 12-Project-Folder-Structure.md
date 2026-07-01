# Chapter 12: Project Folder Structure

## Introduction

A well-organized project structure is one of the simplest ways to improve productivity. Consistent organization makes projects easier to navigate, simplifies backups, reduces confusion, and makes it easier to move between computers.

This chapter establishes the standard directory structure used throughout this handbook. Every project described in later chapters will follow these conventions.

---

## Design Principles

Our folder structure is based on several principles.

- Every folder has a single purpose.
- Active work is separated from archived work.
- Reference material is easy to locate.
- Templates are reusable.
- Every project has one authoritative location.

Consistency is more important than perfection.

---



## The Home Directory

Your Linux home directory serves as the root of your personal workspace.

Example:

```text
/home/rowan
```

Everything related to your development work begins here.

---



## Recommended Directory Structure

The following structure is recommended.

```text
/ home / rowan

├── archive
├── code
├── downloads
├── reference
├── templates
└── tools
```

Each directory has a specific purpose.

---



## The `code` Directory

The `code` directory contains all active software projects.

Example:

```text
/home/rowan/code

├── project-monorepo
├── wsl-web-development-handbook
├── documentation-toolkit
└── experiments
```

Every Git repository should live somewhere beneath this directory.

---



## The `reference` Directory

The `reference` directory stores information that supports development but is not itself a software project.

Examples include:

- PDF documentation
- API references
- Technical articles
- Specifications
- Research notes

These files are generally read but not modified.

---



## The `templates` Directory

The `templates` directory contains reusable starting points for future work.

Examples include:

```text
templates/

chapter-template.md
installation-chapter-template.md
reference-chapter-template.md
appendix-template.md

README-template.md
LICENSE-template.md
.gitignore-template
```

Using templates encourages consistency across projects.

---



## The `tools` Directory

The `tools` directory stores utilities that are not installed through the operating system's package manager.

Examples include:

- Stand-alone utilities
- Downloaded binaries
- Helper scripts
- Development tools

Avoid mixing tools with active projects.

---



## The `archive` Directory

Completed or inactive projects may be moved into the archive.

Example:

```text
archive/

old-project

prototype-v1

deprecated-code
```

Archiving reduces clutter while preserving valuable work.

---



## Naming Conventions

This handbook recommends:

- lowercase names
- descriptive names
- hyphens between words

Examples:

```text
project-monorepo

wsl-web-development-handbook

documentation-toolkit
```

Avoid spaces whenever practical.

---



## One Repository Per Project

Each major project should have its own Git repository.

Examples:

```text
project-monorepo

documentation-toolkit

wsl-web-development-handbook

african-american-religions
```

Separate repositories make projects easier to maintain and simplify version control.

---



## Documentation Within Projects

Every repository should contain its own documentation.

A typical structure might be:

```text
project/

docs/
src/
tests/

README.md
LICENSE
.gitignore
package.json
```

Documentation should remain close to the code it describes.

---



## Our Standard Development Environment

Throughout this handbook we adopt the following standard.

```text
/home/rowan/

archive/
code/
downloads/
reference/
templates/
tools/
```

Every future chapter assumes this organization.

---



## Best Practices

- Store active projects in `code`.
- Use one repository per project.
- Keep templates separate from projects.
- Archive inactive work rather than deleting it.
- Use descriptive directory names.
- Maintain the same structure on every development computer.

---



## Common Mistakes

- Mixing unrelated projects.
- Creating deeply nested directory structures.
- Using inconsistent names.
- Storing projects in multiple locations.
- Keeping duplicate copies of repositories.

---



## Chapter Checklist

Before continuing, confirm that you understand:

- [ ] The purpose of each top-level directory.
- [ ] Where active projects belong.
- [ ] Where templates belong.
- [ ] Where reference material belongs.
- [ ] Why every project should have its own repository.
- [ ] The recommended naming conventions.

---



## Looking Ahead

The next chapter brings together everything introduced so far into a complete daily development workflow. From starting the computer in the morning to committing code at the end of the day, you will learn a consistent process for working efficiently with Windows, WSL, Ubuntu, Cursor, Git, and GitHub.