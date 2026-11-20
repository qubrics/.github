# Published SDK and MCP profile defaults — #1090

Live/origin profile at c860eb9d still recommended the Ruby `sendmux-sdk` pointer and described a local `sendmux-mcp` without its ecosystem. The earlier audit fix preserved compatibility names; the published Ruby/Python releases now make that recommendation stale.

Official registry readbacks on20November2026 confirmed:

- https://rubygems.org/api/v1/gems/qubrics-sdk.json — name `qubrics-sdk`, version `3.0.0`.
- https://pypi.org/pypi/qubrics-mcp/json — name `qubrics-mcp`, version `3.0.0`.
- https://registry.npmjs.org/sendmux-mcp/latest — name `sendmux-mcp`, version `1.0.0`.

Smallest origin fix: change the Ruby package link and make the Python/Node.js MCP packages explicit in `profile/README.md`. Preserve the Node package name and every other published or held compatibility name. No announcement or package release.

Verification: old recommendations observed in the ordinary raw main response before editing; exact new links checked against official registries. `git diff --check` is the local gate; unchanged YAML validation runs in required PR CI. No rename-only test or harness added for two Markdown rows. Normal merge publishes the profile; rollback is revert of this PR. Live organisation HTML and raw main readback remain publication checks after merge.
