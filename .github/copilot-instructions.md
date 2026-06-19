# Copilot Instructions

## Repository Purpose

This repository is a public endpoint engineering portfolio. It is intended for recruiters, hiring managers, and technical peers who need to understand the author's engineering judgment, project focus, and PowerShell-centered work quickly.

Keep the portfolio clean, simple, and easy for humans to navigate. The root `README.md` is the primary landing page and should remain reader-facing, not process-heavy.

## Documentation Standards

When updating this repository:

- preserve the root `README.md` as a concise recruiter and hiring-manager landing page
- keep project pages human-readable, technically honest, and free of unnecessary implementation noise
- align portfolio claims with the referenced project repositories before strengthening wording
- prefer small documentation changes with clear diffs and focused pull requests
- avoid turning the portfolio into a changelog, release tracker, or mirror of project READMEs

## Project Alignment

Use `docs/project-alignment.md` when adding or updating portfolio project pages.

Project pages should summarize why a project exists, what problem it addresses, what was built, and what it demonstrates. They should not overclaim maturity, production use, scope, or business impact beyond what the referenced repository supports.

If a referenced project changes substantially, update only the portfolio sections that help a reader understand the current project value. Do not add reader-facing maintenance process unless it improves navigation or comprehension.

## AI Governance

AI assistance may be used to draft and refine portfolio documentation, but final content must remain accurate, restrained, and reviewable.

Do not add repo-local skills, validation scripts, CI workflows, badges, or heavier governance unless a repeated maintenance problem makes that complexity worthwhile. If such a need appears, propose it first as a small, explicit plan.
