# CAP PDF Engine

Repository: [ArgosML-tech/cap-pdf-engine](https://github.com/ArgosML-tech/cap-pdf-engine)

## Purpose

`cap-pdf-engine` is a side-by-side document generation service that stores document templates and renders business data into `.docx` outputs through a simple service contract.

## Business Problem

Document generation often becomes tightly tied to ERP custom logic or older form technologies. This project explores a reusable external service approach that preserves clean-core principles.

## Core Capabilities

- central template repository
- template administration UI
- document generation by `templateID` plus JSON payload
- role separation between administrators and consumers
- template rendering with `docxtemplater`

## Main Patterns

- reusable side-by-side technical service
- template-driven generation instead of domain-specific logic
- binary file handling in CAP
- administrative UI plus consumption API

## Why It Matters in This Collection

This repository represents the platform-service side of the portfolio. It shows CAP being used not only for business process apps but also for shared technical capabilities.
