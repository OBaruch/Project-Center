# Architecture

Project Center has no runtime, build step, or executable code. Its "architecture" is an **information architecture**: a fixed set of Markdown folders, each with one responsibility, connected by relative links. This document describes that structure as it exists in the repository. It is based on [Blueprint §10](../PROJECT_CENTER_BLUEPRINT.md) and the actual files.

## Layers

```text
┌────────────────────────────────────────────────────────────┐
│ Navigation layer                                           │
│   README.md · INDEX.md                                     │
├────────────────────────────────────────────────────────────┤
│ Governance layer                                           │
│   PROJECT_CENTER_BLUEPRINT.md · CONTRIBUTING.md · AGENTS.md│
│   docs/repository-rules.md                                 │
├────────────────────────────────────────────────────────────┤
│ Identity layer                                             │
│   profile/summary.md · cv/master-cv.md                     │
├────────────────────────────────────────────────────────────┤
│ Work layer                                                 │
│   projects/<slug>.md  ← templates/project-template.md      │
│   timeline/                                                │
├────────────────────────────────────────────────────────────┤
│ Provenance layer                                           │
│   chats/ (redacted summaries) · sources/ (origin registry) │
└────────────────────────────────────────────────────────────┘
```

The layer names are a documentation convenience added during this refactor (**Inferred** grouping). The folders and their responsibilities are **Confirmed** from the files.

## Component Responsibilities

| Component | Responsibility | Defined in |
| --- | --- | --- |
| `README.md` | Entry point and quick orientation | Root |
| `INDEX.md` | Public navigation layer. Links core documents and featured projects | Root |
| `PROJECT_CENTER_BLUEPRINT.md` | Founding design document: problem, goals, principles, roadmap | Root |
| `CONTRIBUTING.md` | How to adopt the template, naming, and commit conventions | Root |
| `AGENTS.md` | Contributor and AI-agent guidelines: structure, style, validation, safety | Root |
| `docs/repository-rules.md` | Core rules, formatting, public/private separation, review cadence | `docs/` |
| `profile/summary.md` | Public-facing identity summary | `profile/` |
| `cv/master-cv.md` | Source-of-truth career record that tailored CVs are derived from | `cv/` |
| `templates/project-template.md` | Standard 20-section model for a project file | `templates/` |
| `projects/` | One file per project (git-ignored by default in the template) | `projects/` |
| `timeline/` | Career and project milestones | `timeline/` |
| `chats/` | Summarized, redacted knowledge extracted from AI chats | `chats/` |
| `sources/` | Provenance: where information came from and whether it is safe to publish | `sources/` |

## Content Flow

The intended workflow, reconstructed from the [README](./original/original-readme.md), [Blueprint §13](../PROJECT_CENTER_BLUEPRINT.md), and folder READMEs:

```text
Scattered sources                      Project Center                        Reuse
─────────────────                      ──────────────                        ─────
AI chats         ──summarize/redact──▶ chats/      ─┐
GitHub repos     ──┐                                │
CV versions      ──┼──record origin──▶ sources/    ─┤
LinkedIn, notes  ──┘                                ├─▶ projects/<slug>.md ─┐
                                                    │   (from template)     ├─▶ INDEX.md ─▶ portfolio, CVs,
                     career events ──▶ timeline/   ─┘                       │               bios, applications
                                       profile/ · cv/ ──────────────────────┘
```

**Confirmed:** V1 extraction is manual or semi-automated. The Blueprint (§13) says "The repository should not depend on direct live integrations in V1."

## Linking Model

- Relative links are used throughout (for example `../projects/project-name.md` in `cv/master-cv.md`).
- `INDEX.md` is the hub. Every important project must be linked from it (the maintenance rule in `INDEX.md`, `docs/repository-rules.md` rule 5).
- Placeholder links in `INDEX.md` and `cv/master-cv.md` point to files that do not exist yet. This is intentional in a template.

## Template/Instance Mechanism

`projects/.gitignore` ignores `*.md` except `README.md`. This lets the public template stay empty while each person's clone keeps its project files local until they change the ignore rule (**Confirmed** in `projects/README.md` and `AGENTS.md`).

## What This Architecture Is Not

To avoid overstating the project: there are no services, APIs, pipelines, scripts, schemas, or generated artifacts in the repository. Automation is explicitly deferred to V2 ([Blueprint §15](../PROJECT_CENTER_BLUEPRINT.md)).
