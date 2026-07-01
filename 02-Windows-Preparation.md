# Chapter 2: Preparing Windows 11 Professional

## Introduction

A reliable WSL environment begins with a properly configured Windows installation. Before installing WSL or Ubuntu, Windows itself should be fully updated and configured. Taking the time to prepare Windows reduces installation problems and provides a stable foundation for future development work.

This chapter establishes the baseline configuration for every development computer.

---

## System Requirements

The development workstation should meet or exceed the following specifications.

### Minimum

- Windows 11 Professional (64-bit)
- Quad-core processor
- 16 GB RAM
- 250 GB SSD
- Reliable internet connection



### Recommended

- Windows 11 Professional
- Modern Intel Core Ultra or AMD Ryzen processor
- 32 GB RAM or more
- 1 TB NVMe SSD or larger
- Hardware virtualization enabled
- Wired or reliable Wi-Fi network

---



## Complete Windows Setup

Before installing development software:

- Activate Windows.
- Sign in with your Microsoft account.
- Connect OneDrive.
- Install all available Windows Updates.
- Restart whenever prompted.
- Continue checking for updates until none remain.

Do not install development tools until Windows Update is completely finished.

---



## Verify Device Drivers

Open **Device Manager** and verify that no devices display warning symbols.

Pay particular attention to:

- Network adapter
- Graphics adapter
- Bluetooth
- Audio devices
- Storage controller

Resolve any driver issues before proceeding.

---



## Enable Hardware Virtualization

WSL 2 requires hardware virtualization.

Most computers have virtualization enabled by default. If it has been disabled in the BIOS or UEFI firmware, WSL may not function correctly.

To verify:

1. Open **Task Manager**.
2. Select the **Performance** tab.
3. Choose **CPU**.
4. Confirm that **Virtualization** is listed as **Enabled**.

If virtualization is disabled, enable Intel VT-x or AMD-V in the computer's BIOS or UEFI settings before continuing.

---



## Install Windows Terminal

Windows Terminal provides a modern interface for PowerShell, Command Prompt, and WSL.

If it is not already installed, install it from the Microsoft Store.

Windows Terminal will become the primary command-line application used throughout this handbook.

---



## Security Considerations

Windows Security should remain enabled.

Recommended settings include:

- Microsoft Defender Antivirus
- SmartScreen
- Windows Firewall
- BitLocker (if appropriate for your workflow)

Avoid disabling security features simply to make software installation easier.

---



## Create a Restore Point

Before installing development software, create a Windows restore point.

Although WSL installations are generally reliable, a restore point provides an additional layer of protection if unexpected problems occur.

---



## Development Philosophy

This handbook follows a simple principle:

- Configure Windows first.
- Verify Windows is stable.
- Install WSL.
- Install Ubuntu.
- Install development tools.
- Begin development.

Skipping steps often creates problems that are more difficult to diagnose later.

---



## Chapter Checklist

Before continuing, confirm the following:

- Windows 11 Professional is activated.
- All Windows Updates have been installed.
- No Device Manager warnings are present.
- Hardware virtualization is enabled.
- Windows Terminal is installed.
- A restore point has been created.
- Internet connectivity is stable.

Once every item has been completed, the computer is ready for WSL installation.

---



## Looking Ahead

The next chapter installs the Windows Subsystem for Linux (WSL), explains the required Windows features, and walks through installing Ubuntu LTS as the development environment.