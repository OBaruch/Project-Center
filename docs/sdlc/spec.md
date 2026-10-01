# Specification — Project Center

> Derived from [intent.md](./intent.md) and the existing repository. Each requirement lists its **source** and its **current status** in this template. Statuses: ✅ Met · 🟡 Partial · ⬜ Not met (by design or pending).

## 1. Scope

Project Center V1 is a Markdown-only repository template. It has no executable code. Every requirement below is satisfied by files, folder conventions, and documented rules.

## 2. Functional Requirements

| ID | Requirement | Source | Status |
| --- | --- | --- | --- |
| FR-01 | The repository SHALL provide an entry README that explains purpose, structure, workflow, and principles | `README.md` | ✅ |
| FR-02 | The repository SHALL provide a navigation index linking all core documents and featured projects | `INDEX.md` | ✅ |
| FR-03 | The repository SHALL provide a founding blueprint describing problem, goals, architecture, scope, and roadmap | `PROJECT_CENTER_BLUEPRINT.md` | ✅ |
| FR-04 | The repository SHALL provide a profile summary template | `profile/summary.md` | ✅ |
| FR-05 | The repository SHALL provide a master CV template that links experience to projects | `cv/master-cv.md` | ✅ |
| FR-06 | The repository SHALL provide a standard project template covering the fields in Blueprint §11 | `templates/project-template.md` | ✅ |
| FR-07 | Users SHALL be able to add one Markdown file per project under `projects/` | `projects/README.md` | ✅ |
| FR-08 | The template SHALL ship with `projects/` empty and user project files ignored by default | `projects/.gitignore` | ✅ |
| FR-09 | The repository SHALL provide guidance for timeline, redacted chat summaries, and source provenance | `timeline/`, `chats/`, `sources/` READMEs | ✅ |
| FR-10 | The repository SHALL document contribution, naming, and commit conventions | `CONTRIBUTING.md` | ✅ |
| FR-11 | The repository SHALL document rules for AI agents and contributors | `AGENTS.md` | ✅ |
| FR-12 | The personal instance SHOULD include 3–10 real project files | Blueprint §14, §16 Phase 3 | ⬜ Out of scope for the template |

## 3. Content Model — Project File

A project file (`projects/<kebab-case-slug>.md`) SHALL follow `templates/project-template.md`:

- **Snapshot:** Status (Idea / Active / Completed / Archived), Category, Owner, Start date, End date, Visibility, Primary links, Tags.
- **Narrative sections:** One-line summary, Context, Problem, Objective, Scope, Why it matters, My role, Users or stakeholders, Stack and tools, Architecture or workflow, Key milestones, Outcomes, Metrics or evidence, Challenges, Decisions made, Lessons learned, Next steps, References.

Allowed categories (Blueprint §12): AI, Data, Full Stack, Finance, Automation, Business, Research, Personal, Brand, Infrastructure, Experimental.

## 4. Non-Functional Requirements

| ID | Requirement | Source | Status |
| --- | --- | --- | --- |
| NFR-01 | Markdown is the single source of truth. No build step is required to read the repository | `docs/repository-rules.md` rule 1, `AGENTS.md` | ✅ |
| NFR-02 | Each file has exactly one H1, with content organized under H2/H3 | `docs/repository-rules.md`, `AGENTS.md` | ✅ |
| NFR-03 | Links between documents are relative | `docs/repository-rules.md` | ✅ |
| NFR-04 | Project filenames use lowercase kebab-case | `CONTRIBUTING.md` | ✅ |
| NFR-05 | Commits follow the `docs:` convention | `CONTRIBUTING.md`, `AGENTS.md` | 🟡 First commit is `init` |
| NFR-06 | No secrets, client data, legal or tax documents, or raw chats are committed | `CONTRIBUTING.md`, `AGENTS.md` | ✅ |
| NFR-07 | Structure stays stable so the template remains reusable | `docs/repository-rules.md` rule 7 | ✅ |
| NFR-08 | Content is structured so AI tools can summarize and transform it | Blueprint §9 | ✅ |

## 5. Acceptance Criteria (manual validation)

From `AGENTS.md` → Testing Guidelines:

- [ ] New or updated project files follow `templates/project-template.md`.
- [ ] `INDEX.md` is updated when important content is added (`rg "<slug>" projects INDEX.md`).
- [ ] Links and filenames are consistent.
- [ ] All content uses public-safe wording and is redacted.
- [ ] `git diff --check` passes.

## 6. Out of Scope (V1)

Static site generation, automatic indexing, résumé generation, tag navigation, search, GitHub Pages, metadata headers, JSON/YAML mirrors, AI summarization scripts, import helpers. These are all listed as V2 in Blueprint §15.

## 7. Open Questions

- Should the template include a filled-in example project (see [original example](../original/original-project-center-example.md))?
- Should a `LICENSE` be added to support reuse as a public template?
- Should the Blueprint's owner-specific advice be separated from the generic template?
