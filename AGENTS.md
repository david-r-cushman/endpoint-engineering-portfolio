# AGENTS.md

## Repository Instructions

This repository's primary AI guidance is maintained in:

```text
.github/copilot-instructions.md
```

Before performing documentation, review, automation, or repository-maintenance work, coding agents must read and follow `.github/copilot-instructions.md`.

That file is the authoritative instruction source for:

- portfolio writing standards
- project alignment expectations
- reader-first documentation boundaries
- AI-assisted maintenance guidance

If `.github/copilot-instructions.md` is missing or unavailable, stop and report that the repository guidance cannot be loaded rather than guessing.

If guidance in this file conflicts with `.github/copilot-instructions.md`, `.github/copilot-instructions.md` is authoritative.

## Portfolio Architecture

The portfolio is organized around engineering investigations. Maintain this
layout unless an approved restructuring explicitly changes it:

```text
README.md                                # Reader-facing portfolio landing page
projects/<investigation>/README.md       # Investigation context and navigation
projects/<investigation>/<project>.md    # Optional project-specific case study
docs/project-selection.md                # Inclusion and curation criteria
docs/project-alignment.md                # Portfolio maintenance and accuracy boundaries
docs/portfolio-roadmap.md                # Future portfolio development
assets/                                  # Reader-facing visual assets
```

The root README catalogues investigations, not every individual project. An
investigation README owns the relationship between its artifacts and any case
studies. A project case study is optional: add one only when project-specific
context provides reader value beyond the investigation landing page.

## Adding, Updating, and Removing Portfolio Entries

After reading the authoritative Copilot guidance, read
`docs/project-alignment.md` before changing portfolio content.

- To add an investigation, create its directory and landing page, then add one
  concise entry to the root README.
- To add a project to an existing investigation, update its landing page and
  add a case study only when justified. Do not ordinarily change the root
  README.
- To remove a project or investigation, remove its navigation, associated
  case study or landing page, and affected links. Do not retain a redundant
  inventory solely for historical convenience.
- Verify relationships between templates and implementations from repository
  evidence; never infer lineage from naming or similar tooling.
- Keep claims proportionate and technically honest, distinguishing production
  experience, recreations, personal tooling, labs, and reference
  implementations.

Before handoff, check Markdown paths and anchors affected by the change. Do
not add automation or validation infrastructure solely for a one-time
documentation update.
