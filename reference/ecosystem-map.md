---
type: Reference Index
title: Ecosystem Map
description: Sibling repositories and where content belongs across Ben's personal Git folders.
tier: reference
timestamp: 2026-06-29T00:00:00Z
path: reference/ecosystem-map.md
---

# Ecosystem Map

| Repo | Path | Purpose |
|------|------|---------|
| **junk_delete** | `C:\Git\junk_delete` | Ephemeral staging — triage here first |
| **personal** | `C:\Git\personal` | Durable personal/business/reference info |
| **Random** | `C:\Git\Random` | Local projects and experiments |
| **RT-BIZ** | `C:\Git\RT-BIZ` | RetinaTek business canon (read-only) |

## Promotion targets

| Content type | Destination |
|--------------|-------------|
| Personal/business info | `personal/` appropriate folder |
| Project/code/experiment | `Random/projects/<name>/` |
| Frozen external source | `imports/` in destination repo |
| RetinaTek business fact | RT-BIZ ingestion — **not** personal repos |

See [promotion-workflow.md](promotion-workflow.md) for the full decision tree.
