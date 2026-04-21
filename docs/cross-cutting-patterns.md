# Cross-Cutting Patterns

This collection is best understood not only by project, but also by recurring patterns.

## Pattern Matrix

| Pattern | BER App | Bulk Uploader | CAP-EXC | CAP-MIL | CAP PDF Engine | LAP-CAP | Link Analysis Platform |
|---|---|---|---|---|---|---|---|
| CDS domain model | Yes | Yes | Yes | Yes | Yes | Yes | Partial |
| Draft support | Yes | Yes | Yes | Yes | Yes | Partial | No |
| Explicit workflow state machine | Yes | No | Yes | Yes | No | Partial | No |
| Role-based authorization | Yes | Partial | Yes | Yes | Yes | Yes | Yes |
| Audit trail or event log | Partial | Partial | Yes | Yes | No | Partial | Yes |
| External service or mock integration | Yes | Yes | No | No | No | Yes | Yes |
| Reusable side-by-side service | No | Yes | No | No | Yes | Yes | No |
| Fiori Elements UI | Yes | Yes | Yes | Yes | Yes | Yes | No |
| Downstream analytical consumption | No | No | No | No | No | Yes | Yes |

## CDS Domain Modeling

The solutions use CAP's modeling layer to encode:

- domain entities
- code lists
- compositions and associations
- catalogs and reference data
- status and lifecycle metadata

## Draft-Enabled Transactions

Several repositories rely on `@odata.draft.enabled` to support enterprise editing flows where changes are prepared, reviewed, and only later activated.

Seen in particular in:

- `ber-app`
- `cap-exc`
- `cap-mil`
- `bulk-uploader`
- `cap-pdf-engine`

## Role-Based Authorization

Role-based access is treated as a first-class concern. The repositories demonstrate service-level and action-level restriction patterns for requesters, approvers, auditors, administrators, operators, and consumers.

## Stateful Workflows

A recurring pattern is the combination of:

- status codes
- explicit transitions
- comments and decisions
- role-specific actions
- validations per transition

This is central to the workflow-oriented repositories.

## Audit Trail and Event Logging

Many solutions persist operational history explicitly through:

- decision logs
- event logs
- comments
- rejection reasons
- closure metadata

## External Service and Mock Integration

The repositories show different ways of using mocks and staged interfaces to develop against external contracts:

- mocked OData services for SAP APIs
- file staging before core-system injection
- extracted CSV handoff between systems

## Reusable Side-by-Side Services

Not every repository is a business app. Some are technical capabilities intended to be called by other systems:

- `bulk-uploader`
- `cap-pdf-engine`
- `lap-cap`

## Downstream Analytical Consumption

The collection also covers the pattern where transformed or staged operational data is consumed by an analytical application rather than a transactional one.

This is most visible in:

- `lap-cap`
- `link-analysis-platform`
