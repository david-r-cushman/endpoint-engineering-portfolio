# WinPE Deployment Lab

## Summary

This project is a PowerShell-driven WinPE lab for building capture and deployment media and performing offline WIM maintenance from a repository-local workflow.

It exists to demonstrate hands-on understanding of the Windows imaging mechanics that products like ConfigMgr and MDT often abstract away.

Repository:
[david-r-cushman/winpe-deployment-lab](https://github.com/david-r-cushman/winpe-deployment-lab)

## Problem Space

Modern deployment platforms are powerful, but they can also hide the underlying mechanics of WinPE boot media, WIM capture, offline servicing, and unattended deployment.

For endpoint engineering, that underlying knowledge still matters.

There are practical scenarios where understanding the lower layers is valuable:

- lab and test VM provisioning
- image troubleshooting and validation
- offline WIM servicing
- environments where a lightweight local workflow is more appropriate than standing up a full deployment platform

## What I Built

The repository acts as its own workspace and provides a PowerShell-based workflow for:

- initializing a repo-local build structure
- generating WinPE capture media
- generating WinPE deployment media
- maintaining a captured WIM offline

The project uses checked-in configuration, payload templates, and public script entry points while keeping runtime artifacts local to the repository.

It also adds PowerShell support to the WinPE runtime so the capture and deployment logic can run in PowerShell rather than relying primarily on batch scripts.

## Design Priorities

### Understanding The Underlying Mechanics

This project is intentionally closer to WinPE, DISM, WIM, and unattended deployment behavior than higher-level deployment products usually require.

### Honest Scope

This is presented as a lab project for local virtual machine deployment and image work, not as a claim that enterprise endpoint teams should replace ConfigMgr, MDT, or modern deployment tooling with custom WinPE media.

### Repo-As-Workspace Simplicity

The repository itself acts as the working area, which keeps configuration, source, logs, ISO output, and WIM artifacts easier to reason about.

### PowerShell-First Automation

Using PowerShell inside the WinPE workflow makes the runtime logic easier to maintain, debug, and extend than a purely batch-driven approach.

## Why This Project Belongs In The Portfolio

This project adds a different kind of signal than the other portfolio entries.

It shows:

- endpoint engineering depth below the management-layer tooling
- practical familiarity with Windows imaging internals
- PowerShell-based automation in a deployment-focused lab scenario
- the judgment to keep a technically interesting project scoped honestly

## What It Demonstrates

- WinPE media creation and customization
- offline WIM servicing
- unattended deployment workflow awareness
- PowerShell-based orchestration of classic deployment mechanics
