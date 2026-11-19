# Organisation profile and policies

Tracks qubrics/qubrics #1090 and #1091. Source prepared; merge and live readback remain coordinated by the parent rebrand task.

## Cause and change

The active organisation profile reads `profile/README.md`; its introduction, product links and first-choice npm packages retained Sendmux copy. Update the Qubrics display name and canonical links, prefer published `@qubrics/sdk`, `@qubrics/cli`, `@qubrics/ai-sdk` and `qubrics/sdk`, and retain published compatibility package names for the remaining ecosystems. No package, command or public route is renamed.

`SUPPORT.md` and `SECURITY.md` retained the old contact address. Canonical product contact is `contact@qubrics.com` in qubrics/docs `docs.json:506`; approved security contact is `security@qubrics.com` in `developer-tools/sdks/versioning-support.mdx:49`. Security scope now names Qubrics repositories. Mail routing is unchanged.

## Verification

- GitHub's ordinary `POST /markdown` GFM response renders the updated profile and both policies. Responses are retained under `.claude/artifacts/rebrand-audit-fixes-ecosystem/{profile,support,security}-render.html` in the owning local checkout.
- Registry responses verified npm `@qubrics/sdk` 3.0.0, `@qubrics/cli` 2.0.0, `@qubrics/ai-sdk` 1.0.0 and Packagist `qubrics/sdk` v3.0.0.
- PyPI `qubrics-sdk` and `langchain-qubrics`, and RubyGems `qubrics-sdk`, returned 404. Released `sendmux-sdk` 3.0.1 on PyPI, `langchain-sendmux` 0.4.0 and `sendmux-sdk` 2.0.0 on RubyGems remain accurate defaults. Go and Rust compatibility identifiers are unchanged.
- Canonical marketing and app URLs return HTTP 200; the A2A Agent Card response names Qubrics A2A.
- `git diff --check` passed. Text-only change adds no executable logic or tests; repository YAML validation runs in CI.
- Fresh-reader critique passed without a rewrite. One humanize pass preserved the exact names, contacts, URLs, published package choices and existing claims.

## Release and rollback

Normal lane: merge the reviewed source PR to `qubrics/.github` main, then read the public organisation profile and policy responses. Source rollback: revert this PR. No registry publication or announcement is needed. This evidence does not claim the unmerged source is live.
