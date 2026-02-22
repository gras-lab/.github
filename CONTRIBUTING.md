# Contributing to gras-lab

Thank you for your interest in contributing to **gras-lab**! This document outlines the standards and workflow we expect all contributors to follow. Please read it carefully before opening an issue or submitting a pull request.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Reporting Bugs](#reporting-bugs)
- [Requesting Features](#requesting-features)
- [Development Workflow](#development-workflow)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Code Style](#code-style)
- [Testing](#testing)

---

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](./CODE_OF_CONDUCT.md). Please read it before contributing.

---

## Getting Started

1. **Fork** the repository you want to contribute to.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
3. **Add the upstream remote:**
   ```bash
   git remote add upstream https://github.com/gras-lab/<repo-name>.git
   ```
4. **Install dependencies** following the instructions in the repository's own `README.md`.
5. **Create a branch** for your work (see [Development Workflow](#development-workflow)).

---

## Reporting Bugs

Before opening a new issue, please search existing issues to avoid duplicates. If you find a confirmed bug, use the **Bug Report** template when creating a new issue. Include as much detail as possible — environment, steps to reproduce, expected vs. actual behavior, and any relevant logs.

---

## Requesting Features

Feature requests are welcome. Use the **Feature Request** template and describe:

- The problem you are trying to solve
- Your proposed solution
- Any alternatives you have considered

We evaluate requests based on alignment with the project's goals and maintainability.

---

## Development Workflow

We use a **feature branch** workflow. All work happens on branches — never directly on `main`.

```
main          ← always stable, deployable
  └── feat/my-feature
  └── fix/login-crash
  └── chore/update-deps
  └── docs/improve-readme
```

### Branch Naming

| Type        | Pattern                   | Example                    |
|-------------|---------------------------|----------------------------|
| Feature     | `feat/<short-description>`  | `feat/user-authentication` |
| Bug fix     | `fix/<short-description>`   | `fix/null-pointer-login`   |
| Chore       | `chore/<short-description>` | `chore/update-node`        |
| Docs        | `docs/<short-description>`  | `docs/api-reference`       |
| Refactor    | `refactor/<description>`    | `refactor/db-layer`        |

**Keep branches short-lived.** If a branch diverges significantly from `main`, rebase regularly:

```bash
git fetch upstream
git rebase upstream/main
```

---

## Commit Message Guidelines

We follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification. Every commit message must have the form:

```
<type>(<optional scope>): <short summary>

[optional body]

[optional footer(s)]
```

### Types

| Type       | When to use                                     |
|------------|-------------------------------------------------|
| `feat`     | A new feature                                   |
| `fix`      | A bug fix                                       |
| `docs`     | Documentation changes only                      |
| `style`    | Formatting, missing semicolons (no logic change) |
| `refactor` | Code change that is neither a fix nor a feature |
| `test`     | Adding or correcting tests                      |
| `chore`    | Build process, dependency updates, tooling      |
| `ci`       | CI/CD configuration changes                     |
| `perf`     | Performance improvements                        |

### Rules

- Use the **imperative mood** in the summary: `add feature` not `added feature`
- Keep the summary line under **72 characters**
- Reference issues in the footer: `Closes #42`
- Breaking changes must include `BREAKING CHANGE:` in the footer

**Good examples:**

```
feat(auth): add JWT refresh token rotation

fix(api): handle null response from upstream service

Closes #37

chore: upgrade Node.js to v22 LTS
```

---

## Pull Request Guidelines

1. **One PR per logical change.** Do not bundle unrelated changes.
2. **Fill in the PR template** completely — incomplete PRs will be returned for revision.
3. **Target the correct base branch** (usually `main`).
4. **Keep PRs small and focused.** Aim for fewer than 400 lines of change per PR where possible.
5. **All CI checks must pass** before a PR can be merged.
6. **At least one approval** from a maintainer is required.
7. **Resolve all review comments** before requesting a re-review.
8. **Do not force-push** to a branch that is under active review.

---

## Code Style

Each repository may define its own linter and formatter configuration. In general, we follow these principles across all gras-lab projects:

- **DRY (Don't Repeat Yourself):** Extract reusable logic into shared utilities.
- **Clarity over cleverness:** Write code that is easy to read and reason about.
- **English only** for all comments, variable names, and documentation.
- **Explicit over implicit:** Avoid magic numbers, magic strings, and hidden side effects.
- Run the project's lint and format commands before committing.

---

## Testing

- Every bug fix must include a regression test that reproduces the bug.
- Every new feature must include unit and/or integration tests.
- All tests must pass locally before opening a PR.
- Aim for meaningful coverage, not coverage for its own sake.

---

Thank you for contributing to gras-lab. We appreciate your time and effort.
