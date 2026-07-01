# Preface

## Purpose of This Handbook

...


# Preface

## Purpose of This Handbook

This handbook documents a complete, repeatable process for building and maintaining a professional web development environment using Windows 11 Professional, the Windows Subsystem for Linux (WSL), Ubuntu Linux, Cursor, GitHub, and a modern JavaScript development stack.

Its purpose extends beyond software installation. It presents a coherent operating environment designed for reliability, maintainability, and long-term productivity. Every recommendation reflects practical experience and a preference for proven, stable technologies over unnecessary complexity.

The handbook is intended to serve both as an installation guide and as an operational reference. It explains not only *how* to configure the environment, but also *why* particular design decisions have been made.

---

## Intended Audience

This handbook is written for developers who choose Windows as their primary desktop operating system while using Linux as their development environment.

Although it assumes little prior experience with Linux, it is written with professional standards in mind. Readers are expected to value careful planning, clear documentation, reproducible systems, and disciplined development practices.

---

## Design Philosophy

Several principles guide every recommendation in this handbook.

### Reliability

A development environment should be dependable. New tools are adopted only when they provide clear and lasting advantages.

### Simplicity

Complexity should be introduced only when it produces measurable benefits. The simplest solution that accomplishes the objective is usually the preferred solution.

### Repeatability

Every development machine should be capable of being rebuilt from this handbook. Configuration should never depend upon undocumented steps or memory.

### Documentation

Important decisions should be recorded. Good documentation reduces mistakes, simplifies maintenance, and shortens recovery time after hardware failures or system rebuilds.

---

## Our Operating Model

Throughout this handbook, Windows and Linux serve different but complementary roles.

**Windows** functions as the workstation. It provides the desktop environment and productivity applications, including Cursor, Microsoft 365, web browsers, communication tools, and device management.

**Linux** functions as the workshop. It hosts source code, development tools, package managers, local servers, and the software required to build, test, and maintain web applications.

Keeping these responsibilities distinct results in a cleaner, more stable development environment.

---

## Scope

The handbook covers the complete lifecycle of a professional WSL development environment, including:

- Preparing Windows 11 Professional
- Installing and configuring WSL
- Installing Ubuntu LTS
- Configuring Linux for development
- Installing Git, Node.js, npm, and related tools
- Using Cursor with WSL
- Organizing development projects
- Daily development workflow
- Backup and recovery procedures
- Troubleshooting common problems
- Long-term maintenance

Future editions may include additional chapters covering Docker, Dev Containers, cloud development, artificial intelligence coding assistants, and related technologies.

---

## A Living Handbook

Technology evolves continually. Rather than treating this handbook as a static document, it should be maintained as a living reference that reflects current best practices, revised workflows, and lessons learned through experience.

The objective is to preserve a dependable, professional development environment that can be reproduced consistently across future computers while remaining adaptable as development tools evolve.