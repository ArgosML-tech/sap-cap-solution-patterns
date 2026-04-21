# LAP-CAP

Repository: [ArgosML-tech/lap-cap](https://github.com/ArgosML-tech/lap-cap)

## Purpose

`lap-cap` is an extraction and staging service that sits between SAP-like source data and a downstream analytical consumer, the Link Analysis Platform.

## Business Problem

Downstream investigative or analytical applications should not couple directly to source-system contracts. A controlled extraction and handoff layer reduces coupling and clarifies responsibilities.

## Core Capabilities

- extraction scenarios and mappings
- transformation of source records into LAP-ready node CSVs
- file staging and ingestion status tracking
- admin UI for scenario management
- HTTP file API consumed by the downstream analytical application

## Main Patterns

- extract-transform-stage handoff
- CAP as integration boundary
- file-based inter-application contract
- clean separation between operational source-facing logic and analytical consumption

## Why It Matters in This Collection

This is a key bridge between transactional/integration concerns and analytics. It is one of the strongest examples of explicit system boundary design in the collection.
