# Agentic Automation Scoring Matrix

Use this to rank automation opportunities before implementation.

Score each dimension from 1 to 5.

## Dimensions

### Business pain

- 1 — cosmetic annoyance.
- 3 — meaningful recurring inefficiency.
- 5 — directly affects revenue, SLA, churn, manager workload, or quality.

### Frequency / volume

- 1 — rare, monthly or less.
- 3 — weekly.
- 5 — daily or high-volume.

### Repeatability

- 1 — every case is unique.
- 3 — process has patterns, but exceptions exist.
- 5 — clear repeated structure.

### Data availability

- 1 — no examples, no docs, no source of truth.
- 3 — some examples, scattered docs/chats.
- 5 — CRM/export/SOP/chats/FAQ available.

### Integration ease

- 1 — closed tools, no export/API, messy manual access.
- 3 — possible via export, webhook, or manual bridge.
- 5 — API/webhook/native integration/structured data.

### Human approval fit

- 1 — hard to review before action.
- 3 — review possible but adds friction.
- 5 — draft/check/approve flow is natural.

### Risk if wrong

Reverse score:

- 1 — high legal, financial, or reputation damage.
- 3 — moderate operational annoyance.
- 5 — low damage and easy rollback.

### Pilot visibility

- 1 — result is invisible or takes months.
- 3 — visible in a few weeks.
- 5 — obvious before/after within days or weeks.

### Commercial value

- 1 — client will not pay meaningfully for it.
- 3 — useful add-on.
- 5 — clear paid pilot / implementation budget.

## Formula

```text
Total = pain + frequency + repeatability + data + integration + approval_fit + risk_score + pilot_visibility + commercial_value
Max = 45
```

## Interpretation

- 36-45: strong first pilot candidate.
- 28-35: useful, but check constraints.
- 20-27: maybe later or needs prep work.
- below 20: do not automate first.

## Weighted shortcut

```text
Priority = pain + frequency + data + approval_fit + pilot_visibility - complexity_penalty - risk_penalty
```

Where:

- complexity penalty: 0-3;
- risk penalty: 0-3.

## Good first-pilot candidates

- lead intake / qualification;
- CRM hygiene and follow-up reminders;
- support triage and draft answers;
- weekly reporting from scattered sources;
- document / brief / proposal drafting with approval;
- knowledge base Q&A with gap detection;
- content repurposing from existing raw material.

## Avoid as first pilots

- agent independently closing deals with discounts/promises;
- legal, medical, or financial advice to clients;
- public publishing without approval;
- destructive admin actions;
- full ERP/accounting migration;
- “CEO replacement”;
- processes with no owner and no source data.
