---
name: agents-md-builder
description: Interview the user and inspect the current repository to create or improve its root AGENTS.md. Use when the user wants to initialize, generate, review, or update project-specific coding-agent instructions.
---

# AGENTS.md Builder

Do not touch the AGENTS.md in ~/AGENTS.md at all !!

Create a concise, project-specific `AGENTS.md` for the current repository.

Do not write the file immediately. Inspect the repository first, ask only the
questions that cannot be answered from the codebase, then show the proposed
content and wait for approval.

## Inspect

Check the high-level directory structure and any relevant files, including:

- `README.md`, existing `AGENTS.md`, and `.codex/`
- `package.json`, lockfiles, and language package files
- `src/`, `app/`, `tests/`, `docs/`, and configuration files
- `Makefile`, Docker files, and CI workflows
- lint, format, type-check, build, and test configuration

Infer the language, framework, package manager, commands, test tools,
architecture, important directories, database, API conventions, and deployment
approach. Do not ask the user about facts that the repository makes clear.

## Interview

Ask questions in small groups, about 4-6 at a time. Wait for the answers before
asking the next group.

Ask about:

1. Project purpose, primary users.
2. Architecture rules, business-logic location, abstractions to preserve, and
   patterns to avoid.
3. E2E Testing strategy
4. Safety boundaries for secrets, potential securities vulnerabilities.

## Propose and write

Before writing, show the proposed sections and ask for approval. Include at least these sections:

- Project Overview
- Tech Stack
- Repository Structure
- Development Commands
- Architecture Rules
- Coding Conventions
- Testing

Then create a local AGENTS.md file within the current project only. DO NOT CHANGE ~/AGENTS.md

## Last check when finish

- Include this instructions: "Use subagents wherever possible"
