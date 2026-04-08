# Contributing to StefShield

Thank you for your interest in contributing.
This guide applies to all repositories under the [StefShield](https://github.com/stefshield) organization.
Every contribution, no matter how small, is appreciated and valued.

Please read this document before opening an issue or submitting a pull request.


## Table of Contents

- [Ways to Contribute](#ways-to-contribute)
- [Code of Conduct](#code-of-conduct)
- [Communication](#communication)
- [Getting Started](#getting-started)
- [Branching Strategy](#branching-strategy)
- [Commit Messages](#commit-messages)
- [Code Style](#code-style)
- [Tests](#tests)
- [Pull Requests](#pull-requests)
- [CI and Quality Checks](#ci-and-quality-checks)
- [Reporting Issues](#reporting-issues)


## Ways to Contribute

You don't need to write code to contribute. You can help by:

- Improving documentation
- Reporting bugs
- Suggesting features
- Reviewing pull requests
- Improving tests
- Sharing feedback

All contributions are welcome.


## Code of Conduct

By participating in any StefShield project, you agree to our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.


## Communication

- Be respectful and constructive
- Assume good intent
- If feedback is unclear, ask for clarification


## Getting Started

1. **Fork** the repository and clone your fork locally
2. **Install dependencies** following the instructions in the project's `README.md`
3. **Create a branch** from `main` using the naming conventions described below
4. **Make your changes** and commit them following the commit guidelines
5. **Push your branch** and open a pull request

If you are unsure where to start:

- Issues labeled `good first issue` are ideal for beginners
- Issues labeled `help wanted` are open for contributions but may require more context


## Branching Strategy

All work happens on short-lived branches off `main`.

The `main` branch is always stable and deployable — never commit directly to it.

Use the following prefixes for your branch name:

| Prefix                        | When to use                  |
| ----------------------------- | ---------------------------- |
| `feature/<small-description>` | New features or enhancements |
| `fix/<small-description>`     | Bug fixes                    |
| `docs/<small-description>`    | Documentation changes only   |

**Examples:**

```
feature/add-retry-logic
fix/null-pointer-on-startup
docs/update-installation-guide
```

Keep branches short-lived. If a branch lives longer than a few days, consider breaking the work into smaller pull requests.


## Commit Messages

All commits must follow the [Conventional Commits](https://www.conventionalcommits.org) specification.
This keeps the history readable and enables automated tooling.

**Format:**

```
<type>(<scope>): <short summary>
```

**Common types:**

| Type       | When to use                                     |
| ---------- | ----------------------------------------------- |
| `feat`     | A new feature                                   |
| `fix`      | A bug fix                                       |
| `docs`     | Documentation only                              |
| `test`     | Adding or updating tests                        |
| `refactor` | Code change that is neither a fix nor a feature |
| `chore`    | Build process, dependencies, or tooling         |
| `ci`       | CI configuration changes                        |

**Examples:**

```
feat(auth): add OAuth2 support
fix(parser): handle empty input without crashing
docs(readme): clarify installation steps
```

Breaking changes must be clearly indicated:

`feat(api)!: remove deprecated authentication method`

or include:

`BREAKING CHANGE: explanation here`

Rules:

- Use the **imperative, present tense**: "add" not "added" or "adds"
- Keep the summary **under 72 characters**
- Do not end with a period

> Pull requests are merged using **squash merge**.
> Your individual commit messages still matter — they inform the final squashed commit message.


## Code Style

Follow the conventions already established in the project you are contributing to.
If the project includes a linter or formatter configuration, use it.
When in doubt, mimic the style of the surrounding code.

General rules that apply across all StefShield projects:

- Prefer clarity over cleverness
- Avoid unnecessary abstractions
- Write self-documenting code; use comments only when the _why_ is not obvious


## Tests

- All new features must include tests
- All bug fixes must include a test that reproduces the issue
- Do not reduce existing test coverage

Follow the testing conventions already used in the project.
If unsure, look at existing tests for guidance.


## Pull Requests

All changes, including those from maintainers, must go through a pull request.
Direct pushes to `main` are not allowed.

**Before opening a PR:**

- [ ] Your branch is up to date with `main`
- [ ] Your branch is rebased on top of `main` (do not merge `main` into your branch)
- [ ] Tests are added or updated where applicable
- [ ] Code is formatted and linted
- [ ] All CI checks pass locally
- [ ] The PR is focused on a single concern

After rebasing, you may need to force-push your branch:

`git push --force-with-lease`

**When opening a PR:**

- Fill out the pull request template completely
- Link any related issues using `Closes #<issue-number>` if applicable
- You are encouraged to open Draft PRs early if you want feedback before your work is complete
- Keep PRs small and focused (under ~300 lines of changes when possible) — large PRs are harder to review and may be delayed or requested to be split into smaller ones

**Review process:**

All PRs require at least one approval before merging.
For now, the project maintainer is responsible for reviewing and merging PRs.
Reviews focus on correctness, code quality, test coverage, and consistency with project conventions.

**Merge strategy:**

All PRs are merged using **squash merge** to keep the `main` history clean and linear.


## CI and Quality Checks

All pull requests must pass CI checks before they can be merged.

If CI fails, fix the issue before requesting a review.


## Reporting Issues

Before opening an issue:

1. Search existing issues to avoid duplicates
2. Use the appropriate issue template (bug report or feature request)
3. Provide enough context for the maintainer to reproduce or understand the problem

For security vulnerabilities, **do not open a public issue**.
Follow the process described in [SECURITY.md](SECURITY.md).

---

Thank you for helping make StefShield projects better.
