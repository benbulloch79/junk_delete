---
type: Index
title: junk_delete
description: Ephemeral staging repo — triage before promoting to personal or Random, or delete.
tier: reference
owner: Ben
timestamp: "2026-06-29T00:00:00Z"
path: junk_delete/README.md
url: "https://github.com/benbulloch79/junk_delete/blob/main/README.md"
---

# junk_delete

Temporary staging for content that might be worth keeping. **Triage everything** — promote to a permanent repo or delete.

> **Contributors & AI agents:** read [`AGENTS.md`](AGENTS.md) first.

## Structure

```
junk_delete/
├── index.md              # Bundle index
├── AGENTS.md             # Agent bootstrap
├── inbox/                # Unsorted incoming
├── staging/              # Sorted by topic, still ephemeral
├── reference/            # OKF profile, ecosystem map, promotion workflow
├── tracking/             # Staging queue and promotion log
├── imports/              # Frozen downloads (optional)
└── templates/            # New-file scaffold
```

## Workflow

1. Drop new items in `inbox/`.
2. Move to `staging/<topic>/` when you know the category.
3. Decide: promote (see [reference/promotion-workflow.md](reference/promotion-workflow.md)) or delete.
4. Log promotions in `tracking/promotion-log.md`.

## Permanent homes

| Content | Destination |
|---------|-------------|
| Personal/business info | [`personal`](C:\Git\personal) |
| Projects/experiments | [`Random`](C:\Git\Random) |
| RetinaTek business facts | [`RT-BIZ`](C:\Git\RT-BIZ) |

See [reference/ecosystem-map.md](reference/ecosystem-map.md).
## Writing rule

Do not use em dash punctuation in any output. Use commas, parentheses, colons, or hyphens instead.
