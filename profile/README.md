# Sendmux

Sendmux is an email API for AI agents and developers. Create programmable inboxes, send and receive email, parse inbound messages into structured JSON, route across providers, and automate email workflows.

**[Get a free email inbox API for AI agents](https://myagent.mx).**

## Start here

| Need | Link |
| --- | --- |
| Get a free email inbox API for AI agents | [myagent.mx](https://myagent.mx) |
| Learn about Sendmux | [sendmux.ai](https://sendmux.ai) |
| Use the product | [app.sendmux.ai](https://app.sendmux.ai) |
| Read the docs | [sendmux.ai/docs](https://sendmux.ai/docs) |
| Manage API keys | [API keys guide](https://sendmux.ai/docs/account/api-keys) |
| Install the CLI | [Homebrew tap](https://github.com/Sendmux/homebrew-tap) (`brew install sendmux/tap/sendmux`) |
| Browse all SDKs and tools | [Sendmux SDK monorepo](https://github.com/Sendmux/sendmux-sdk) |
| Get support | [Support policy](https://github.com/Sendmux/.github/blob/main/SUPPORT.md) |
| Report a vulnerability | [Security policy](https://github.com/Sendmux/.github/blob/main/SECURITY.md) |

## SDKs and developer tools

| Language or tool | Package |
| --- | --- |
| TypeScript | [`@sendmux/sdk`](https://www.npmjs.com/package/@sendmux/sdk) |
| Python | [`sendmux-sdk`](https://pypi.org/project/sendmux-sdk/) |
| Go | [`sendmux.ai/go/v3`](https://pkg.go.dev/sendmux.ai/go/v3) |
| Rust | [`sendmux`](https://crates.io/crates/sendmux) (`cargo add sendmux`) |
| PHP | [`sendmux/sdk`](https://packagist.org/packages/sendmux/sdk) |
| Ruby | [`sendmux-sdk`](https://rubygems.org/gems/sendmux-sdk) |
| CLI | [Homebrew](https://github.com/Sendmux/homebrew-tap) or [`@sendmux/cli`](https://www.npmjs.com/package/@sendmux/cli) |

The SDK monorepo also contains focused packages for sending, mailbox, and management workflows.

## AI framework integrations

| Framework | Integration | Install |
| --- | --- | --- |
| Vercel AI SDK | [`@sendmux/ai-sdk`](https://www.npmjs.com/package/@sendmux/ai-sdk) provides tools for agent inboxes and sending | `npm install @sendmux/ai-sdk ai zod` |
| LangChain | [`langchain-sendmux`](https://pypi.org/project/langchain-sendmux/) provides a Sendmux toolkit for agent inboxes and sending | `pip install langchain-sendmux` |

## Agent protocols and tools

| Surface | What it provides | Link |
| --- | --- | --- |
| Model Context Protocol (MCP) | Hosted OAuth access and a local `sendmux-mcp` package for mailbox, management, and sending tools | [MCP docs](https://sendmux.ai/docs/ai-integrations/mcp) |
| Agent2Agent (A2A) Protocol 1.0 | A hosted OAuth-protected HTTP+JSON agent for mailbox, management, and sending operations | [A2A docs](https://sendmux.ai/docs/ai-integrations/a2a) and [Agent Card](https://a2a.sendmux.ai/.well-known/agent-card.json) |
| Agent skills | Installable Sendmux workflows for coding agents | [Sendmux skills](https://github.com/Sendmux/skills) |

## Why Sendmux

Email platforms were built for people clicking send, not agents and product workflows that need to send, receive, route, and react to email from code.

Sendmux covers outbound delivery, programmable inboxes, provider routing, delivery monitoring, and workflow automation in the same workspace.

- **Send and receive email.** Send through API or SMTP, receive into programmable mailboxes, and manage product email workflows from the same workspace.
- **Bring your providers.** Connect Gmail, Outlook, SendGrid, Mailgun, Resend, Amazon SES, or any SMTP-compatible provider. Sendmux handles routing, failover, monitoring, and quota guardrails.
- **Parse inbound email for agents.** Incoming email becomes structured JSON, including the subject, body, attachments, headers, and metadata.
- **Monitor delivery.** Delivery logs, bounces, complaints, webhooks, and provider health monitoring show what happened and help teams respond quickly.
- **Weekly reconnect digest (planned).** Active team owners and admins who can manage accounts can receive an email and bell digest of accounts that still need reconnecting. Each team gets at most one digest a week. Reconnected or deleted accounts are excluded before delivery. Notices link to Accounts. The **Accounts needing reconnection** item in notification settings has its own Email and In-app controls.

## Contributing

Organisation defaults live in this repository and apply to Sendmux repositories that do not define their own files.

- Read the [contributing guidelines](https://github.com/Sendmux/.github/blob/main/CONTRIBUTING.md) before opening a pull request.
- Use the issue templates so maintainers receive the details needed to triage quickly.
- Never paste API keys, passwords, tokens, webhook secrets, customer data, or private account details into GitHub.
- Report vulnerabilities through the [security policy](https://github.com/Sendmux/.github/blob/main/SECURITY.md), not public issues.
