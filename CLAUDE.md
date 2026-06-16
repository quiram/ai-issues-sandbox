# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is a sandbox for experimenting with AI-assisted workflows across the SDLC. Experiments produce hands-on examples and notes that feed documentation and presentations for engineering teams evaluating AI tooling.

## Structure

Experiments are organized by scenario, each in its own directory. A scenario typically includes a setup, a problem to solve or task to perform, and notes on what worked, what didn't, and what was surprising.

### `linting/`

Tests AI-based linting ideas. Subdirectories are organized by file type:

- `linting/markdown/` — linting experiments specific to Markdown files

Each file within a subdirectory focuses on a single linting idea. Files must open with a header section that declares the rule(s) under test using the standard nomenclature of the relevant linting tool:

- **Markdown**: use [markdownlint rule IDs](https://github.com/markdownlint/markdownlint/blob/main/docs/RULES.md) (e.g., `MD013`, `MD041`)

## Audience

Content produced here targets engineering teams adopting AI tooling — keep examples realistic and grounded in actual outcomes rather than idealized results.
