# Architecture Principles

The repositories in this collection are different in purpose, but they share a consistent set of architectural ideas.

## 1. Model the domain first

The solutions generally start from CDS-based domain modeling rather than from controllers or ad-hoc endpoints. Entities, code lists, compositions, and associations define the structure of the process before implementation logic is added.

## 2. Prefer business actions over uncontrolled CRUD

Many business transitions are expressed through explicit service actions such as submit, approve, reject, return, close, process, or generate. This makes intent visible and keeps workflow transitions auditable and testable.

## 3. Treat workflow as part of the domain

Statuses, transitions, approver roles, comments, and event logs are not afterthoughts. They are part of the model and service contract.

## 4. Keep integration boundaries explicit

The integration-oriented repositories use CAP as a boundary layer between source systems and consumers. This can mean:

- staging inbound files before pushing to a target service
- extracting and transforming source-system records before publishing them
- exposing a reusable side-by-side service without leaking domain-specific assumptions

## 5. Preserve clean-core thinking

Several solutions are explicitly aligned with clean-core ideas:

- side-by-side services instead of modifying the core system
- staged exchange instead of direct invasive coupling
- reusable document generation outside the ERP core

## 6. Use generated UI where it accelerates delivery

Fiori Elements is used repeatedly as the transactional UI layer. This allows the repositories to focus on domain model, annotations, and behavior rather than low-level UI plumbing.

## 7. Make testability part of the design

The repositories typically include integration tests around:

- workflow transitions
- authorization
- service actions
- mocked external services
- success and failure paths

## 8. Separate transactional systems from analytical consumers

The strongest illustration of this principle is the `lap-cap` plus `link-analysis-platform` pairing:

- transactional and source-facing logic stays in the extraction layer
- analytical interpretation stays in the downstream graph application

This separation reduces coupling and clarifies responsibilities.
