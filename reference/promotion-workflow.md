---
type: Workflow
title: Promotion Workflow
description: Decision tree for promoting staged content to permanent repos or deleting it.
tier: reference
owner: Ben
timestamp: "2026-06-29T00:00:00Z"
path: junk_delete/reference/promotion-workflow.md
url: "https://github.com/benbulloch79/junk_delete/blob/main/reference/promotion-workflow.md"
---

# Promotion Workflow

Use this when an item in `inbox/` or `staging/` is no longer "maybe."

## Decision tree

1. **Still needed long-term?** No → delete from this repo. Done.
2. **Personal or business reference?** → Copy to [`personal`](C:\Git\personal) in the appropriate folder (`personal/`, `business/`, `notes/`, `documents/`, `research/`).
3. **Project, code, or experiment?** → Copy to [`Random/projects/<name>/`](C:\Git\Random\projects). Add a row to `Random/projects/index.md`.
4. **Frozen external source?** → Copy to `imports/` in the destination repo with frontmatter: `type: Source Import`, `tier: import`, `validation_tier: unvalidated`.
5. **RetinaTek business fact?** → Do **not** copy to personal or Random. Use RT-BIZ ingestion protocol instead.

## After promotion

1. Log in [tracking/promotion-log.md](../tracking/promotion-log.md) (date · source path · destination · note).
2. Log in destination repo's `tracking/promotion-log.md` if it exists.
3. Remove the file from `inbox/` or `staging/` here.
4. Remove from [tracking/staging-queue.md](../tracking/staging-queue.md).

## Staging rules

- Unsorted incoming → `inbox/`
- Sorted by topic but not yet promoted → `staging/<topic>/`
- Every staged `.md` file gets `type: Staging`, `tier: staging` frontmatter
