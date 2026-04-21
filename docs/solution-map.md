# Solution Map

## Portfolio View

| Solution | Domain | Main Stack | Main Pattern | Strength |
|---|---|---|---|---|
| BER App | Budget control | SAP CAP, Fiori Elements | Approval workflow | Clear multi-level routing |
| Bulk Uploader | Master data integration | SAP CAP, xlsx, external service mock | Sanitized staging before S/4 | Generic ingestion contract |
| CAP-EXC | Operational governance | SAP CAP, Fiori Elements | Exception regularization workflow | Strong auditability |
| CAP-MIL | Procurement operations | SAP CAP, Fiori Elements | Urgent procurement lifecycle | Rich end-to-end flow |
| CAP PDF Engine | Document services | SAP CAP, docxtemplater | Side-by-side rendering service | Reusable cross-domain capability |
| LAP-CAP | Extraction and handoff | SAP CAP, Fiori Elements | Extract-transform-stage pattern | Clear integration boundary |
| Link Analysis Platform | Investigation and analytics | React, Node.js, Express | Graph-driven analysis workspace | Rich analytical consumption layer |

## Functional Grouping

### Process and Workflow

- [BER App](projects/ber-app.md)
- [CAP-EXC](projects/cap-exc.md)
- [CAP-MIL](projects/cap-mil.md)

### Clean-Core Integration

- [Bulk Uploader](projects/bulk-uploader.md)
- [LAP-CAP](projects/lap-cap.md)

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

If the focus is analytics and downstream use of extracted data:

- start with `lap-cap`
- continue with `link-analysis-platform`
