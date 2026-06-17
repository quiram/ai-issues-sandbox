# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is a sandbox for experimenting with AI-assisted workflows across the SDLC. Experiments produce hands-on examples and notes that feed documentation and presentations for engineering teams evaluating AI tooling.

## Structure

Experiments are organized by scenario, each in its own directory. A scenario typically includes a setup, a problem to solve or task to perform, and notes on what worked, what didn't, and what was surprising.

### `linting/`

Tests AI-based linting ideas. Subdirectories are organized by file type:

- `linting/markdown/` — linting experiments specific to Markdown files

Each file within a subdirectory focuses on a single linting idea and follows this structure:

```markdown
# <RULE_ID> — <Rule title>

Rules under test: [<RULE_ID>](<link to rule documentation>)

<One or two sentences describing what violation(s) the file demonstrates.>

... content with intentional violations ...
```

- **Markdown**: rule IDs and doc links come from [markdownlint](https://github.com/DavidAnson/markdownlint/tree/main/doc) (e.g., `MD013`, `MD041`)

## CI / GitHub Actions

`.github/workflows/ai-lint-fix.yml` runs on every PR and:

1. Uses Moon's `--affected` flag to detect which projects changed.
2. Runs the `lint` task for any affected projects.
3. If violations are found, invokes `anthropics/claude-code-action` with the linter output as the prompt.
4. Commits and pushes Claude's fixes back to the PR branch.

**Required secret:** `CLAUDE_CODE_OAUTH_TOKEN` must be set in the repository's GitHub Actions secrets. Generate it with `claude setup-token` (requires Claude Pro or Max).

## Audience

Content produced here targets engineering teams adopting AI tooling — keep examples realistic and grounded in actual outcomes rather than idealized results.
