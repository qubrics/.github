# GitHub live references — organisation defaults

Part of qubrics/qubrics#897, spec A15. Source-only PR; no merge, publication, deployment, tombstone-org update or GitHub settings change.

Policy links, profile GitHub links and the owner-qualified Homebrew example now use the current `qubrics` organisation. SDK source points at `qubrics/qubrics-sdk`. Existing formula name, package names, product copy and service hosts remain unchanged.

Checks: `git diff --check` passed; live old-owner/repository reference search across tracked files returned no matches. No executable behaviour changed, so no tests were added.

Blocked acceptance clause: this repository has zero GitHub Actions workflows, confirmed by its tracked tree and the read-only Actions API. Existing CI cannot be reported green. No workflow was invented or configured for this documentation-only repair.

Independent review is coordinated across the batch; no review-settled claim is made here.
