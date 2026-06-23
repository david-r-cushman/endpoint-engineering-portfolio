# Windows PowerShell 5.1 Development Template

[← Project Index](./README.md) · [Portfolio](../README.md)

## Summary

This project is a reusable repository template for Windows PowerShell 5.1 Desktop projects that require a native Windows development and validation baseline.

It complements `pwsh-dev-template` rather than replacing it. The modern template is designed around PowerShell Core, Linux containers, and portability. This template preserves the same engineering discipline for projects that depend on the full .NET Framework, Windows-only modules, or management surfaces that must run under `powershell.exe`.

Repository:
[david-r-cushman/powershell-dev-template](https://github.com/david-r-cushman/powershell-dev-template)

## Problem Space

Windows PowerShell 5.1 remains relevant for endpoint engineering and Microsoft platform work where the supported runtime, module, or API is tied to Windows and the Desktop edition.

Using a modern PowerShell environment as a substitute can hide compatibility problems until deployment. Trying to reproduce Windows PowerShell inside the existing Linux Dev Container model would also create an environment that does not faithfully represent the target runtime.

The template addresses that problem by making the runtime boundary explicit:

- Windows PowerShell 5.1 Desktop is the supported execution environment
- development occurs natively on Windows
- CI validates on a GitHub-hosted Windows runner using `powershell.exe`
- Dev Containers and Codespaces are intentionally excluded rather than replaced with unsupported or high-maintenance infrastructure

## What I Built

The template provides a controlled starting point for Windows PowerShell projects, including:

- source, test, documentation, and reusable scaffold structure
- module manifests that declare PowerShell 5.1 and Desktop-edition compatibility
- Pester 5.7.1 testing and PSScriptAnalyzer 1.25.0 validation
- GitHub Actions CI on `windows-2022` using Windows PowerShell
- centralized runtime and tooling policy through `eng/runtime-policy.json`
- generated documentation checks that keep runtime claims aligned with policy
- AI-assisted development guidance through agent and Copilot instructions
- an Architecture Decision Record documenting the native-Windows runtime boundary
- downstream AI guidance synchronization for repositories created from the template
- repo-local workflows for runtime policy updates, guidance sync, and release management
- template health and version validation for maintainers

The implementation began from the `pwsh-dev-template` baseline and changed only the parts required by the Windows PowerShell runtime and environment model.

## Design Priorities

### Runtime Fidelity

Local development and CI use the same Windows PowerShell edition that downstream projects are expected to support. Compatibility is validated directly instead of inferred from PowerShell Core behavior.

### Minimal Divergence

The repository keeps the structure, scaffolds, validation approach, AI guidance, and maintenance controls of the modern template where they remain compatible. Differences are tied to an explicit Windows PowerShell requirement rather than preference.

### Deterministic Validation

The repository pins its principal testing and analysis tools, explicitly loads the required Pester version instead of Windows' older built-in copy, and checks that CI, editor settings, module manifests, and documentation agree with the runtime policy.

### Honest Environment Boundaries

The template does not claim container or Codespaces support. VS Code Dev Containers does not support Windows container images, and a Linux environment cannot execute the Windows PowerShell 5.1 Desktop contract faithfully.

## Why This Project Belongs In The Portfolio

This project demonstrates that modernization judgment is not simply a matter of moving every workload to the newest runtime.

It shows:

- practical understanding of Windows PowerShell 5.1 and Desktop-edition constraints
- the ability to preserve engineering standards across modern and legacy runtime boundaries
- deliberate tradeoff analysis around containers, hosted development, and native Windows tooling
- deterministic testing, analysis, CI, policy validation, and release controls
- reuse of a proven template architecture without forcing inappropriate environment assumptions
- clear documentation of why the Windows-specific design exists

Together, `pwsh-dev-template` and `powershell-dev-template` show two related engineering baselines: one optimized for modern portability, and one optimized for faithful Windows PowerShell compatibility.

## Good Fit For

This project is especially relevant to teams working on:

- endpoint engineering automation that must run under Windows PowerShell 5.1
- Windows administration modules tied to the Desktop edition or full .NET Framework
- legacy enterprise automation that still requires disciplined testing and maintenance
- gradual modernization programs that need clear runtime boundaries
- internal PowerShell repositories that need shared governance without overstating cross-platform support
