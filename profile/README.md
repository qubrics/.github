# Qubrics

Qubrics is an email API for AI agents and developers. Create programmable inboxes, send and receive email, parse inbound messages into structured JSON, route across providers, and automate email workflows.

**[Get a free email inbox API for AI agents](https://myagent.mx).**

## Start here

| Need | Link |
| --- | --- |
| Get a free email inbox API for AI agents | [myagent.mx](https://myagent.mx) |
| Learn about Qubrics | [qubrics.com](https://qubrics.com) |
| Use the product | [app.qubrics.com](https://app.qubrics.com) |
| Read the docs | [qubrics.com/docs](https://qubrics.com/docs) |
| Manage API keys | [API keys guide](https://qubrics.com/docs/account/api-keys) |
| Install the CLI | [`@qubrics/cli`](https://www.npmjs.com/package/@qubrics/cli) (`npm install -g @qubrics/cli`) |
| Browse all SDKs and tools | [Qubrics SDK monorepo](https://github.com/qubrics/qubrics-sdk) |
| Get support | [Support policy](https://github.com/qubrics/.github/blob/main/SUPPORT.md) |
| Report a vulnerability | [Security policy](https://github.com/qubrics/.github/blob/main/SECURITY.md) |

## SDKs and developer tools

| Language or tool | Package |
| --- | --- |
| TypeScript | [`@qubrics/sdk`](https://www.npmjs.com/package/@qubrics/sdk) |
| Python | [`sendmux-sdk`](https://pypi.org/project/sendmux-sdk/) |
| Go | [`sendmux.ai/go/v3`](https://pkg.go.dev/sendmux.ai/go/v3) |
| Rust | [`sendmux`](https://crates.io/crates/sendmux) (`cargo add sendmux`) |
| PHP | [`qubrics/sdk`](https://packagist.org/packages/qubrics/sdk) |
| Ruby | [`qubrics-sdk`](https://rubygems.org/gems/qubrics-sdk) |
| CLI | [`@qubrics/cli`](https://www.npmjs.com/package/@qubrics/cli) or [Homebrew](https://github.com/qubrics/homebrew-tap) |

The SDK monorepo also contains focused packages for sending, mailbox, and management workflows.

## AI framework integrations

| Framework | Integration | Install |
| --- | --- | --- |
| Vercel AI SDK | [`@qubrics/ai-sdk`](https://www.npmjs.com/package/@qubrics/ai-sdk) provides tools for agent inboxes and sending | `npm install @qubrics/ai-sdk ai zod` |
| LangChain | [`langchain-sendmux`](https://pypi.org/project/langchain-sendmux/) provides a Qubrics toolkit for agent inboxes and sending | `pip install langchain-sendmux` |

## Agent protocols and tools

| Surface | What it provides | Link |
| --- | --- | --- |
| Model Context Protocol (MCP) | Hosted OAuth access, or local Python [`qubrics-mcp`](https://pypi.org/project/qubrics-mcp/) and Node.js [`sendmux-mcp`](https://www.npmjs.com/package/sendmux-mcp) packages for mailbox, management, and sending tools | [MCP docs](https://qubrics.com/docs/ai-integrations/mcp) |
| Agent2Agent (A2A) Protocol 1.0 | A hosted OAuth-protected HTTP+JSON agent for mailbox, management, and sending operations | [A2A docs](https://qubrics.com/docs/ai-integrations/a2a) and [Agent Card](https://a2a.qubrics.com/.well-known/agent-card.json) |
| Agent skills | Installable Qubrics workflows for coding agents | [Qubrics skills](https://github.com/qubrics/skills) |

## Why Qubrics

Email platforms were built for people clicking send, not agents and product workflows that need to send, receive, route, and react to email from code.

Qubrics covers outbound delivery, programmable inboxes, provider routing, delivery monitoring, and workflow automation in the same workspace.

- **Send and receive email.** Send through API or SMTP, receive into programmable mailboxes, and manage product email workflows from the same workspace.
- **Bring your providers.** Connect Gmail, Outlook, SendGrid, Mailgun, Resend, Amazon SES, or any SMTP-compatible provider. Qubrics handles routing, failover, monitoring, and quota guardrails.
- **Parse inbound email for agents.** Incoming email becomes structured JSON, including the subject, body, attachments, headers, and metadata.
- **Monitor delivery.** Delivery logs, bounces, complaints, webhooks, and provider health monitoring show what happened and help teams respond quickly.
- **Weekly reconnect digest.** Active team owners and admins who can manage accounts can receive an email and bell digest of accounts that still need reconnecting. Each team gets at most one digest a week. Reconnected or deleted accounts are excluded before delivery. Notices link to Accounts. The **Accounts needing reconnection** item in notification settings has its own Email and In-app controls.

## Contributing

Organisation defaults live in this repository and apply to Qubrics repositories that do not define their own files.

- Read the [contributing guidelines](https://github.com/qubrics/.github/blob/main/CONTRIBUTING.md) before opening a pull request.
- Use the issue templates so maintainers receive the details needed to triage quickly.
- Never paste API keys, passwords, tokens, webhook secrets, customer data, or private account details into GitHub.
- Report vulnerabilities through the [security policy](https://github.com/qubrics/.github/blob/main/SECURITY.md), not public issues.
