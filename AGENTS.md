---
type: Agent Bootstrap
title: junk_delete — Agent Bootstrap
description: Triage ephemeral content here — promote to personal or Random, or delete.
tier: reference
timestamp: 2026-06-29T00:00:00Z
path: AGENTS.md
---

# junk_delete — Agent Bootstrap

Read this first. **Humans:** [README.md](README.md) · **Bundle index:** [index.md](index.md)

## Purpose

This repo holds **temporary** content. Nothing should live here permanently. Every item gets triaged: promote to a permanent repo or delete.

## Where things go

| Zone | Path | Put here |
|------|------|----------|
| Unsorted | `inbox/` | Anything new — figure out later |
| Sorted temp | `staging/<topic>/` | Grouped but not yet promoted |
| Frozen downloads | `imports/` | External files — do not edit |
| Queue | `tracking/staging-queue.md` | Items needing a decision |
| Log | `tracking/promotion-log.md` | What was promoted and where |

## Promotion

Follow [reference/promotion-workflow.md](reference/promotion-workflow.md):

- Personal/business → `C:\Git\personal`
- Projects/code → `C:\Git\Random\projects/<name>/`
- RetinaTek facts → RT-BIZ only

## New files

Use `type: Staging`, `tier: staging` frontmatter. Copy [templates/concept.md](templates/concept.md).
