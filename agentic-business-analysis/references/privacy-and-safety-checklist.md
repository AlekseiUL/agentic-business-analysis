# Privacy and Safety Checklist

Use this before requesting client data, uploading examples to AI systems, or proposing automated actions.

## Data minimization

- Ask only for data that changes the automation design.
- Prefer anonymized samples over raw exports.
- Remove names, phone numbers, emails, addresses, payment details, medical data, legal details, and private employee/client notes unless they are strictly required.
- Do not copy full CRM/chat/database exports into prompts by default.

## Consent and access

- Confirm the client is allowed to share the data being analyzed.
- List which systems need access: CRM, messengers, email, spreadsheets, website, support tool, documents.
- Define who approves access and who can revoke it.
- Use read-only access for audit where possible.

## External AI restrictions

- Identify data that must not be sent to external AI providers.
- If sensitive data is unavoidable, propose local/private processing or redaction first.
- Never put API keys, passwords, session files, OAuth tokens, private keys, or production credentials into the analysis.

## Approval gates

Human approval is required before:

- client-facing messages;
- public publishing;
- discounts, invoices, payments, refunds;
- legal/formal claims;
- medical/financial/legal advice;
- deletion, migration, or destructive admin actions;
- access/security/configuration changes.

## Logging and retention

- Define what the agent logs and why.
- Avoid storing raw sensitive messages when summaries are enough.
- Define retention: what is kept after the pilot and what is deleted.
- Make failure/escalation cases visible to the human owner.

## Safe wording

Say “drafts”, “prepares”, “checks”, “routes”, “summarizes”, “flags”, “asks for approval”.

Avoid “fully autonomous”, “replaces employees”, “guaranteed revenue”, and “AI runs the business”.
