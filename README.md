# Project Center

A Markdown-first repository template to centralize projects, CV, timeline, portfolio, and professional context in one reusable public system.

## Project Overview

Project Center is a documentation system, not an application. It gives a person one version-controlled home for their profile, master CV, project files, milestones, and the provenance of that information. It uses a fixed folder structure and a standard project template, so the content stays consistent, easy to present, and easy for both humans and AI tools to reuse.

## Project Context

- **Type:** Personal Project (repository template)
- **Author:** Baruch López
- **Created:** March 2026 (two commits on 2026-03-17)
- **Status:** V1 skeleton complete. It ships intentionally empty so it can be cloned.

Evidence and history: [docs/project-context.md](./docs/project-context.md).

## Problem Statement

Builders produce work across AI chats, GitHub repositories, cloud and VPS tools, LinkedIn, several CV versions, and loose notes. Without a single source of truth, project history gets lost, portfolios stay weak, and every CV update repeats the same work.

## Objective

Provide a simple, minimalist, public, and reusable structure where every project becomes a structured Markdown file, every milestone is recorded, and the whole profile is portable and versioned.

## Repository Structure

```text
.
├── README.md                     # This overview
├── INDEX.md                      # Public navigation hub
├── PROJECT_CENTER_BLUEPRINT.md   # Founding design document
├── CONTRIBUTING.md               # Adoption, naming, and commit conventions
├── AGENTS.md                     # Guidelines for contributors and AI agents
├── profile/                      # Public profile summary
├── cv/                           # Master CV (source of truth)
├── projects/                     # One file per project (git-ignored by default)
├── timeline/                     # Milestones over time
├── chats/                        # Redacted summaries extracted from chats
├── sources/                      # Provenance registry
├── templates/                    # Project template
└── docs/                         # Rules, project documentation, intent/spec/plan
    ├── sdlc/                     # intent.md · spec.md · plan.md
    └── original/                 # Original README and files recovered from history
```

## Original Implementation

This repository preserves the original implementation of the project. The template files (blueprint, index, contributing guide, agent guidelines, repository rules, and every content folder) have intentionally not been refactored or modernized, in order to retain the historical context and original design approach. They represent the original implementation developed as a personal project.

The only replaced file is this `README.md`. Its original version is preserved verbatim at [docs/original/original-readme.md](./docs/original/original-readme.md).

## Technologies

- Markdown
- Git and GitHub

There are no programming languages, frameworks, dependencies, or build tools in the repository.

## How It Works

1. Describe yourself in [`profile/summary.md`](./profile/summary.md).
2. Record your full experience in [`cv/master-cv.md`](./cv/master-cv.md).
3. Copy [`templates/project-template.md`](./templates/project-template.md) to `projects/<kebab-case-name>.md` for each project and fill it in.
4. Use `timeline/`, `chats/` (summarized and redacted only), and `sources/` for milestones and provenance.
5. Link every important project from [`INDEX.md`](./INDEX.md), the public navigation layer.

Project files are ignored by [`projects/.gitignore`](./projects/.gitignore) so the template stays empty. Edit that rule in your fork to version your own projects.

## Architecture

The repository is an information architecture with navigation, governance, identity, work, and provenance layers, connected by relative links. See [docs/architecture.md](./docs/architecture.md).

## Inputs and Outputs

- **Inputs:** manually summarized content from chats, repositories, CVs, LinkedIn, notes, and other tools.
- **Outputs:** a navigable public portfolio, and reusable material for CVs, bios, websites, and applications.

## Running the Project

There is nothing to run or build. Read the files in any Markdown viewer or on GitHub. The validation commands used by contributors (from [`AGENTS.md`](./AGENTS.md)) are:

```bash
rg --files                             # list tracked docs
rg "project-name" projects INDEX.md    # check that a project and its index entry match
git diff --check                       # catch whitespace errors before committing
```

## Documentation

- [Blueprint](./PROJECT_CENTER_BLUEPRINT.md) · [Index](./INDEX.md) · [Contributing](./CONTRIBUTING.md) · [Agent Guidelines](./AGENTS.md)
- [Documentation index](./docs/README.md)
- [Project Context](./docs/project-context.md) · [Architecture](./docs/architecture.md) · [Content Overview](./docs/content-overview.md) · [Possible Improvements](./docs/possible-improvements.md)
- [Intent](./docs/sdlc/intent.md) · [Specification](./docs/sdlc/spec.md) · [Plan](./docs/sdlc/plan.md)

## Public Template Note

If you publish your own copy, remove any sensitive, confidential, or non-public information first. Never commit secrets, API keys, client data, legal or tax documents, or unreviewed raw chats.

## Historical Note

This repository was later reorganized and documented to improve readability and preserve the historical context of the original project. The original template files remain unchanged.
