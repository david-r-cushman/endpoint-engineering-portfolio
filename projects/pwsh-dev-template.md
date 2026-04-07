# PowerShell 7.4 Template: Available Anywhere

## Summary

This project is a reusable PowerShell repository template for engineers who want a consistent development baseline across local workstations, Docker Dev Containers, and GitHub Codespaces.

It was designed to remove a common source of friction in PowerShell work: rebuilding the same repo structure, tooling, and development environment every time a new project starts.

Repository:
[david-r-cushman/pwsh-dev-template](https://github.com/david-r-cushman/pwsh-dev-template)

## Problem Space

PowerShell projects often start with inconsistent structure, inconsistent tool availability, and too much dependence on whatever happens to be installed on the host machine.

That creates several avoidable problems:

- new repos take too long to bootstrap
- testing and linting differ across environments
- developers leak convenience tooling and credentials into places they do not really belong
- project quality depends too heavily on workstation drift

## What I Built

This template establishes a baseline repository structure for PowerShell 7.4 development, including:

- source and test folders
- Pester support
- PSScriptAnalyzer support
- Markdown and editor configuration
- Docker Dev Container support
- GitHub Codespaces compatibility

The template is intentionally opinionated about development hygiene. It supports flexible downstream use, but it starts from a controlled baseline instead of a blank directory.

## Design Priorities

### Portability

The same repo can be worked on locally, inside a Dev Container, or in GitHub Codespaces.

### Trust Boundary Awareness

The project separates host-editor convenience from container execution. That matters when authenticated tools, extensions, or cached credentials are present on the host.

### Clean Starting State

The template provides structure and tooling without pretending to know the business logic of downstream projects.

### Operational Discipline

Linting, testing, and repo conventions are treated as part of the engineering surface, not optional cleanup for later.

## Why This Project Belongs In The Portfolio

This repo reflects how I think about engineering systems before application logic is even written.

It shows:

- environment design as part of software reliability
- practical security thinking in day-to-day development workflows
- PowerShell engineering beyond one-off scripting
- a preference for reusable foundations over repetitive setup work

## Good Fit For

This project is especially relevant to teams working on:

- internal PowerShell tooling
- Azure or Microsoft 365 automation
- endpoint engineering utilities
- repeatable engineering baselines for small platform teams
