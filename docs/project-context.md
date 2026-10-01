# Project Context

This document reconstructs the origin, purpose, and history of **Project Center** from the evidence available in the repository. Each statement is labeled as **Confirmed**, **Inferred**, or **Unknown**.

## Classification

- **Project origin:** Personal Project
- **Project type:** Markdown-first repository template (documentation system, no executable code)
- **Confidence:** High

### Evidence

| Evidence | Source | Status |
| --- | --- | --- |
| Both commits were authored by Baruch López on 2026-03-17 | `git log` | Confirmed |
| The repository is described as a "personal operating repository" and a "personal project operating system" | [`PROJECT_CENTER_BLUEPRINT.md`](../PROJECT_CENTER_BLUEPRINT.md) §1, §20 | Confirmed |
| The blueprint recommends two repos: a public template (`project-center-template`) and a personal live repo (`project-center`) | [`PROJECT_CENTER_BLUEPRINT.md`](../PROJECT_CENTER_BLUEPRINT.md) §7 | Confirmed |
| The author's role was recorded as "System designer, information architect, and initial author" | [`original-project-center-example.md`](./original/original-project-center-example.md) | Confirmed |
| No university, course, assignment, or client is mentioned anywhere | All files | Confirmed (absence) |
| This repository is the **template** variant, not the personal live variant | Placeholder content in `profile/`, `cv/`; empty `projects/` | Inferred |

## Problem Statement

**Confirmed** ([Blueprint §2](../PROJECT_CENTER_BLUEPRINT.md)): professionals who build many things produce work across fragmented systems (AI chat workspaces, GitHub repositories, VPS projects, cloud tools, LinkedIn, multiple résumé versions, notes). This leads to:

- no single source of truth,
- no structured historical memory,
- weak project presentation,
- duplicated effort when updating CVs or portfolios,
- difficulty explaining the full scope of one's work.

## Objective

**Confirmed** ([Blueprint §3](../PROJECT_CENTER_BLUEPRINT.md)): build a public, reusable, Markdown-first repository that centralizes projects, CV, timeline, knowledge extracted from chats and tools, and a navigable index presenting a complete professional profile. It should be simple, minimalist, easy to clone, easy to maintain, and good enough to present publicly.

## Scope

**Confirmed** ([Blueprint §14](../PROJECT_CENTER_BLUEPRINT.md), [original example project](./original/original-project-center-example.md)):

- **In scope (V1):** README, blueprint, reusable project template, profile summary, master CV, project index, starter folders, and contribution and repository rules.
- **Out of scope (V1):** heavy automation, databases, front-end dependencies, private data ingestion, over-engineered schemas.
- **Deferred to V2:** static site generation, automatic indexing, résumé generation, tag navigation, search, GitHub Pages, metadata headers, JSON/YAML mirrors, AI summarization scripts, import helpers ([Blueprint §15](../PROJECT_CENTER_BLUEPRINT.md)).

## Historical Timeline

| Date | Commit | Change | Status |
| --- | --- | --- | --- |
| 2026-03-17 13:50 (UTC-6) | `2a63d9a` `init` | Initial skeleton: README, blueprint, index, contributing guide, all content folders, the project template, and one example project (`projects/project-center.md`) documenting Project Center itself | Confirmed |
| 2026-03-17 13:59 (UTC-6) | `5b59a63` `docs: add repository guidelines and empty projects template` | Added `AGENTS.md` (contributor and AI-agent guidelines). Removed the example project and added `projects/.gitignore` so user project files are ignored by default. Rewrote `projects/README.md` | Confirmed |
| 2026-09 | Repository documentation refactor | Added modern documentation around the original files without changing them (this document) | Confirmed |

### Interpretation of the second commit

**Inferred:** the author turned the repository from a *personal instance* into a *clean, clonable template*. The self-describing example project was removed, and new project files are git-ignored so each person who clones it starts empty. The removed files are kept in [`docs/original/`](./original/) for historical reference.

## Relation to the Blueprint Roadmap

**Inferred** from the repository contents compared with [Blueprint §16](../PROJECT_CENTER_BLUEPRINT.md):

| Phase | Status |
| --- | --- |
| 1 — Define the system | Done (blueprint, conventions, founding docs) |
| 2 — Build the repository skeleton | Done (all folders, templates, index) |
| 3 — Populate with initial content | Not started in this template (placeholders only). By design, this belongs in the personal live repository |
| 4 — Standardize project ingestion | Partly done (template, naming rules, `sources/` and `chats/` guidance) |
| 5 — Prepare public distribution | Partly done (`projects/.gitignore`, public-safety rules) |
| 6 — Optional automation | Not started |

## Unknowns

- Whether a separate personal live `project-center` repository exists. *The original repository does not provide enough information to determine this.*
- Which tools, if any, were used to draft the blueprint. `AGENTS.md` shows the repo is meant to be AI-agent-friendly, but authorship tooling is not recorded.
- Whether the repository has been published as a GitHub template repository.

## Contradictions Found

- **Blueprint §14 vs. the current template:** V1 "should include … a few real example projects", but commit `5b59a63` intentionally removed the only example project. *Inferred resolution:* the blueprint describes the personal live repo, and the template stays empty on purpose.
- **Blueprint §7:** it recommends the name `project-center-template` for the public template, but this repository is named `Project-Center`.
- **`AGENTS.md`:** it says "The current history is minimal (`init`)", which was written before its own commit was added.

These are documented, not corrected. See [possible-improvements.md](./possible-improvements.md).
