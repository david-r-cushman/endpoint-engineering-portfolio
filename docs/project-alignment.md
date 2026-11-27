# Portfolio Maintenance Guide

[← Portfolio](../README.md) · [Project Selection Criteria](./project-selection.md) · [Portfolio Roadmap](./portfolio-roadmap.md)

This guide helps maintainers and AI agents keep the portfolio aligned with the repositories it references without adding clutter for readers.

The portfolio is a summary layer. It should explain value, constraints, and engineering signal; it should not copy implementation READMEs, track every release, or make claims unsupported by the referenced repository.

## Document Responsibilities

| Document | Primary responsibility |
|---|---|
| Root README | Professional introduction and catalogue of engineering investigations. |
| Investigation README | Context, objectives, artifact relationships, outcomes, and navigation. |
| Project case study | Project-specific problem, constraints, implementation, and engineering significance. |
| Project selection criteria | Inclusion and continued-inclusion criteria. |
| This guide | Maintenance and accuracy boundaries. |
| Portfolio roadmap | Future portfolio development. |
| Implementation repository README | Technical implementation, usage, and repository-specific documentation. |

Each document should add useful context rather than repeat its parent or child document.

## When To Update

Update an investigation landing page when its body of work, artifact relationships, or reader-facing engineering outcome changes materially. Update a case study when a project changes what it is, why it exists, what it demonstrates, or the audience it serves.

Do not update the portfolio for every routine commit. Small fixes, internal refactors, dependency updates, and release housekeeping do not usually change the reader-facing story.

Update the root README only when the portfolio-level narrative or investigation catalogue changes. Update the selection criteria or this guide only when their respective policies change.

## Adding and Removing Work

To add an investigation, add its landing page and one concise root-README entry. An investigation may contain one implementation repository, multiple related repositories, or no individual case studies when a landing page fully explains the evidence.

To add a project to an existing investigation, update that investigation's navigation and add a case study only when project-specific context adds reader value. To remove a project, remove its investigation entry, its case study if present, and affected references. Do not ordinarily edit the root README for either operation.

To remove an investigation, remove its root-README entry, its landing page, associated case studies, and affected references.

## Accuracy Boundaries

When updating portfolio documentation:

- do not overstate production readiness, adoption, uniqueness, or business impact
- distinguish production experience, recreated solutions, personal tooling, technical investigations, labs, and reference implementations
- verify template relationships before documenting them; do not infer lineage from similar structure or tooling
- summarize durable reader-facing meaning instead of copying ADRs, process details, or implementation README content
- do not add scripts, skills, CI, badges, or automation unless a repeated maintenance problem justifies it
