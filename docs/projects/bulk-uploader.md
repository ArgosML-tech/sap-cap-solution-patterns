# Bulk Uploader

Repository: [ArgosML-tech/bulk-uploader](https://github.com/ArgosML-tech/bulk-uploader)

## Purpose

`bulk-uploader` implements a clean-core-friendly mass upload pattern that receives Excel files, stages them, parses them dynamically, and delegates clean rows to a configured external API.

## Business Problem

Mass uploads into SAP systems often become brittle, domain-specific, and tightly coupled. This project explores a safer gateway pattern: stage first, validate and sanitize second, inject third.

## Core Capabilities

- Excel file upload and staging
- template-driven target resolution
- dynamic row parsing without hardcoded business columns
- row-by-row delegation to an external service
- persistent error reporting per rejected row

## Main Patterns

- staging boundary before ERP injection
- generic integration service contract
- file-based ingestion with structured feedback
- mocked external API for local development

## Why It Matters in This Collection

This repository represents the \"integration sanitization\" pattern. It complements workflow-oriented apps by showing CAP as a protective boundary in front of SAP APIs.
