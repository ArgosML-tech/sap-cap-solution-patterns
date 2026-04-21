# BER App

Repository: [ArgosML-tech/ber-app](https://github.com/ArgosML-tech/ber-app)

## Purpose

`ber-app` models a budget expenditure request process with multi-level approvals and role-aware transactional UI.

## Business Problem

Organizations often need a lightweight workflow for spend requests that sits between informal email approvals and a full ERP purchasing cycle. The solution addresses that gap with a structured, auditable approval process.

## Core Capabilities

- draft-based request creation and editing
- threshold-driven approval routing
- requester and approver views
- approval history
- mocked master data integration

## Main Patterns

- workflow-centric CAP service
- explicit business actions for submit, approve, reject, request more info, and withdraw
- role-based authorization
- Fiori Elements for transactional UI

## Why It Matters in This Collection

This project is a strong reference for approval workflows in CAP. It represents the \"process application\" side of the collection.
