---
type: Workflow
title: junk_delete OKF Profile
description: How this repository uses Open Knowledge Format v0.2 — type taxonomy, extension fields, path/url convention, and folder conventions.
tier: reference
validation_tier: authoritative
owner: Ben
timestamp: "2026-07-02T15:16:39Z"
path: junk_delete/reference/okf-profile.md
url: "https://github.com/benbulloch79/junk_delete/blob/main/reference/okf-profile.md"
---

# junk_delete OKF Profile

> Standardized RetinaTek OKF profile (v0.2). Structure and vocabulary mirror the
> RT-BIZ master profile; repo-specific facts, claims, and registries are intentionally
> out of scope here. Frontmatter is **metadata only** — facts stay in document bodies.

## Conformance rule

Every `.md` file in this repo (except subdirectory `index.md` / `log.md` navigation files)
should have **parseable YAML frontmatter** with a non-empty **`type`** field.

## Required field

| Field | Rule |
|---|---|
| `type` | One value from the vocabulary below |

## Recommended fields

| Field | Rule |
|---|---|
| `title` | Human title; usually mirrors first `#` heading |
| `description` | One-line summary for agents |
| `tier` | `canon` · `reference` · `analysis` · `ops` · `import` |
| `timestamp` | ISO 8601 UTC — last meaningful edit |
| `path` | Repo-qualified path for human sharing (`junk_delete/<file>`) |
| `url` | GitHub blob link (tool-generated; **internal-only** for private repos) |

**Path/URL convention:** `path` = `junk_delete/<repo-relative-path>`; `url` =
`https://github.com/benbulloch79/junk_delete/blob/main/<repo-relative-path>` (path segments URL-encoded). Both are tool-generated —
regenerate with `python <RT-BIZ>/tools/okf-apply.py --root . --apply`.

## Extension fields

| Field | Values | Use |
|---|---|---|
| `sensitivity` | `public-ok` · `internal` · `confidential` | Disclosure tier — never put confidential content in frontmatter |
| `validation_tier` | `authoritative` · `superseded` · `unvalidated` | Source-validation status |
| `owner` | `Mark` · `Ben` · `shared` · `routine` | Accountability |
| `depends_on` | List of path stems | Upstream docs to read first (repo-local) |
| `supersedes` | List of path stems | Lineage when this doc replaces another |

## Type vocabulary

| `type` | Use for |
|---|---|
| `Index` | Root `README.md`, bundle `index.md` |
| `Agent Bootstrap` | `AGENTS.md`, `FOR-BEN.md` |
| `Agent Skill` | `SKILL.md` |
| `Domain Narrative` | Topic documents, notes, analyses |
| `Reference Index` | `reference/*.md` maps and indexes |
| `Workflow` | SOPs, profiles, this file |
| `Meeting Note` | Synthesized meetings |
| `Operational Log` | Append-only logs |
| `Tracking` | Queues, radars, action lists |
| `Source Import` | Frozen files in `imports/` |
| `Pitch` | Outward pitch artifacts |
| `Template` | `templates/*.md` |

## Folder conventions

| Folder | Default `type` | Default `tier` |
|---|---|---|
| `reference/` | `Reference Index` or `Workflow` | `reference` |
| `meetings/` | `Meeting Note` | `ops` |
| `tracking/` | `Operational Log` or `Tracking` | `ops` |
| `imports/` | `Source Import` | `import` |
| `pitches/` | `Pitch` | `reference` |
| `templates/` | `Template` | `reference` |

## Reserved filenames

- **`index.md`** — directory navigation; subdirectory copies stay body-only.
- **`log.md`** — chronological history; body-only.
