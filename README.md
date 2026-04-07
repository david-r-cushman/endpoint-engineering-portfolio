# David R. Cushman | Endpoint Engineering Portfolio

This repository is the landing pad for my GitHub portfolio.

It brings together the work, documentation style, and engineering approach behind my PowerShell and endpoint-management projects, with a focus on automation, operational reliability, and disciplined change control.

My background is in enterprise endpoint engineering across financial services and energy infrastructure, with hands-on experience in:

- Microsoft Configuration Manager (ConfigMgr / MECM / SCCM)
- Microsoft Intune and modern endpoint management
- Windows deployment and platform lifecycle work
- PowerShell automation
- Active Directory and Group Policy
- Microsoft 365, Azure, and security-adjacent platform administration

## Engineering Point Of View

Most IT teams talk about reliability as a quality target. I tend to think about it as an operational obligation.

Before endpoint engineering, I worked in an environment where the margin for error was effectively zero. That experience shaped how I approach systems work today:

- if a step is not verified, it is not complete
- good automation reduces risk, not just effort
- maintainability matters because operational tools usually outlive their first use case
- documentation should preserve intent, not just syntax

That mindset shows up throughout the projects in this portfolio. I care about practical outcomes, predictable behavior, and solutions that can stand up to real operational pressure.

## Featured Projects

### [PowerShell 7.4 Template: Available Anywhere](./projects/pwsh-dev-template.md)

A reusable development baseline for PowerShell repositories with support for local development, Docker Dev Containers, and GitHub Codespaces.

Why it matters:

- creates a consistent, portable engineering environment
- separates host tooling from in-container execution
- establishes linting, test, and structure conventions from the start

Repository:
[pwsh-dev-template](https://github.com/david-r-cushman/pwsh-dev-template)

### [Uninstall-DisplayDrivers](./projects/powershell-driver-management.md)

A PowerShell script built from a real ConfigMgr deployment scenario to remove display driver packages by using `devcon.exe`.

Why it matters:

- solves a specific operational blocker from an enterprise Windows upgrade effort
- preserves ConfigMgr deployment fit while improving testability
- uses explicit safeguards and exit codes for operational reporting

Repository:
[powershell-driver-management](https://github.com/david-r-cushman/powershell-driver-management)

## Portfolio Structure

- [`projects/`](./projects/)
  Project summaries and portfolio-facing case-study pages
- [`docs/portfolio-roadmap.md`](./docs/portfolio-roadmap.md)
  Notes on where this portfolio can expand next
- [`docs/project-selection.md`](./docs/project-selection.md)
  Framing for the kinds of work this portfolio is intended to highlight

## What This Repository Will Become

This repo is intended to grow into the main public-facing entry point for my work.

That includes:

- curated project summaries
- deeper case studies with problem, constraints, and design decisions
- links to source repositories
- supporting materials for recruiters, hiring managers, and technical peers who want a faster way to understand how I think and build

## Current Focus

The first phase of this portfolio centers on endpoint engineering and PowerShell-driven operational tooling.

The immediate goal is not to collect every script or experiment. It is to present a small number of projects clearly, with enough context to show:

- the problem being solved
- the operational environment or constraint
- the engineering decisions involved
- the reliability and maintainability considerations behind the implementation

## Project Navigation

- [Portfolio Project Index](./projects/README.md)
- [pwsh-dev-template Case Study](./projects/pwsh-dev-template.md)
- [powershell-driver-management Case Study](./projects/powershell-driver-management.md)
