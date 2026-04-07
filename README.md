# David R. Cushman | Endpoint Engineering Portfolio

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

The work I am most drawn to usually sits at the intersection of:

- endpoint engineering at enterprise scale
- automation that reduces operational risk
- platform modernization across on-prem and cloud-connected tooling
- documentation and process design that make systems supportable over time

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

## Why This Portfolio Exists

This repository is meant to make it easier for recruiters, hiring managers, and technical peers to quickly understand how I work.

Rather than collecting every script or experiment, I want this portfolio to highlight a smaller number of projects that clearly show:

- the problem being solved
- the operational constraints involved
- the engineering decisions behind the implementation
- the reliability and maintainability thinking behind the result

## Explore The Work

- [Portfolio Project Index](./projects/README.md)
- [pwsh-dev-template Case Study](./projects/pwsh-dev-template.md)
- [powershell-driver-management Case Study](./projects/powershell-driver-management.md)
- [Portfolio Roadmap](./docs/portfolio-roadmap.md)
