# Solution Map

## Portfolio View

| Solution | Domain | Main Stack | Main Pattern | Strength | Best Entry Point For |
|---|---|---|---|---|---|
| BER App | Budget control | SAP CAP, Fiori Elements | Approval workflow | Clear multi-level routing | CAP approval flows |
| Bulk Uploader | Master data integration | SAP CAP, xlsx, external service mock | Sanitized staging before S/4 | Generic ingestion contract | File staging and clean-core ingestion |
| CAP-EXC | Operational governance | SAP CAP, Fiori Elements | Exception regularization workflow | Strong auditability | Governance-heavy workflow design |
| CAP-MIL | Procurement operations | SAP CAP, Fiori Elements | Urgent procurement lifecycle | Rich end-to-end flow | Longer operational lifecycle handling |
| CAP PDF Engine | Document services | SAP CAP, docxtemplater | Side-by-side rendering service | Reusable cross-domain capability | Reusable technical services |
| LAP-CAP | Extraction and handoff | SAP CAP, Fiori Elements | Extract-transform-stage pattern | Clear integration boundary | System boundary and handoff design |
| Warranty Management | SAP standard extension | SAP CAP, Fiori Elements, imported OData services | Side-by-side standard-object extension | Strong data mashup and draft flow | Standard SAP extensibility patterns |
| Link Analysis Platform | Investigation and analytics | React, Node.js, Express | Graph-driven analysis workspace | Rich analytical consumption layer | Downstream analytical UI |

## Functional Grouping

### Process and Workflow

- [BER App](projects/ber-app.md)
- [CAP-EXC](projects/cap-exc.md)
- [CAP-MIL](projects/cap-mil.md)

### Clean-Core Integration

- [Bulk Uploader](projects/bulk-uploader.md)
- [LAP-CAP](projects/lap-cap.md)

### Standard SAP Extensibility

- [Warranty Management](projects/warranty-mgmt.md)

### Reusable Technical Services

- [CAP PDF Engine](projects/cap-pdf-engine.md)

### Downstream Consumption and Analytics

- [Link Analysis Platform](projects/link-analysis-platform.md)

## Reading Strategy

If the focus is CAP workflow design:

- start with `cap-exc`
- continue with `ber-app`
- then explore `cap-mil`

If the focus is integration and side-by-side architecture:

- start with `bulk-uploader`
- continue with `lap-cap`
- then explore `cap-pdf-engine`

If the focus is extending standard SAP objects and imported services:

- start with `warranty-mgmt`
- continue with `ber-app`
- then compare with `bulk-uploader`

If the focus is analytics and downstream use of extracted data:

- start with `lap-cap`
- continue with `link-analysis-platform`

## What Each Repository Proves

### Workflow and Process Apps

- `cap-exc` proves that CAP can model exception governance with states, comments, event logs, and role-restricted transitions.
- `ber-app` proves threshold-driven approval routing with draft-enabled request handling and mock master data integration.
- `cap-mil` proves a broader urgent procurement lifecycle beyond simple approval, including follow-through and closure.

### Integration and Boundary Services

- `bulk-uploader` proves a staging-first mass upload pattern that keeps parsing and sanitization outside the core target system.
- `lap-cap` proves a handoff architecture where extraction and transformation are kept separate from downstream analytics.

### Standard SAP Extensibility

- `warranty-mgmt` proves that CAP can consume standard SAP APIs, enrich standard records with local data, and support draft-enabled business processes around extended objects.

### Reusable Technical Services

- `cap-pdf-engine` proves a side-by-side template-rendering service that other systems can consume without embedding domain-specific document logic.

### Downstream Consumption

- `link-analysis-platform` proves that staged and transformed operational data can support a graph-first analytical application with risk-oriented exploration.
