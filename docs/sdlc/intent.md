# Intent — Project Center

> Reverse-engineered from the existing repository (commits `2a63d9a`, `5b59a63`). This file records **why** the system exists. [spec.md](./spec.md) records **what** it must be, and [plan.md](./plan.md) records **how and when** it is delivered.

## Intent Statement

Give a multidisciplinary builder **one structured, version-controlled, public home** for their projects, career record, and professional narrative. It should be written in plain Markdown, readable by both humans and AI tools, and simple enough for anyone to clone and adapt.

## Problem

Work is fragmented across AI chat workspaces, GitHub repositories, VPS and cloud tools, LinkedIn, multiple CV versions, and scattered notes. There is no single source of truth, no structured historical memory, and every CV or portfolio update duplicates effort. *(Source: [Blueprint §2](../../PROJECT_CENTER_BLUEPRINT.md))*

## Target Users

- **Primary:** the repository owner, a builder with many parallel initiatives.
- **Readers:** recruiters, collaborators, clients.
- **Adopters:** developers, AI engineers, data professionals, consultants, founders, researchers, and others who clone the template. *(Source: [Blueprint §5](../../PROJECT_CENTER_BLUEPRINT.md))*
- **Agents:** AI coding and writing assistants that read and edit the repository following [`AGENTS.md`](../../AGENTS.md).

## Desired Outcomes

1. Someone can understand the owner's professional profile quickly.
2. Work is no longer fragmented.
3. Updating a CV becomes easier.
4. Projects are documented consistently.
5. Others can clone the system with minimal friction.

*(Source: [Blueprint §17](../../PROJECT_CENTER_BLUEPRINT.md))*

## Guiding Principles

Markdown-first · Human-readable · AI-friendly · Minimal by default · Public-friendly · Modular · Reusable. *(Source: [Blueprint §9](../../PROJECT_CENTER_BLUEPRINT.md))*

## Non-Goals (V1)

- Heavy automation or live integrations.
- Databases or complex schemas.
- Front-end frameworks.
- Ingesting private or confidential data.

*(Source: [Blueprint §14](../../PROJECT_CENTER_BLUEPRINT.md))*

## Constraints

- **Public by default:** no secrets, client data, legal or tax documents, or unreviewed raw chats. *(Sources: `CONTRIBUTING.md`, `AGENTS.md`)*
- **No build pipeline:** validation is manual. *(Source: `AGENTS.md`)*
- **Template stays empty:** user project files are git-ignored by default. *(Source: `projects/.gitignore`)*

## Success Signal

> "The best V1 is the one that is clean, is usable, is public, is easy to update, and already tells a compelling story." — [Blueprint §20](../../PROJECT_CENTER_BLUEPRINT.md)
