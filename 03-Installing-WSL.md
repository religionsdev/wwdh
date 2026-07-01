# Chapter 3: Installing WSL

## Introduction

With Windows properly prepared, the next step is to install the Windows Subsystem for Linux (WSL). WSL provides a Linux environment that runs alongside Windows, allowing modern web development tools to operate as they would on a native Linux computer.

This chapter installs WSL, enables the required Windows features, and installs Ubuntu LTS.

---

## Before You Begin

Verify that:

- Windows 11 Professional is fully updated.
- Hardware virtualization is enabled.
- You are connected to a reliable Internet connection.
- You have administrator privileges on the computer.

---



## Step 1: Open an Administrator Terminal

1. Click **Start**.
2. Type **Windows Terminal**.
3. Right-click **Windows Terminal**.
4. Select **Run as administrator**.

Administrator privileges are required because Windows must enable system features during installation.

---



## Step 2: Install WSL

Run the following command:

```powershell
wsl --install
```

This command performs several tasks:

- Enables the Windows Subsystem for Linux feature.
- Enables the Virtual Machine Platform feature.
- Installs the Linux kernel.
- Sets WSL 2 as the default version.
- Downloads Ubuntu.

Depending on your Internet connection, this process may take several minutes.

---



## Step 3: Restart Windows

When prompted, restart the computer.

Do not skip this step.

Many installation problems occur because Windows features are not fully enabled until after a restart.

---



## Step 4: Complete Ubuntu Installation

After Windows restarts, Ubuntu should launch automatically.

The first launch performs the initial Linux configuration.

You will be asked to create:

- A Linux username
- A Linux password

These credentials are separate from your Windows account.

The password will not be displayed while you type. This is normal Linux behavior.

---



## Step 5: Verify the Installation

Open Windows Terminal and run:

```powershell
wsl --status
```

Then run:

```powershell
wsl --list --verbose
```

You should see Ubuntu listed and using WSL version 2.

---



## Understanding the Components

A successful installation consists of four major components:

### Windows

Provides the desktop operating system.

### WSL

Provides the compatibility layer that allows Linux to run.

### Ubuntu

Provides the Linux operating system.

### Windows Terminal

Provides the primary interface for interacting with Linux.

Each component serves a different purpose.

---



## Common Installation Problems



### Ubuntu does not start

Restart Windows and try again.

---



### WSL reports that no distributions are installed

Run the installation command again.

---



### Installation stops unexpectedly

Verify that:

- Windows Update has completed.
- Internet access is working.
- Administrator privileges were used.

---



### Virtualization errors

Check that hardware virtualization is enabled in the BIOS or UEFI firmware.

---



## Best Practices

- Install only one Linux distribution initially.
- Use Ubuntu LTS.
- Do not interrupt the installation.
- Restart whenever Windows requests it.
- Verify the installation before installing development tools.

---



## Chapter Checklist

Before continuing, confirm that:

- WSL is installed.
- Ubuntu launches successfully.
- A Linux username has been created.
- A Linux password has been created.
- `wsl --status` reports a healthy installation.
- Ubuntu is using WSL version 2.

Once these items are complete, you are ready to configure Ubuntu for development.

---



## Looking Ahead

The next chapter introduces Ubuntu, explains the Linux file system, and performs the initial configuration needed before installing development tools.