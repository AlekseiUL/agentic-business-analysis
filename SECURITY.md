# Security Policy

## Scope

This repository is a Markdown-only methodology and Hermes-style skill package. It does not ship executable code, services, credentials, or infrastructure.

Security issues can still exist in the form of unsafe automation advice, prompt-injection-prone workflows, privacy leaks, or templates that encourage excessive access.

## Please report

Report an issue if you find:

- leaked secrets, local paths, or private/internal context;
- instructions that request API keys, passwords, session files, private keys, or production credentials;
- advice that encourages autonomous legal, medical, financial, public, destructive, or client-facing actions without approval;
- weak privacy guidance around client data, PII, exports, logs, or retention;
- prompt-injection risks in agent workflows;
- broken install instructions that could lead users to copy unsafe commands.

## Do not report as security issues

- general methodology disagreements;
- requests for new industry examples;
- wording preferences;
- implementation support for a specific CRM, workflow engine, or agent framework.

Use regular issues for those.

## Safe automation baseline

Human approval should be required before:

- client-facing messages;
- public publishing;
- discounts, invoices, payments, refunds;
- legal/formal claims;
- medical, financial, or legal advice;
- deletion, migration, or destructive admin actions;
- access/security/configuration changes.

## Data handling baseline

- Prefer anonymized samples over raw exports.
- Do not include secrets or credentials in prompts, issues, examples, or pull requests.
- Remove names, emails, phone numbers, addresses, payment details, medical data, and private notes unless strictly necessary.
- Use read-only access during audit wherever possible.
- Define retention and deletion rules for pilot data.
