# Possible Improvements

> **None of these improvements have been applied.** The original template files are deliberately preserved as authored, to keep their historical context and the original design approach. This list is only a set of observations for future work.

## Consistency issues

| # | Observation | Location |
| --- | --- | --- |
| 1 | The repository tree in the original README does not list `AGENTS.md` (added later in `5b59a63`) | [`original/original-readme.md`](./original/original-readme.md) |
| 2 | `AGENTS.md` says the history is "minimal (`init`)", which became outdated once its own commit was added | [`AGENTS.md`](../AGENTS.md) |
| 3 | Blueprint §14 expects "a few real example projects" in V1, but the template ships with none | [`PROJECT_CENTER_BLUEPRINT.md`](../PROJECT_CENTER_BLUEPRINT.md) |
| 4 | Blueprint §10 architecture omits `AGENTS.md` and `projects/.gitignore` | [`PROJECT_CENTER_BLUEPRINT.md`](../PROJECT_CENTER_BLUEPRINT.md) |
| 5 | `INDEX.md` "Core documents" does not link `AGENTS.md` | [`INDEX.md`](../INDEX.md) |
| 6 | Blueprint §7 recommends naming the template `project-center-template`, but the repo is `Project-Center` | Repository name |

## Template usability

- Placeholder links (`./projects/project-name.md`, `../projects/project-name.md`) are broken until a user creates the files. A short note next to them could prevent confusion.
- The Blueprint contains some owner-specific advice (§7 "For your use case…", §20 "Your CV, projects…"). A cloned template might separate the generic blueprint from the author's personal notes.
- There is no worked example for `timeline/`, `chats/`, or `sources/`. The removed [example project](./original/original-project-center-example.md) could be offered as `templates/example-project.md`.
- A `LICENSE` file is absent. That limits reuse as a public template.

## Optional V2 ideas already listed in the Blueprint

These come from [Blueprint §15](../PROJECT_CENTER_BLUEPRINT.md) and are listed here only for completeness: static site / GitHub Pages, automatic index generation, résumé generation from project data, tag navigation, search, YAML front-matter metadata, JSON/YAML mirrors, AI-assisted summarization and import helpers.

## Lightweight validation (if ever wanted)

- A Markdown link checker would catch broken relative links.
- A small script could verify that each `projects/*.md` file appears in `INDEX.md` (today this is a manual `rg` check in `AGENTS.md`).

These would add tooling, which the Blueprint deliberately postpones ("Validate the structure first", §18).
