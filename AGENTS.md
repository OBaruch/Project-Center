# Repository Guidelines

## Project Structure & Module Organization
This repository is a Markdown-first portfolio system. Core navigation lives in `README.md`, `INDEX.md`, `PROJECT_CENTER_BLUEPRINT.md`, and `CONTRIBUTING.md`. Content is organized by purpose: `profile/` for the public summary, `cv/` for the master CV, `projects/` for user-added project files, `timeline/` for milestones, `chats/` for redacted summaries, `sources/` for provenance notes, `templates/` for reusable Markdown starters, and `docs/` for repository rules. In the template, `projects/` is kept empty except for instructions, and Markdown files there are ignored by default.

## Build, Test, and Development Commands
There is no build pipeline in this repository; contributors work directly in Markdown.

- `rg --files` lists all tracked docs quickly.
- `rg "project-name" projects INDEX.md` verifies that a project file and index entry stay aligned.
- `git diff --check` catches trailing whitespace and malformed patches before commit.
- `git status` confirms the exact files changed for review.

Preview Markdown locally in your editor before opening a pull request.

## Coding Style & Naming Conventions
Use Markdown as the source of truth. Keep one `#` heading per file, then organize content with clear `##` and `###` sections. Prefer short paragraphs and scan-friendly bullets. Use relative links where possible.

Project files in `projects/` should use lowercase kebab-case, for example `projects/ai-finance-dashboard.md`. Keep summaries factual, durable, and specific. Separate facts, outcomes, and reflections instead of mixing them into free-form notes. If you want project files versioned in your own fork, update `projects/.gitignore` first.

## Testing Guidelines
There is no automated test suite. Validation is manual:

- confirm new or updated project files follow `templates/project-template.md`,
- update `INDEX.md` when adding important content,
- check links and filenames for consistency,
- review all content for public-safe wording and redaction.

## Commit & Pull Request Guidelines
The current history is minimal (`init`), so follow the documented `docs:` convention from `CONTRIBUTING.md`. Examples: `docs: add new project file`, `docs: update master cv`, `docs: refine profile summary`.

Pull requests should include a brief description of changed sections, note any required `INDEX.md` updates, and confirm that no secrets, client data, or raw private chats were introduced. Add screenshots only when Markdown rendering or formatting needs review.

## Security & Content Safety
Treat this repository as public by default. Never commit secrets, API keys, confidential client material, legal/tax documents, or unreviewed raw chat exports. Summarize and redact first.
