# David R. Cushman | Endpoint Engineering Portfolio

[Project Index](./projects/README.md) · [Project Selection Criteria](./docs/project-selection.md) · [Portfolio Roadmap](./docs/portfolio-roadmap.md)

![Portfolio Demo](./.assets/PortfolioIntro.gif)

## Introduction

Senior Endpoint Engineer focused on automation, platform reliability, and disciplined change management across enterprise environments.

This repository is the public landing pad for my portfolio work. It brings together the engineering approach, project documentation, and PowerShell-driven tooling behind my work in endpoint management and Microsoft platform administration.

My background includes enterprise endpoint engineering in financial services and energy infrastructure, with practical experience in:

- Configuration Manager (ConfigMgr / MECM / SCCM)
- Microsoft Intune and modern endpoint management
- Windows deployment and platform lifecycle engineering
- PowerShell automation
- Active Directory and Group Policy
- Microsoft 365, Azure, and security-aligned platform administration

## What I Bring

I build endpoint and automation solutions for environments where reliability matters, operational drift is expensive, and change has to be handled deliberately.

The work I am most drawn to sits at the intersection of:

- endpoint engineering at enterprise scale
- automation that reduces operational risk
- platform modernization across on-prem and cloud-connected tooling
- documentation and process design that make systems supportable over time

I also apply a structured, AI-assisted development approach as part of that same focus on consistency and maintainability. AI is used as a drafting accelerator, while constraints, scope boundaries, and review practices ensure that the final result remains aligned with real-world operational needs rather than over-engineered or purely theoretical solutions.

## Engineering Mindset

My approach to engineering was shaped early by work in a role where the margin for error was effectively zero. That experience still informs how I design and evaluate technical work now:

- if a step is not verified, it is not complete
- automation should reduce risk, not just save time
- operational tooling should be maintainable long after the first deployment
- clear documentation preserves engineering intent, not just implementation detail

I care about solutions that behave predictably, hold up under pressure, and remain useful to the people who inherit them.

## Featured Projects

### [PowerShell 7.4 Template: Available Anywhere](./projects/pwsh-dev-template.md)

A reusable PowerShell development baseline designed for local workstations, Docker Dev Containers, and GitHub Codespaces.

What it demonstrates:

- consistent engineering setup across development environments
- thoughtful separation between host tooling and in-container execution
- a reusable foundation for secure, testable PowerShell work

Repository:
[pwsh-dev-template](https://github.com/david-r-cushman/pwsh-dev-template)

### [Uninstall-DisplayDrivers](./projects/powershell-driver-management.md)

A PowerShell script built from a real ConfigMgr deployment scenario to remove display driver packages with `devcon.exe`.

What it demonstrates:

- practical problem-solving rooted in an enterprise endpoint use case
- preserving deployment fit while improving structure and testability
- safety guardrails and explicit operational reporting through exit codes

Repository:
[powershell-driver-management](https://github.com/david-r-cushman/powershell-driver-management)

### [WinPE Deployment Lab](./projects/winpe-deployment-lab.md)

A PowerShell-driven WinPE lab for building capture and deployment media and working directly with offline WIM maintenance.

What it demonstrates:

- hands-on understanding of WinPE and Windows imaging mechanics beyond ConfigMgr and MDT abstractions
- PowerShell-based automation for capture media, deployment media, and offline servicing workflows
- intentional scoping of a lab solution for local VM deployment rather than overstating it as enterprise imaging

Repository:
[winpe-deployment-lab](https://github.com/david-r-cushman/winpe-deployment-lab)

### [GPU Cooldown Sleep](./projects/gpu-cooldown-sleep.md)

A PowerShell module that monitors GPU temperature and can put a Windows system to sleep once a target cooldown threshold is reached.

What it demonstrates:

- hardware telemetry integration with a provider model designed for future expansion
- safe, reviewable power-state changes via `ShouldProcess` and `-WhatIf`
- operational UX: device selection, argument completion, and testable behavior

Repository:
[gpu-cooldown-sleep](https://github.com/david-r-cushman/gpu-cooldown-sleep)

## Why This Portfolio Exists

This repository is meant to make it easier for recruiters, hiring managers, and technical peers to quickly understand how I work.

Rather than collecting every script or experiment, I want this portfolio to highlight a smaller number of projects that clearly show:

- the problem being solved
- the operational constraints involved
- the engineering decisions and constraintsbehind the implementation
- the reliability and maintainability thinking behind the result

## Explore The Work

- [Portfolio Project Index](./projects/README.md)
- [pwsh-dev-template Case Study](./projects/pwsh-dev-template.md)
- [powershell-driver-management Case Study](./projects/powershell-driver-management.md)
- [winpe-deployment-lab Case Study](./projects/winpe-deployment-lab.md)
- [gpu-cooldown-sleep Case Study](./projects/gpu-cooldown-sleep.md)
- [Portfolio Roadmap](./docs/portfolio-roadmap.md)

## Usage Notice

This repository is provided for portfolio and evaluation purposes.

See [`NOTICE.md`](./NOTICE.md) for rights and usage details.
