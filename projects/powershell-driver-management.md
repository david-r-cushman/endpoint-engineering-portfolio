# Uninstall-DisplayDrivers

[← Project Index](./README.md) · [Portfolio](../README.md)

## Summary

`Uninstall-DisplayDrivers.ps1` is a PowerShell operational script built to remove display driver packages by using `devcon.exe`.

This is one of the clearest examples in the portfolio of hands-on endpoint scripting shaped by a real deployment constraint rather than a hypothetical exercise.

Repository:
[david-r-cushman/powershell-driver-management](https://github.com/david-r-cushman/powershell-driver-management)

## Problem Space

In-place Windows upgrades were being blocked by legacy display drivers.

Removing the device alone was not enough, because the associated driver package could remain in the driver store and be reinstalled later. The real challenge was reliable driver-package removal without already knowing the exact `oem*.inf` name in advance.

That constraint shaped the solution.

## What I Built

The script uses `devcon.exe` to:

- enumerate display-class devices
- extract matching hardware IDs
- remove the associated display driver packages

It remains intentionally aligned to ConfigMgr Scripts deployment, including explicit process exit codes that can be surfaced operationally by the client.

## Design Priorities

### Fidelity To The Original Use Case

The deployable artifact remains a single PowerShell script because that matches how the solution is consumed operationally.

### Testability Without Losing Practical Shape

Although the deployment form is a single script, the internal structure supports Pester-based testing by isolating logic into testable helper functions and mocking `devcon.exe` interactions.

### Guardrails

The script checks for:

- elevated execution context
- the presence of `devcon.exe`
- virtual machine scenarios where execution should not proceed
- `ShouldProcess` support for safer review with `-WhatIf`

### Operational Reporting

Explicit exit codes make the script more useful in managed deployment contexts where success and failure need to be reported clearly.

## Why This Project Belongs In The Portfolio

This project represents the kind of applied work I care most about:

- solving a real enterprise problem
- respecting deployment reality instead of rewriting for aesthetics
- improving maintainability and testability without losing operational fit
- treating reliability and safety as first-class requirements

## What It Demonstrates

- PowerShell automation rooted in actual endpoint operations
- ConfigMgr-aware script design
- disciplined handling of high-consequence system changes
- engineering judgment around when to preserve original deployment shape
