# Content Overview

This repository contains no source code. Its original implementation is the set of Markdown template files. This document explains what each file does. It is the equivalent of a code overview for a documentation-only project.

All files listed under **Original files** are preserved exactly as they were originally written.

## Original files

### Root

| File | Purpose | Key contents |
| --- | --- | --- |
| [`PROJECT_CENTER_BLUEPRINT.md`](../PROJECT_CENTER_BLUEPRINT.md) | Founding design document (20 sections) | Problem, objective, audience, why Markdown, naming options, design principles, folder architecture, project file model, categories, data sources, V1/V2 scope, 6-phase roadmap, success criteria, risks |
| [`INDEX.md`](../INDEX.md) | Public navigation hub | Links to core documents, placeholder "Featured projects", suggested thematic sections (AI and data, Engineering, Business, Personal tools, Experimental), maintenance rule |
| [`CONTRIBUTING.md`](../CONTRIBUTING.md) | Adoption guide | 5-step template usage, documentation rules, `projects/project-name.md` naming, `docs:` commit styles, public safety list |
| [`AGENTS.md`](../AGENTS.md) | Guidelines for contributors and AI coding agents | Structure, no-build workflow (`rg`, `git diff --check`), style, manual validation checklist, commit/PR rules, security |
| `README.md` | Entry point | Replaced by a modern README during this refactor. The original is preserved verbatim at [`original/original-readme.md`](./original/original-readme.md) |

### `docs/`

| File | Purpose |
| --- | --- |
| [`repository-rules.md`](./repository-rules.md) | 7 core rules, formatting conventions, public/private separation, review cadence (monthly, quarterly, yearly) |

### `profile/`

| File | Purpose |
| --- | --- |
| [`summary.md`](../profile/summary.md) | Placeholder public profile: who I am, what I work on, differentiators, current focus, themes, links |

### `cv/`

| File | Purpose |
| --- | --- |
| [`master-cv.md`](../cv/master-cv.md) | Placeholder master CV: identity, summary, strengths, repeated experience blocks (scope, responsibilities, achievements, related projects), education, certifications, tools, project clusters, tailoring notes |

### `templates/`

| File | Purpose |
| --- | --- |
| [`project-template.md`](../templates/project-template.md) | Standard project model: Snapshot (status, category, owner, dates, visibility, links, tags), one-line summary, context, problem, objective, scope, why it matters, role, stakeholders, stack, architecture, milestones, outcomes, metrics, challenges, decisions, lessons, next steps, references |

### `projects/`

| File | Purpose |
| --- | --- |
| [`README.md`](../projects/README.md) | Instructions for adding one kebab-case file per project, and a note about the ignore rule |
| [`.gitignore`](../projects/.gitignore) | Ignores `*.md` except `README.md` and `.gitignore`, so the template stays empty |

### `timeline/`, `chats/`, `sources/`

| File | Purpose |
| --- | --- |
| [`timeline/README.md`](../timeline/README.md) | Guidance for milestone files (`2024.md`, `career-milestones.md`, …) |
| [`chats/README.md`](../chats/README.md) | Rule: summarize and redact, never dump raw chats. Lists use cases |
| [`sources/README.md`](../sources/README.md) | Provenance registry guidance: origin, capture date, summarization, public safety |

## Historical files (`docs/original/`)

| File | Origin |
| --- | --- |
| [`original-readme.md`](./original/original-readme.md) | Root `README.md` as of commits `2a63d9a` and `5b59a63`, before this refactor |
| [`original-projects-readme.md`](./original/original-projects-readme.md) | `projects/README.md` from `init` (`2a63d9a`), rewritten in `5b59a63` |
| [`original-project-center-example.md`](./original/original-project-center-example.md) | `projects/project-center.md` from `init` (`2a63d9a`): the only filled-in example project, which documented Project Center itself. Removed in `5b59a63` |

Files in `docs/original/` are copies recovered from git history, kept for reference. They are not active parts of the template.

## Documentation added during the refactor

| File | Purpose |
| --- | --- |
| [`README.md`](./README.md) | Documentation index |
| [`project-context.md`](./project-context.md) | Origin, evidence, timeline, contradictions |
| [`architecture.md`](./architecture.md) | Information architecture and content flow |
| [`content-overview.md`](./content-overview.md) | This file |
| [`possible-improvements.md`](./possible-improvements.md) | Observations that were deliberately not applied |
| [`sdlc/intent.md`](./sdlc/intent.md), [`sdlc/spec.md`](./sdlc/spec.md), [`sdlc/plan.md`](./sdlc/plan.md) | Intent, specification, and plan reconstructed from the existing repository |
