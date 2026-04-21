# SAP CAP Solution Patterns

Collection of reference applications and technical patterns for enterprise workflows, integration services, side-by-side extensions, reusable platform components, and analytical applications built with SAP CAP and adjacent technologies.

This repository is a documentation hub. It does not duplicate the source code of the individual solutions. Instead, it provides a structured map of the solution space covered by the linked repositories and highlights the architectural patterns that connect them.

## Scope

The current collection covers four broad areas:

- workflow-centric CAP applications
- integration and clean-core side-by-side services
- reusable platform services
- analytical consumption of extracted and operational data

## Solution Map

| Solution | Domain | Main Stack | Primary Pattern | Repository |
|---|---|---|---|---|
| BER App | Budget expenditure requests | SAP CAP, Fiori Elements, SQLite | Multi-level approval workflow | [ArgosML-tech/ber-app](https://github.com/ArgosML-tech/ber-app) |
| Bulk Uploader | Clean-core mass upload | SAP CAP, Excel parsing, external service mock | Staging and sanitization gateway | [ArgosML-tech/bulk-uploader](https://github.com/ArgosML-tech/bulk-uploader) |
| CAP-EXC | Operational exception handling | SAP CAP, Fiori Elements, SQLite | Stateful workflow with audit trail | [ArgosML-tech/cap-exc](https://github.com/ArgosML-tech/cap-exc) |
| CAP-MIL | Urgent procurement | SAP CAP, Fiori Elements, SQLite | End-to-end urgent case lifecycle | [ArgosML-tech/cap-mil](https://github.com/ArgosML-tech/cap-mil) |
| CAP PDF Engine | Document generation side-by-side | SAP CAP, docxtemplater, Fiori Elements | Reusable document rendering service | [ArgosML-tech/cap-pdf-engine](https://github.com/ArgosML-tech/cap-pdf-engine) |
| LAP-CAP | SAP-to-analytics integration | SAP CAP, Fiori Elements, SQLite | Extract-transform-stage handoff | [ArgosML-tech/lap-cap](https://github.com/ArgosML-tech/lap-cap) |
| Link Analysis Platform | Graph analysis and investigation | React, Node.js, Express, SQLite | Interactive analytical application | [ArgosML-tech/link_analysis](https://github.com/ArgosML-tech/link_analysis) |

## Collection Structure

- [Overview](docs/overview.md)
- [Solution Map](docs/solution-map.md)
- [Architecture Principles](docs/architecture-principles.md)
- [Cross-Cutting Patterns](docs/cross-cutting-patterns.md)
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

## Suggested Reading Order

A useful order for exploring the collection is:

1. `cap-exc` or `ber-app` for workflow-oriented CAP applications
2. `cap-mil` for a broader procurement lifecycle
3. `bulk-uploader` and `cap-pdf-engine` for reusable service patterns
4. `lap-cap` for extraction and integration boundary design
5. `link-analysis-platform` for downstream analytical consumption

## Repository Goal

The goal of this repository is to provide a coherent, impersonal, architecture-first showcase of SAP CAP solution patterns across multiple business and technical scenarios.
