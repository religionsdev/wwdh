# Chapter 9: Node.js and NVM

## Introduction

Node.js is the runtime environment that powers modern JavaScript development. It allows JavaScript to run outside a web browser and provides the foundation for many of today's most popular development tools.

Whether you are building websites, APIs, or full-stack applications, Node.js is an essential part of the modern web development ecosystem.

This chapter explains what Node.js is, why it is important, and how to install and manage it using the Node Version Manager (NVM).

---

## What Is Node.js?

Originally, JavaScript could run only inside a web browser.

Node.js changed that by allowing JavaScript to run directly on your computer.

With Node.js you can:

- Build web servers
- Create APIs
- Run development tools
- Install third-party packages
- Build desktop applications
- Automate repetitive tasks

Nearly every modern JavaScript framework depends on Node.js.

---

## Why Use NVM?

NVM (Node Version Manager) allows multiple versions of Node.js to exist on the same computer.

Instead of installing one permanent version, NVM lets you:

- Install multiple versions
- Switch between versions
- Upgrade safely
- Remove older versions
- Test projects that require different releases

For professional development, NVM is considered the recommended installation method.

---

## Installing NVM

Download and install NVM using:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
```

After installation, close the terminal and open a new Ubuntu session.

Verify that NVM is available.

```bash
nvm --version
```

If Ubuntu displays the version number, the installation was successful.

---

## Installing Node.js

Install the current Long-Term Support (LTS) version.

```bash
nvm install --lts
```

Activate the installed version.

```bash
nvm use --lts
```

Set it as the default.

```bash
nvm alias default lts/*
```

---

## Verify the Installation

Display the installed version of Node.js.

```bash
node --version
```

Display the npm version.

```bash
npm --version
```

Display the NVM version.

```bash
nvm --version
```

If all three commands succeed, your installation is complete.

---

## Understanding npm

npm stands for **Node Package Manager**.

It installs and manages JavaScript libraries and development tools.

Examples include:

- React
- Astro
- Fastify
- Vite
- ESLint
- Prettier

Most JavaScript projects rely on npm.

---

## Installing Packages

Install a package locally.

```bash
npm install package-name
```

Example:

```bash
npm install react
```

Install a package globally.

```bash
npm install -g package-name
```

Use global installations sparingly.

Most project dependencies should remain local to the project.

---

## Creating a Project

Create a new directory.

```bash
mkdir hello-node
```

Move into it.

```bash
cd hello-node
```

Initialize a Node project.

```bash
npm init
```

For a faster setup:

```bash
npm init -y
```

This creates a file named:

```text
package.json
```

---

## Understanding package.json

The `package.json` file describes the project.

It records:

- Project name
- Version
- Scripts
- Dependencies
- Development dependencies
- License
- Metadata

Every Node project contains a `package.json` file.

---

## Installing Project Dependencies

Install all dependencies listed in a project.

```bash
npm install
```

This command reads `package.json` and installs everything required.

---

## Updating Packages

Check for outdated packages.

```bash
npm outdated
```

Update packages.

```bash
npm update
```

Keeping dependencies reasonably current improves security and reliability.

---

## Essential Node Commands

| Command | Purpose |
|----------|---------|
| `node --version` | Display Node.js version |
| `npm --version` | Display npm version |
| `nvm --version` | Display NVM version |
| `nvm install --lts` | Install latest LTS |
| `nvm use --lts` | Use LTS version |
| `npm init` | Create project |
| `npm install` | Install dependencies |
| `npm update` | Update dependencies |

---

## Best Practices

- Install Node.js using NVM.
- Use the LTS release for production work.
- Keep project dependencies local.
- Commit `package.json` to Git.
- Review package updates regularly.

---

## Common Mistakes

- Installing Node.js without NVM.
- Using outdated Node versions.
- Installing unnecessary global packages.
- Editing `package.json` without understanding its purpose.
- Ignoring dependency updates for long periods.

---

## Chapter Checklist

Before continuing, confirm that you can:

- [ ] Install NVM.
- [ ] Install the latest Node.js LTS release.
- [ ] Verify Node.js and npm installations.
- [ ] Create a Node project.
- [ ] Understand the purpose of `package.json`.
- [ ] Install project dependencies.
- [ ] Update installed packages.

---

## Looking Ahead

The next chapter introduces Cursor, the AI-powered development environment used throughout this handbook. You will learn how to install Cursor, configure it for WSL development, organize your workspace, and establish a productive AI-assisted coding workflow.