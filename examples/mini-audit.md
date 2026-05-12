# Mini Audit Example

This is a compact illustrative example. It is not a real case study.

## 1. Short verdict

The first pilot should be incoming lead intake and CRM hygiene, not full sales automation. The process is frequent, visible, measurable, and safe with manager approval.

## 2. Business snapshot

- Business: service agency.
- Customers: B2B clients requesting project work.
- Main channels: Telegram, website form, referrals.
- Current tools: messenger, spreadsheet CRM, shared documents.
- Main pain: leads arrive in different channels, summaries are inconsistent, follow-ups are missed.

## 3. Process lanes

### Sales / CRM

- Trigger: new lead message.
- Input: raw message, contact, project details.
- Steps: read message, ask missing questions, create CRM row, assign manager, follow up.
- Output: structured lead card and next action.
- Bottleneck: manual copy-paste and missed fields.

## 4. Top opportunities

### Lead Intake Agent — high priority

- Pain: 5/5.
- Frequency: 5/5.
- Data availability: 4/5.
- Approval fit: 5/5.
- Risk score: 4/5.
- Pilot visibility: 5/5.
- Why now: visible operational pain and low-risk draft/update workflow.

### Weekly Report Agent — medium priority

- Useful, but depends on cleaner CRM data first.

## 5. Recommended first pilot

```text
Pilot goal:
Structure incoming leads and prepare CRM updates with human approval.

Included:
- parse incoming lead text;
- extract name, company, request, budget, urgency, missing fields;
- prepare CRM row/update draft;
- flag hot or incomplete leads;
- generate daily summary.

Excluded:
- autonomous pricing;
- sending final client promises;
- discounts or contract terms;
- destructive CRM changes.

Acceptance criteria:
- 90%+ incoming leads have required fields extracted;
- daily missed-follow-up report is produced;
- manager approves every client-facing message.
```

## 6. Proposed agent contour

### Intake Agent

- Reads: Telegram/site-form lead messages.
- Produces: structured lead summary.
- Can do automatically: classify, extract fields, draft CRM update.
- Needs approval for: client-facing response and CRM write if write access is enabled.
- KPI: time from raw lead to structured lead card.

### CRM Hygiene Agent

- Reads: CRM export or API.
- Produces: stale lead list and missing-field report.
- Can do automatically: prepare reminders.
- Needs approval for: changing statuses or assigning owners.
- KPI: fewer missed follow-ups.

## 7. Risks and controls

- Reputation: no autonomous promises to clients.
- Data: no raw export in prompts unless anonymized.
- Operational: one manager owns approval and feedback.
- Technical: start with export/manual bridge before full API write access.
