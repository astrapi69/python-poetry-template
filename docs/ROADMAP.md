# Roadmap

Deliberately deferred work. Each item is its own focused change — not to be
mixed into unrelated template work.

## Open

### OIDC / Trusted Publishing (PyPI)

Migrate releases from manual token-based `poetry publish` to PyPI **Trusted
Publishing (OIDC)** via a tag-triggered GitHub Actions workflow — no long-lived
tokens or secrets.

- **Why deferred:** the token workflow works and is the established path. This
  is a conscious migration, not a drive-by change.
- **Prerequisite:** per-repo publisher configuration on PyPI (Project →
  Settings → Publishing → add a GitHub publisher: repo + workflow filename +
  environment) before the workflow can authenticate.
- **Scope:** add `.github/workflows/release.yml` (`push: tags: ['v*']`,
  `permissions: id-token: write`, `pypa/gh-action-pypi-publish`). See the
  "Automating with GitHub Actions" section in
  [`.claude/rules/release-workflow.md`](../.claude/rules/release-workflow.md).
- **Decision owner:** do as its own session.

### Backport tooling improvements to pluginforge

This template grew checks that `pluginforge` lacks: mypy, codespell in
pre-commit, a CI workflow file, and `make publish-test`. Port those back to
`pluginforge`.

- **Why deferred:** belongs in the `pluginforge` repo, not here. Keep template
  work and pluginforge work separate.
- **Scope:** own branch, own session in `pluginforge` — mypy config + strict
  pass, codespell pre-commit hook, a `ci.yml`, and the `publish-test` target.
- **Decision owner:** do as its own session, do not mix with template changes.
