# PowerShell Development Template: Available Anywhere

[← Project Index](./README.md) · [Portfolio](../README.md)

## Summary

This project is a reusable PowerShell Core repository template for engineers who want a consistent, validated development baseline across local workstations, Docker Dev Containers, and GitHub Codespaces.

It shows how I standardize reliable project setup, validation, and AI-assisted maintenance without letting that governance overshadow delivery quality.

Repository:
[david-r-cushman/pwsh-dev-template](https://github.com/david-r-cushman/pwsh-dev-template)

## Problem Space

PowerShell projects often start with inconsistent structure, inconsistent tool availability, and too much dependence on whatever happens to be installed on the host machine.

That creates several avoidable problems:

- new repos take too long to bootstrap
- testing and linting differ across environments
- runtime and tooling versions drift across docs, containers, and CI
- AI-assisted changes can become inconsistent without shared rules and validation boundaries
- developers leak convenience tooling and credentials into places they do not really belong
- project quality depends too heavily on workstation drift

## What I Built

This template establishes a baseline repository structure for PowerShell Core development, including:

- source and test folders
- reusable script, function, module, and test scaffolds
- Pester support
- PSScriptAnalyzer support
- GitHub Actions CI validation
- Markdown and editor configuration
- Docker Dev Container support
- GitHub Codespaces compatibility
- runtime and tooling policy tracked through `eng/runtime-policy.json`
- generated Markdown validation so documented runtime details stay aligned with policy
- AI-assisted development guidance through `AGENTS.md`, Copilot instructions, and supporting governance docs
- downstream AI guidance and ADR scaffold sync for repositories created from the template
- Architecture Decision Records for durable template decisions and workflow boundaries
- repo-local agent skills for guidance sync, runtime policy updates, and template release management
- release/version governance through validation, changelog entries, and GitHub Release guidance
- a template health report for maintainers and agents to inspect the current baseline before deeper work

The template is intentionally opinionated about development hygiene. It supports flexible downstream use, but it starts from a controlled baseline instead of a blank directory.

## Design Priorities

### Portability

The same repo can be worked on locally, inside a Dev Container, or in GitHub Codespaces.

### Trust Boundary Awareness

The project separates host-editor convenience from container execution. That matters when authenticated tools, extensions, or cached credentials are present on the host.

### Clean Starting State

The template provides structure and tooling without pretending to know the business logic of downstream projects.

### Deterministic Validation

Pester, PSScriptAnalyzer, GitHub Actions, version-policy checks, generated Markdown checks, template-version checks, and template-health reporting give the template a repeatable way to detect drift before it becomes project debt.

### Agent-Friendly Maintenance

The template treats agents as workflow coordinators, not as a replacement for engineering judgment. Repo-local skills point agents toward deterministic scripts, Pester coverage, diff review, release validation, and pull requests for repeatable maintenance tasks.

### AI-Assisted Guardrails

The template treats AI as a drafting accelerator rather than an authority. Agent instructions, Copilot guidance, ADRs, validation checks, and review expectations give AI-assisted changes a shared baseline for scope control, verification, and maintainability.

## Why This Project Belongs In The Portfolio

This repo reflects how I think about engineering systems before application logic is even written.

It shows:

- environment design as part of software reliability
- practical security thinking in day-to-day development workflows
- PowerShell engineering beyond one-off scripting
- deterministic validation through Pester, PSScriptAnalyzer, CI, policy checks, and release metadata checks
- ADR-backed workflow boundaries for downstream sync, agent workflows, and release decisions
- AI-assisted development guardrails that can be reused across downstream PowerShell projects
- small, tested maintenance utilities that agents can operate instead of improvising repo changes
- a preference for reusable foundations over repetitive setup work

## Good Fit For

This project is especially relevant to teams working on:

- internal PowerShell tooling
- Azure or Microsoft 365 automation
- endpoint engineering utilities
- AI-assisted scripting workflows that still require reviewable, repeatable controls
- repeatable engineering baselines for small platform teams
- multiple PowerShell repositories that need shared guidance without clobbering project-owned code
