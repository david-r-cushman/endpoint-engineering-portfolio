# Project Alignment Guide

[← Portfolio](../README.md) · [Projects](../projects/README.md) · [Project Selection Criteria](./project-selection.md)

This guide helps maintainers and AI agents keep the portfolio aligned with the repositories it references without adding clutter for readers.

The portfolio is a summary layer. It should explain the value, constraints, and engineering signal of each project. It should not copy full project READMEs, track every release, or make claims that are not supported by the referenced repository.

## When To Update Portfolio Pages

Update a portfolio project page when a referenced project has changed in a way that affects the reader's understanding of:

- what the project is
- why it exists
- what was built
- what engineering judgment it demonstrates
- what audience or use case it is relevant to

Do not update the portfolio for every routine project commit. Small fixes, internal refactors, dependency bumps, and release housekeeping usually do not need portfolio changes unless they materially change the story a reader should see.

When a referenced project adds durable ADRs, governance boundaries, or maintenance workflows that change the engineering signal, summarize the reader-facing meaning without copying the ADR text or turning the portfolio into a release archive.

## Project Page Checklist

Each project page should make these points easy to find:

- clear summary of the project
- link to the referenced repository
- problem space or reason the project exists
- what was built
- design priorities or constraints
- why the project belongs in the portfolio
- what the project demonstrates to a technical reader

Use plain language. Prefer accurate, specific claims over broad marketing language.

## Alignment Boundaries

When updating project documentation:

- do not overstate production readiness, adoption, uniqueness, or business impact
- do not copy the referenced repository README into the portfolio
- do not turn the portfolio into a changelog or release archive
- do not add process details that distract from reader understanding
- do not add scripts, skills, CI, or badges unless there is a repeated maintenance problem worth solving

The root `README.md` should stay focused on navigation and first-impression clarity. Deeper project context belongs in `projects/`, and maintainer guidance belongs in `docs/`.
