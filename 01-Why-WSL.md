# Chapter 1: Why WSL?

## Introduction

Modern web development is built on Linux.

The operating systems that power cloud platforms, web servers, containers, continuous integration systems, and many development tools are overwhelmingly Linux-based. While Windows remains an outstanding desktop operating system, Linux has become the standard operating environment for professional software development.

The Windows Subsystem for Linux (WSL) combines the strengths of both operating systems. It allows developers to run a genuine Linux environment directly within Windows without the overhead of a traditional virtual machine.

For many developers, WSL provides the ideal balance: Windows remains the desktop operating system while Linux becomes the development environment.

---



## What Is WSL?

The Windows Subsystem for Linux is a Microsoft technology that allows Linux distributions such as Ubuntu to run directly on Windows.

Unlike a virtual machine, WSL shares the computer's hardware with Windows. Linux applications run alongside Windows applications, allowing both environments to work together while maintaining their own file systems and tools.

With WSL, a developer can:

- Use the Linux terminal.
- Install Linux development tools.
- Run Node.js, Git, and package managers.
- Develop and test web applications.
- Edit Linux files directly from Cursor.

---



## Why Use WSL?

WSL combines the advantages of Windows and Linux into a single development environment.

### Windows provides

- A familiar desktop environment
- Microsoft 365
- Outlook
- OneDrive
- Excellent hardware support
- Device management
- Productivity applications



### Linux provides

- Native development tools
- Package management
- Node.js development
- Git
- Build systems
- Development servers
- A Unix command-line environment

Using each operating system for what it does best results in a stable and productive workflow.

---



## Why Ubuntu LTS?

This handbook uses Ubuntu Long-Term Support (LTS).

Ubuntu LTS is chosen because it offers:

- Long-term stability
- Excellent documentation
- Broad community support
- Wide compatibility with development tools
- Predictable update cycles

For a professional development environment, stability is generally more valuable than having the newest features.

---



## Why Not Use a Virtual Machine?

Virtual machines remain valuable for many purposes, but WSL offers several advantages for daily web development.

Compared with a traditional virtual machine, WSL typically provides:

- Faster startup
- Lower memory usage
- Better integration with Windows
- Simpler file sharing
- Easier day-to-day development

For most web developers, WSL is the more practical choice.

---



## Our Development Philosophy

This handbook follows a simple principle.

**Windows is the workstation.**

Windows is used for productivity applications, communication, documentation, and development tools such as Cursor.

**Linux is the workshop.**

Linux contains the development tools, project source code, package managers, and local development servers.

Keeping these responsibilities separate makes the environment easier to understand, maintain, and rebuild.

---



## Key Takeaways

- Modern web development is centered on Linux.
- WSL allows Linux and Windows to work together.
- Ubuntu LTS provides a stable development platform.
- Windows remains the desktop operating system.
- Linux becomes the development environment.
- Active development projects should be stored in the Linux file system.

---



## Looking Ahead

The next chapter prepares Windows 11 Professional for WSL by ensuring that the operating system, firmware, and required features are correctly configured before installation begins.