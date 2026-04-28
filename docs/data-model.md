
---

## `docs/data-model.md`

```md
# CloudTask DynamoDB Data Model

## 1. Data Model Overview

CloudTask uses DynamoDB with a single-table design.

The table stores:

- Tenants
- Users
- Projects
- Tasks
- Attachments
- Audit events

Table name:

```text
CloudTaskTable
