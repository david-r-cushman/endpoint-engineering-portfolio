# David R. Cushman | Endpoint Engineering Portfolio

[Project Index](./projects/README.md) · [Project Selection Criteria](./docs/project-selection.md) · [Portfolio Roadmap](./docs/portfolio-roadmap.md)

![Portfolio Demo](./assets/PortfolioIntro.gif)

## About Me

I build endpoint platforms and engineering foundations for Microsoft environments, with a focus on PowerShell automation, governance, and reliability.

## Reliable. Repeatable. Governable.

This portfolio shows how I approach engineering work that must be reliable in production, repeatable across teams and environments, and governable over time. It brings together reusable PowerShell foundations, applied endpoint work, and the documentation that explains the constraints and decisions behind it.

### Reliable

Engineering should produce systems that are dependable, verifiable, and safe to trust in production.

- if a step is not verified, it is not complete
- automation should reduce operational risk, not simply save time

### Repeatable

Engineering should produce results that remain consistent across operators, environments, and future maintenance.

- reusable engineering foundations should reduce environmental drift
- automation should remain maintainable throughout its lifecycle

### Governable

Engineering should remain understandable, reviewable, and maintainable as systems evolve.

- documentation should preserve engineering intent, not just implementation details
- automation should be guided by standards, validation, and explicit review boundaries

## How To Read This Portfolio

This portfolio is organized around practical engineering investigations in endpoint engineering and automation. Each featured repository explores the technologies, underlying mechanics, abstractions, constraints, and tradeoffs behind an operational problem.

The resulting implementation is intended to demonstrate that understanding rather than stand on its own as the claim. The code matters, but it is only part of the evidence. The documentation, architecture, ADRs, tests, CI, validation, and implementation choices collectively show how I approach engineering work.

Across the portfolio, that work is meant to demonstrate:

- reusable PowerShell engineering foundations for both PowerShell 7 and Windows PowerShell 5.1
- applied endpoint and automation work shaped by real operational constraints
- engineering judgment made visible through documentation, validation, and deliberate implementation decisions
- AI-assisted engineering governed by explicit review, validation, and maintenance boundaries

Rather than collecting every script or experiment, this portfolio focuses on a smaller number of projects that show how I investigate problems, make decisions, and build solutions that are practical, well-documented, and operationally useful.

If you want the quickest read, go straight to [Featured Projects](#featured-projects). Each case study explains the problem, constraints, implementation choices, and engineering signal behind the work.

## How I Use AI

AI is part of my engineering process, but it is not the source of engineering judgment.

I use AI throughout the work of investigating problems, challenging assumptions, comparing alternatives, evaluating tradeoffs, drafting implementations, reviewing code and documentation, validating conclusions, and helping maintain alignment over time.

That matters in a portfolio like this because working code on its own may say very little about the understanding behind it. I want the engineering process to remain visible through the constraints, decisions, validation, and documentation surrounding the implementation.

AI remains one component of a governed engineering process. Human judgment, evidence, review, validation, and accountability remain essential to the result.

## What I Build

I build endpoint and automation solutions for environments where reliability matters, drift is expensive, and change has to be handled deliberately.

The work I am most drawn to sits at the intersection of:

- endpoint engineering at enterprise scale
- automation that reduces operational risk
- platform modernization across on-prem and cloud-connected tooling
- documentation and process design that make systems supportable over time

My approach to engineering was shaped early by work in a role where the margin for error was effectively zero. That experience still informs how I evaluate technical work now.

## Background

My background includes enterprise endpoint engineering in financial services and energy infrastructure, with practical experience in:

- Configuration Manager (ConfigMgr / MECM / SCCM)
- Microsoft Intune and modern endpoint management
- Windows deployment and platform lifecycle engineering
- PowerShell automation
- Active Directory and Group Policy
- Microsoft 365, Azure, and security-aligned platform administration

Professional profile: [LinkedIn](https://www.linkedin.com/in/davidrcushman/).

## Featured Projects

This section is the clearest view of the engineering approach described above.

### Foundations

#### [PowerShell Development Template: Available Anywhere](./projects/pwsh-dev-template.md)

A reusable PowerShell Core repository template with CI validation, Dev Containers, AI guardrails, ADR-backed decisions, downstream guidance sync, repo-local agent workflows, and template health reporting.

Best signal: reusable engineering standards, deterministic validation, and AI-governed maintenance workflows for modern PowerShell work.

Repository:
[pwsh-dev-template](https://github.com/david-r-cushman/pwsh-dev-template)

#### [Windows PowerShell 5.1 Development Template](./projects/powershell-dev-template.md)

A reusable repository template for Windows PowerShell 5.1 projects that need a native Windows development baseline, Windows-hosted CI, and the same testing, analysis, governance, and maintenance discipline as the modern PowerShell template.

Best signal: runtime-aware engineering judgment for legacy and Windows-only PowerShell work without giving up validation discipline.

Repository:
[powershell-dev-template](https://github.com/david-r-cushman/powershell-dev-template)

### Applied Projects

For the fastest view of hands-on implementation work, begin with the projects in this section.

#### [Uninstall-DisplayDrivers](./projects/powershell-driver-management.md)

A PowerShell script built from a real ConfigMgr deployment scenario to remove display driver packages with `devcon.exe`.

Best signal: practical ConfigMgr-oriented scripting shaped by real deployment constraints, safety guardrails, and operational reporting.

Repository:
[powershell-driver-management](https://github.com/david-r-cushman/powershell-driver-management)

#### [WinPE Deployment Lab](./projects/winpe-deployment-lab.md)

A PowerShell-driven WinPE lab for building capture and deployment media while working directly with offline WIM maintenance.

Best signal: hands-on platform depth in Windows imaging and offline servicing, with scoped automation that stays technically honest.

Repository:
[winpe-deployment-lab](https://github.com/david-r-cushman/winpe-deployment-lab)

#### [GPU Cooldown Sleep](./projects/gpu-cooldown-sleep.md)

A PowerShell module that monitors GPU temperature and can put a Windows system to sleep once a target cooldown threshold is reached.

Best signal: disciplined module design that combines hardware telemetry, safe state changes, and testable operational UX.

Repository:
[gpu-cooldown-sleep](https://github.com/david-r-cushman/gpu-cooldown-sleep)

## Explore The Work

For a faster scan, use the links below to jump directly into the project evidence and supporting portfolio context.

- [Portfolio Project Index](./projects/README.md)
- [pwsh-dev-template Case Study](./projects/pwsh-dev-template.md)
- [powershell-dev-template Case Study](./projects/powershell-dev-template.md)
- [powershell-driver-management Case Study](./projects/powershell-driver-management.md)
- [winpe-deployment-lab Case Study](./projects/winpe-deployment-lab.md)
- [gpu-cooldown-sleep Case Study](./projects/gpu-cooldown-sleep.md)
- [Portfolio Roadmap](./docs/portfolio-roadmap.md)

## Usage Notice

This repository is provided for portfolio and evaluation purposes.

See [`NOTICE.md`](./NOTICE.md) for rights and usage details.
