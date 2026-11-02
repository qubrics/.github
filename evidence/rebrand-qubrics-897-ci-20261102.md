# Organisation repository validation prerequisite

Goal: one checked validation-only draft PR for `qubrics/.github`.
Status: source prerequisite only; no merge, publication or deployment authorised.

## Scope and trace

- Base: fetched `origin/main` at `9e9e760e8062b6a4187b6bdd20880d41d068aea6`.
- `.github/workflows/validate.yml` runs on pull requests and pushes to `main`, with `contents: read`, no persisted checkout credentials and a five-minute job timeout.
- `.yamllint.yml` enables duplicate-key rejection. yamllint always checks YAML syntax independently of configured cosmetic rules.
- `yamllint --strict .github FUNDING.yml .yamllint.yml` checks seven YAML files: three issue forms, issue chooser configuration, funding configuration, the workflow and its native validator configuration.
- Existing product copy, policy/profile Markdown and rebrand PR [#7](https://github.com/qubrics/.github/pull/7) remain unchanged. That PR was observed at `cce072302c4b169987ecdd9d2b0514d9fd4a398b`.

## Native validation

yamllint `1.38.0` was installed in an isolated local virtual environment. No custom test harness or package manifest was added.

| Case | Native input or command | Result |
| --- | --- | --- |
| Duplicate mapping key | `printf 'name: first\nname: duplicate\n' \| yamllint --strict -` | Exit 1: `2:1 error duplication of key "name" in mapping (key-duplicates)` |
| Malformed YAML | `printf 'name: [\n' \| yamllint --strict -` | Exit 1: `2:1 error syntax error: expected the node content, but found '<stream end>' (syntax)` |
| Repository YAML | `yamllint --strict .github FUNDING.yml .yamllint.yml` | Exit 0; no warnings or errors |

Local receipts: `.claude/artifacts/rebrand-qubrics-897-ci/{install,red-duplicate,red-syntax,green}.log` in the main checkout. CI runs the same repository validation command; its authoritative result is the draft PR check for the final head.

Tests: no test files added, removed, weakened or skipped. Both native rejection cases were observed before the passing repository check.
Journeys: not applicable; no product or browser surface changes.
Review: the source diff is limited to the workflow, native validator configuration and this evidence file; no extra infrastructure or changed policy assertions.

## Sources and pins

- [yamllint installation and native usage](https://github.com/adrienverge/yamllint/blob/v1.38.0/README.rst)
- [Independent rule configuration](https://yamllint.readthedocs.io/en/stable/configuration.html)
- [Duplicate-key rule](https://yamllint.readthedocs.io/en/stable/rules.html#module-yamllint.rules.key_duplicates)
- [Syntax validation independent of configured rules](https://github.com/adrienverge/yamllint/blob/v1.38.0/yamllint/linter.py#L187)
- [yamllint 1.38.0 release](https://github.com/adrienverge/yamllint/releases/tag/v1.38.0)
- [Checkout v7.0.1](https://github.com/actions/checkout/releases/tag/v7.0.1), official tag resolved to `3d3c42e5aac5ba805825da76410c181273ba90b1`.
- [setup-python v7.1.0](https://github.com/actions/setup-python/releases/tag/v7.1.0), official tag resolved to `6d4fd22b20465ccc0f7354476588e8df7c9ca0e0`.
- [setup-python usage](https://github.com/actions/setup-python/blob/6d4fd22b20465ccc0f7354476588e8df7c9ca0e0/README.md)
- [GitHub workflow syntax](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax)

## Limits and cleanup

This prerequisite checks syntax and duplicate mappings. GitHub issue-form semantics, Markdown copy and external-link availability are outside its scope. It creates no publishing, settings or product rebrand action.

No containers, browsers, servers or production resources were created. Local tooling is temporary; the branch and worktree remain for review while the draft PR is unmerged.
