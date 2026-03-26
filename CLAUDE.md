# CLAUDE.md

This file provides guidance to Claude Code and other AI assistants working in this repository.

---

## Repository Overview

**Repository:** odiumhex/Default
**Status:** New / empty — no project type has been established yet.

When a project is initialized here, update this file with:
- The project's purpose and a short description
- The primary language(s) and framework(s)
- Any external services or dependencies

---

## Branch Conventions

- `main` — stable, production-ready code
- `claude/<description>` — branches created by AI assistants for specific tasks
- `feat/<description>` — feature branches
- `fix/<description>` — bug fix branches
- `chore/<description>` — maintenance and tooling changes

Development branches should be short-lived. Open a pull request into `main` once work is complete; **never push directly to `main`**.

---

## Commit Message Style

Use the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<optional scope>): <short summary>

<optional body>
```

Common types: `feat`, `fix`, `chore`, `docs`, `refactor`, `test`, `ci`

Examples:
```
feat(auth): add JWT refresh token support
fix(api): handle null response from upstream service
docs: update CLAUDE.md with project structure
```

- Keep the summary line under 72 characters
- Use the imperative mood ("add" not "added")
- Reference issues/PRs in the body when relevant: `Closes #42`

---

## Development Workflow

1. **Branch** — create a branch from `main` using the naming convention above
2. **Code** — make focused, atomic changes
3. **Test** — run the test suite before committing (commands listed below once established)
4. **Lint** — run linting/formatting checks
5. **Commit** — use Conventional Commits format
6. **Push** — `git push -u origin <branch-name>`
7. **PR** — open a pull request; do not merge your own PR without review

---

## AI Assistant Guidelines

### General Principles

- Read files before editing them
- Make the minimum change needed to accomplish the task
- Do not add features, refactoring, or cleanup beyond what was asked
- Do not add comments or docstrings to code you did not change
- Prefer editing existing files over creating new ones
- Do not introduce security vulnerabilities (injection, XSS, insecure secrets, etc.)

### Before Making Changes

- Understand the existing code and conventions first
- Check for related tests and update them alongside code changes
- Verify that the change fits the existing architecture

### Committing and Pushing

- Always develop on the designated feature branch, never on `main`
- Use `git push -u origin <branch-name>` when pushing
- Do not create a pull request unless explicitly asked

### Risky Actions — Always Confirm First

The following require explicit user confirmation before proceeding:
- Deleting files or directories
- Force-pushing (`git push --force`)
- Resetting commits (`git reset --hard`)
- Dropping database tables or destructive migrations
- Modifying CI/CD pipelines
- Publishing releases or pushing to production environments

---

## Project Structure

*To be filled in once the project is initialized.*

A typical layout to follow when setting up:

```
/
├── src/              # Application source code
├── tests/            # Test files (mirrors src/ structure)
├── docs/             # Documentation
├── .github/
│   └── workflows/    # CI/CD pipeline definitions
├── CLAUDE.md         # This file
└── README.md         # Human-facing project overview
```

---

## Commands

*To be filled in once the project is initialized.* Common commands to document here:

| Purpose | Command |
|---------|---------|
| Install dependencies | `...` |
| Run tests | `...` |
| Run linter | `...` |
| Format code | `...` |
| Build | `...` |
| Start dev server | `...` |

---

## Code Style

*To be filled in once the language/framework is chosen.* Document here:

- Indentation (tabs vs spaces, width)
- Naming conventions (camelCase, snake_case, etc.)
- File naming conventions
- Import ordering rules
- Any auto-formatters in use (Prettier, Black, gofmt, etc.)

---

## Testing

*To be filled in once the test framework is chosen.* Document here:

- Test framework and runner
- Where tests live and how they are named
- How to run a single test vs the full suite
- Coverage requirements (if any)
- Conventions for mocks, fixtures, and test data

---

## Environment and Secrets

- Never commit secrets, API keys, or credentials to the repository
- Use `.env` files locally (add `.env` to `.gitignore`)
- Document required environment variables in `.env.example` (with placeholder values only)
- For CI, store secrets in GitHub Actions Secrets

---

## Updating This File

Keep this file current as the project evolves. Update it when:
- The project type or stack is decided
- New commands are added
- Conventions change
- New tools or services are integrated
