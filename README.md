# SAP CAP Solution Patterns

Collection of reference applications and technical patterns for enterprise workflows, integration services, side-by-side extensions, reusable platform components, and analytical applications built with SAP CAP and adjacent technologies.

This repository is a documentation hub. It does not duplicate the source code of the individual solutions. Instead, it provides a structured map of the solution space covered by the linked repositories and highlights the architectural patterns that connect them.

## How To Use This Repository

Use this repository as a decision guide, not as a standalone executable product.

- If you want to study workflow-oriented CAP applications, start with `cap-exc` or `ber-app`.
- If you want clean-core integration and boundary patterns, start with `bulk-uploader` or `lap-cap`.
- If you want reusable side-by-side services, start with `cap-pdf-engine`.
- If you want analytics consuming staged operational data, start with `lap-cap` and then `link-analysis-platform`.

## Scope

The current collection covers four broad areas:

- workflow-centric CAP applications
- integration and clean-core side-by-side services
- reusable platform services
- analytical consumption of extracted and operational data

## Solution Map

| Solution | Domain | Main Stack | Primary Pattern | Use This When | Repository |
|---|---|---|---|---|---|
| BER App | Budget expenditure requests | SAP CAP, Fiori Elements, SQLite | Multi-level approval workflow | You want a CAP reference for approval routing and role-aware request handling | [ArgosML-tech/ber-app](https://github.com/ArgosML-tech/ber-app) |
| Bulk Uploader | Clean-core mass upload | SAP CAP, Excel parsing, external service mock | Staging and sanitization gateway | You need a file-based staging layer before sending rows to SAP APIs | [ArgosML-tech/bulk-uploader](https://github.com/ArgosML-tech/bulk-uploader) |
| CAP-EXC | Operational exception handling | SAP CAP, Fiori Elements, SQLite | Stateful workflow with audit trail | You want a strong CAP example for governance-heavy workflow and auditability | [ArgosML-tech/cap-exc](https://github.com/ArgosML-tech/cap-exc) |
| CAP-MIL | Urgent procurement | SAP CAP, Fiori Elements, SQLite | End-to-end urgent case lifecycle | You want a richer operational workflow that continues beyond simple approval | [ArgosML-tech/cap-mil](https://github.com/ArgosML-tech/cap-mil) |
| CAP PDF Engine | Document generation side-by-side | SAP CAP, docxtemplater, Fiori Elements | Reusable document rendering service | You need a side-by-side document service decoupled from ERP core logic | [ArgosML-tech/cap-pdf-engine](https://github.com/ArgosML-tech/cap-pdf-engine) |
| LAP-CAP | SAP-to-analytics integration | SAP CAP, Fiori Elements, SQLite | Extract-transform-stage handoff | You need a controlled handoff layer between SAP-like data and analytics | [ArgosML-tech/lap-cap](https://github.com/ArgosML-tech/lap-cap) |
| Link Analysis Platform | Graph analysis and investigation | React, Node.js, Express, SQLite | Interactive analytical application | You want to see how staged business data can be consumed in a graph-first analytical UI | [ArgosML-tech/link_analysis](https://github.com/ArgosML-tech/link_analysis) |

## Where To Start

### For CAP Workflow Learning

1. [CAP-EXC](docs/projects/cap-exc.md)
2. [BER App](docs/projects/ber-app.md)
3. [CAP-MIL](docs/projects/cap-mil.md)

### For Integration and Clean-Core Patterns

1. [Bulk Uploader](docs/projects/bulk-uploader.md)
2. [LAP-CAP](docs/projects/lap-cap.md)
3. [CAP PDF Engine](docs/projects/cap-pdf-engine.md)

### For Downstream Analytical Consumption

1. [LAP-CAP](docs/projects/lap-cap.md)
2. [Link Analysis Platform](docs/projects/link-analysis-platform.md)

## Collection Structure

- [Overview](docs/overview.md)
- [Solution Map](docs/solution-map.md)
- [Architecture Principles](docs/architecture-principles.md)
- [Cross-Cutting Patterns](docs/cross-cutting-patterns.md)
- [MVP vs Production Hardening](docs/mvp-vs-production-hardening.md)
- Project notes:
  - [BER App](docs/projects/ber-app.md)
  - [Bulk Uploader](docs/projects/bulk-uploader.md)
  - [CAP-EXC](docs/projects/cap-exc.md)
  - [CAP-MIL](docs/projects/cap-mil.md)
  - [CAP PDF Engine](docs/projects/cap-pdf-engine.md)
  - [LAP-CAP](docs/projects/lap-cap.md)
  - [Link Analysis Platform](docs/projects/link-analysis-platform.md)

## Cross-Cutting Themes

Across the repositories, several patterns appear repeatedly:

- CDS-based domain modeling
- business actions over generic CRUD surfaces
- draft-enabled transactional flows
- role-based authorization
- explicit workflow and state transitions
- audit trail and event logging
- Fiori Elements as a transactional enterprise UI layer
- mocked or staged integration with SAP core services
- automated validation through integration tests
- separation between source systems, integration boundaries, and downstream consumers

## Why This Repository Exists

This repository is intentionally stronger as a map of solutions than as a standalone codebase. Its purpose is to:

- show the range of problems SAP CAP can address
- make patterns discoverable across multiple repositories
- separate what each MVP proves from what production hardening would still require
- help readers jump quickly to the right repository for the right problem

## Repository Goal

The goal of this repository is to provide a coherent, impersonal, architecture-first showcase of SAP CAP solution patterns across multiple business and technical scenarios.
