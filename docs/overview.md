# Overview

`sap-cap-solution-patterns` is a documentation-first showcase of several related repositories that explore different solution patterns around SAP CAP.

The collection is not intended to represent a single product line. Instead, it groups together a set of architectural approaches that often appear in enterprise SAP landscapes:

- workflow applications with explicit business actions
- clean-core side-by-side services
- standard SAP extensibility and mashup scenarios
- integration boundaries between SAP source systems and downstream consumers
- reusable platform services
- developer tooling and accelerators for CAP delivery
- analytical applications that consume staged or transformed business data

The repositories in this collection are useful as reference implementations, MVPs, and pattern explorations rather than as drop-in production products.

## Areas Covered

### Workflow Applications

Applications that model stateful business processes with roles, transitions, comments, decisions, attachments, and audit trails.

- `ber-app`
- `cap-exc`
- `cap-mil`

### Integration Services

Services that sit between SAP systems and consumers, adding staging, transformation, validation, or clean-core boundaries.

- `bulk-uploader`
- `lap-cap`

### Standard Extensibility

Applications that consume standard SAP APIs, extend standard business objects with local behavior or fields, and expose side-by-side transactional flows through CAP and Fiori Elements.

- `warranty-mgmt`

### Reusable Platform Services

Cross-domain building blocks that can be consumed by other systems or apps.

- `cap-pdf-engine`

### CAP Tooling and Accelerators

Tools that package recurring CAP patterns into starters, generators, and support libraries so that new projects can begin from a stronger baseline.

- `cap-acc`

### Analytical Applications

Applications focused on investigation, graph exploration, risk analysis, and interpretation of staged data.

- `link-analysis-platform`

## Why This Collection Matters

Taken together, the repositories show that SAP CAP can support more than CRUD-based business applications. It can also be used for:

- orchestrating business workflows
- exposing side-by-side services
- extending standard SAP objects through imported services and local enrichments
- handling document generation
- standardizing CAP project bootstrap and extension workflows
- sanitizing inbound data before it reaches core systems
- staging data for downstream analytical applications

That breadth is the main value of the collection.
