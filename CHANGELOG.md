# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Enforced PyPI release gate: `make build-check` (build + `twine check` + wheel
  inspection), `make release-check` (CI + codespell + build-check), and
  `make publish-test`. `publish`/`publish-test` run `release-check` as a hard
  prerequisite, so a red check blocks publishing.
- Release SOP at `.claude/rules/release-workflow.md` (SemVer rules, CHANGELOG
  step, TestPyPI smoke test, checklist) and this `CHANGELOG.md` scaffold.
- Registered pytest `slow` marker (paired with `--strict-markers`).
- Roadmap for deliberately deferred work at `docs/ROADMAP.md`.

### Changed

- Bumped GitHub Actions to their Node 24 majors — `actions/checkout@v7`,
  `actions/setup-python@v6`, `codecov/codecov-action@v7` — clearing the
  Node 20 deprecation warning. CI verified green across Python 3.10–3.14.

### Fixed

## [0.1.0] - 2026-06-23

### Added

- Initial template: PEP 621 `pyproject.toml`, `src/` layout, typed example CLI.
- Ruff (lint + format), mypy `strict`, codespell, pytest with branch coverage.
- Pre-commit hooks and a GitHub Actions CI matrix (Python 3.10–3.14).
- PyPI release tooling: `twine` validation, TestPyPI flow, and a release
  workflow rule under `.claude/rules/release-workflow.md`.

[Unreleased]: https://github.com/astrapi69/python-poetry-template/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/astrapi69/python-poetry-template/releases/tag/v0.1.0
