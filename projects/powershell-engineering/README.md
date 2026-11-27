# PowerShell Engineering

[← Portfolio](../../README.md) · [Project Selection Criteria](../../docs/project-selection.md) · [Portfolio Roadmap](../../docs/portfolio-roadmap.md)

## Investigation Context

This investigation examines what it takes to develop and maintain reliable PowerShell solutions throughout their lifecycle. It treats PowerShell engineering as more than producing a functional script: development environments, runtime fidelity, design, validation, operational safety, documentation, and maintenance all affect whether automation remains useful over time.

The two development templates are related outcomes of this investigation, not mandatory foundations for future work. Individual projects may use different foundations when their requirements call for them.

## Engineering Focus

- development environments that reduce drift while respecting runtime constraints
- scripts, functions, modules, interfaces, and structured output designed for maintainability
- validation through Pester, PSScriptAnalyzer, and continuous integration
- guardrails and controlled state changes for operational automation
- documentation, durable decisions, and AI-assisted engineering boundaries
- lifecycle tradeoffs between standardization, flexibility, and maintenance cost

## Reusable Engineering Foundations

| Repository | Purpose |
|---|---|
| [pwsh-dev-template](./pwsh-dev-template.md) | Portable PowerShell Core development baseline with validation and governed maintenance workflows. |
| [powershell-dev-template](./powershell-dev-template.md) | Native Windows PowerShell 5.1 baseline that preserves validation discipline while prioritizing runtime fidelity. |

`powershell-dev-template` began from the `pwsh-dev-template` baseline and adapts it for the Windows PowerShell 5.1 runtime and native Windows environment.

## Applied Engineering Projects

| Project | Problem or objective | Engineering signal |
|---|---|---|
| [Uninstall-DisplayDrivers](./powershell-driver-management.md) | Remove display driver packages that interfere with Windows upgrades. | ConfigMgr-aware endpoint remediation, operational reporting, guardrails, and safe system changes. |
| [WinPE Deployment Lab](./winpe-deployment-lab.md) | Explore deployment mechanics abstracted by higher-level platforms. | Windows imaging, WinPE, offline servicing, and deployment automation. |
| [GPU Cooldown Sleep](./gpu-cooldown-sleep.md) | Safely transition a workstation to sleep after GPU cooldown. | Module design, provider abstraction, telemetry, testability, and operational safety. |

## Outcomes and Tradeoffs

Reusable foundations can improve consistency and make validation easier to repeat, but their controls must remain proportional to the operational problem. Runtime-specific validation matters: a portable PowerShell Core environment and a Windows PowerShell 5.1 environment have different fidelity requirements.

AI guidance can make assistance more consistent and reviewable, but it does not replace correctness verification or engineering accountability. The investigation therefore treats templates, tests, analysis, documentation, and review as complementary controls rather than proof that every solution needs the same architecture.

## Explore the Case Studies

- [PowerShell Development Template: Available Anywhere](./pwsh-dev-template.md)
- [Windows PowerShell 5.1 Development Template](./powershell-dev-template.md)
- [Uninstall-DisplayDrivers](./powershell-driver-management.md)
- [WinPE Deployment Lab](./winpe-deployment-lab.md)
- [GPU Cooldown Sleep](./gpu-cooldown-sleep.md)
