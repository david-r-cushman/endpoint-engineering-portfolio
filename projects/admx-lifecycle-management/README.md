# Administrative Template Lifecycle Management

[← Portfolio](../../README.md) · [Project Selection Criteria](../../docs/project-selection.md) · [Portfolio Roadmap](../../docs/portfolio-roadmap.md)

## Investigation Context

Administrative templates are deployment dependencies. This investigation considers how vendor-provided ADMX and ADML distributions can be preserved across releases with provenance and integrity information available when a known source artifact must be re-supplied to an endpoint-management or Group Policy process.

The work distinguishes preserving a source artifact from managing its deployment. It does not establish vendor authenticity, acquire releases, extract packages automatically, deploy templates, create or restore Intune configuration, or manage Group Policy Objects or Central Store state.

## Engineering Artifacts

| Repository | Purpose |
|---|---|
| [vendor-admx-archive](https://github.com/david-r-cushman/vendor-admx-archive) | Reusable template for archiving one vendor's administrative-template distributions across releases. |
| [demo-admx-archive](https://github.com/david-r-cushman/demo-admx-archive) | Public, populated reference implementation using self-authored fictional artifacts to demonstrate the multi-release archive workflow. |

Each registered release preserves original source files, records provenance and SHA-256 hashes in an immutable first manifest, and can verify that registered downloads have not changed. Optional extracted content is kept outside that integrity baseline.

## Engineering Significance

This investigation demonstrates a narrow, deliberate trust boundary around source preservation. It separates known deployment inputs from the separate concerns of vendor trust, configuration deployment, platform state, and recovery execution.

The template and demonstration show how repository structure, explicit boundaries, validation, documentation, and release governance can make a small operational dependency more traceable and reviewable without overstating what the archive itself guarantees.
