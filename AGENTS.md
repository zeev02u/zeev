# Repository Guidelines

## Project Structure & Module Organization

This repository is currently minimal, so keep new work organized from the start. Place application source code under `src/`, tests under `tests/`, and static or generated assets under `assets/` when needed. Use a clear module layout that mirrors the product area being implemented, for example `src/auth/`, `src/ui/`, and `tests/auth/`.

Avoid placing implementation files at the repository root. Reserve the root for project metadata and documentation such as `README.md`, `AGENTS.md`, package manifests, build files, and environment examples.

## Build, Test, and Development Commands

No build or test tooling is defined yet. When adding a language or framework, document the exact commands here and in `README.md`.

Common examples:

```sh
npm install      # install JavaScript dependencies
npm run dev      # start a local development server
npm test         # run the test suite
```

If using another stack, prefer standard commands such as `make test`, `pytest`, `go test ./...`, or `cargo test`.

## Coding Style & Naming Conventions

Follow the formatter and linter conventions of the chosen stack. Add configuration files such as `.editorconfig`, `.prettierrc`, `eslint.config.*`, `pyproject.toml`, or equivalent before the codebase grows.

Use descriptive names. Prefer `kebab-case` for file and directory names in web projects, `snake_case` for Python modules, and `PascalCase` for exported classes or components where the language convention expects it. Keep modules focused and avoid mixing unrelated responsibilities in one file.

## Testing Guidelines

Add tests with each behavior change. Keep test files close to the feature they validate or mirror the `src/` tree inside `tests/`. Use recognizable names such as `*.test.ts`, `*.spec.ts`, `test_*.py`, or the default convention of the selected framework.

Tests should cover expected behavior, edge cases, and regressions for fixed bugs. Document any required services, fixtures, or environment variables.

## Commit & Pull Request Guidelines

This directory is not currently initialized as a Git repository, so no existing commit convention is available. Once Git is used, prefer short imperative commit messages, for example `Add login validation` or `Fix report export path`.

Pull requests should include a brief summary, testing notes, linked issues when applicable, and screenshots or recordings for visible UI changes. Keep changes scoped so reviewers can understand the intent quickly.

## Security & Configuration Tips

Do not commit secrets, credentials, private keys, or local environment files. Use `.env.example` to document required configuration keys and keep real values in ignored local files.
