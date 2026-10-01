# Plan — Project Center

> Implements [spec.md](./spec.md). The phases come from [Blueprint §16](../../PROJECT_CENTER_BLUEPRINT.md). Status is based on the repository evidence documented in [project-context.md](../project-context.md).

## Delivery Model

Work follows an intent → spec → plan → tasks → validate loop. Human contributors and AI agents follow the same rules ([`AGENTS.md`](../../AGENTS.md)):

1. **Intent:** state why the change matters ([intent.md](./intent.md)).
2. **Spec:** express it as requirements and acceptance criteria ([spec.md](./spec.md)).
3. **Plan:** break it into small, reviewable tasks (this file).
4. **Implement:** make Markdown-only changes on a feature branch.
5. **Validate:** run the manual checklist in spec §5 and `git diff --check`.
6. **Review:** open a PR with a `docs:` commit and an explanation of changed sections and any `INDEX.md` updates, and confirm that no sensitive content was added.

## Roadmap

### Phase 1 — Define the system ✅

- [x] Choose the repository name
- [x] Define the folder structure
- [x] Define Markdown conventions
- [x] Write the founding docs (Blueprint, README, CONTRIBUTING)

### Phase 2 — Build the repository skeleton ✅

- [x] Create the repo (`2a63d9a`)
- [x] Add README, Blueprint, and INDEX
- [x] Add the project template and core folders
- [x] Add AI-agent guidelines (`AGENTS.md`, `5b59a63`)

### Phase 3 — Populate with initial content ⬜ (personal instance)

- [ ] Fill in `profile/summary.md`
- [ ] Fill in `cv/master-cv.md`
- [ ] Add 3–10 project files
- [ ] Add timeline notes

> This template intentionally ships without personal content (`5b59a63`). Phase 3 is done in a personal clone.

### Phase 4 — Standardize project ingestion 🟡

- [x] Naming conventions (`CONTRIBUTING.md`)
- [x] Chat redaction and provenance guidance (`chats/`, `sources/`)
- [ ] Documented rules for turning a chat or repository into a project file

### Phase 5 — Prepare public distribution 🟡

- [x] Public-safety rules
- [x] Empty-by-default `projects/`
- [x] Repository documentation refactor (see below)
- [ ] Decide on a license
- [ ] Publish as a GitHub template repository

### Phase 6 — Optional automation ⬜

- [ ] Automatic index generation
- [ ] CV views generated from project data
- [ ] GitHub Pages
- [ ] Import/export helpers

## Current Workstream — Repository Documentation Refactor

**Goal:** make the repository self-explanatory as a portfolio artifact **without changing the original template files**.

| Task | Output | Status |
| --- | --- | --- |
| Analyze all files and git history | Findings in `docs/project-context.md` | ✅ |
| Preserve superseded and removed originals | `docs/original/` | ✅ |
| Document information architecture | `docs/architecture.md` | ✅ |
| Document every file | `docs/content-overview.md` | ✅ |
| Record observations without applying them | `docs/possible-improvements.md` | ✅ |
| Reconstruct intent, spec, and plan | `docs/sdlc/` | ✅ |
| Replace the root README with a professional overview | `README.md` | ✅ |
| Validate links and `git diff --check` | Manual | ✅ |

**Constraint:** all original template files (`PROJECT_CENTER_BLUEPRINT.md`, `INDEX.md`, `CONTRIBUTING.md`, `AGENTS.md`, `docs/repository-rules.md`, `profile/`, `cv/`, `projects/`, `timeline/`, `chats/`, `sources/`, `templates/`) remain byte-for-byte unchanged.

## Risks

From [Blueprint §18](../../PROJECT_CENTER_BLUEPRINT.md): over-documenting early, mixing public and confidential content, premature automation, inconsistent formatting, and the repository becoming an abandoned archive. Mitigation: keep changes small, template-driven, and reviewed against spec §5.
