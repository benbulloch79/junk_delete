---
type: Workflow
title: junk_delete OKF Profile
description: How this staging repository uses Open Knowledge Format v0.1.
tier: reference
timestamp: 2026-06-29T00:00:00Z
path: reference/okf-profile.md
---

# junk_delete OKF Profile

> **Bundle root:** [`index.md`](../index.md) · **Agent bootstrap:** [`AGENTS.md`](../AGENTS.md)

## Purpose

This repo is **ephemeral staging**. Every file should eventually be promoted to **personal** or **Random**, or deleted.

## Conformance rule

Every `.md` file (except subdirectory `index.md`) must have YAML frontmatter with `type` and `tier: staging` (or `tier: import` in `imports/`).

## Type vocabulary

| `type` | Use for |
|---|---|
| `Index` | Root `README.md`, bundle `index.md` |
| `Agent Bootstrap` | `AGENTS.md` |
| `Staging` | Content in `inbox/` and `staging/` |
| `Source Import` | Frozen files in `imports/` |
| `Reference Index` | `reference/*.md` |
| `Workflow` | SOPs including promotion-workflow |
| `Operational Log` | `tracking/promotion-log.md` |
| `Tracking` | `tracking/staging-queue.md` |
| `Template` | `templates/*.md` |

## Folder conventions

| Folder | Default `type` | Default `tier` |
|---|---|---|
| `inbox/` | `Staging` | `staging` |
| `staging/` | `Staging` | `staging` |
| `imports/` | `Source Import` | `import` |
| `tracking/` | `Tracking` or `Operational Log` | `ops` |
