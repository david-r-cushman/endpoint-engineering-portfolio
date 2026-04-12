# GPU Cooldown Sleep

[← Project Index](./README.md) · [Portfolio](../README.md)

## Summary

`gpu-cooldown-sleep` is a PowerShell module that monitors GPU temperature and can put a Windows system to sleep once a target cooldown threshold is reached.

It began as a practical personal-workstation need and evolved into a clean, testable PowerShell module with strong safety and a provider model intended for future expansion beyond a single GPU vendor.

Repository:
[david-r-cushman/gpu-cooldown-sleep](https://github.com/david-r-cushman/gpu-cooldown-sleep)

## Problem Space

High-performance GPUs can stay hot after sustained load, even when active work is done.

On a personal workstation, that creates a simple but real operational problem: if the system goes to sleep too early, the cooling fans stop while the GPU may still be carrying significant residual heat. The goal is to let the system remain awake long enough for the GPU to cool to an acceptable temperature, then transition to sleep deliberately.

This project turns that into an automation workflow that is:

- explicit about which device is being monitored
- safe to review with `-WhatIf`
- suitable for repeatable use rather than one-off scripting

## What I Built

The module provides commands to:

- discover supported GPU devices
- read GPU temperature through a provider implementation
- wait until a target temperature is reached (with optional progress)
- request system sleep once cooldown is complete (with `ShouldProcess` guardrails)

It returns structured objects rather than relying on console-only output, and it includes Pester tests with mocks so the logic can be validated without requiring real hardware state changes during test runs.

## Design Priorities

### Safety And Reviewability

Putting a system to sleep is a state-changing action, so the entry point is built around `SupportsShouldProcess` and `-WhatIf` behavior.

### Provider Model For Growth

The implementation starts with an NVIDIA-first provider, but the module structure is designed to make it straightforward to add additional GPU telemetry providers over time.

### Good Operational UX

The command surface supports stable automation selection (for scheduled tasks) and friendly interactive selection, including argument completion for device names.

### Testability

The module uses a design that is mock-friendly in Pester so that timing, device discovery, and telemetry calls can be tested deterministically.

## Why This Project Belongs In The Portfolio

This repo is not about building a business application. It is about showing how I approach operational automation:

- define a small, real problem clearly
- build a safe, testable contract around it
- design for maintainability and future expansion
- keep the output structured so the tool can be composed into larger workflows

## What It Demonstrates

- PowerShell module design with a clean public command surface
- provider-style abstraction for hardware telemetry
- `ShouldProcess` discipline around system-impacting actions
- Pester-based testing with mocks for safe validation
