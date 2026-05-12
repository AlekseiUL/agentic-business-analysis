---
name: agentic-business-analysis
description: "Use when analyzing a business to find safe, measurable AI-agent automation opportunities: process mapping, opportunity scoring, agent role design, approval gates, and 2-4 week pilot scope."
version: 1.0.0
author: Agentic Business Analysis contributors
license: MIT
metadata:
  hermes:
    tags: [business-analysis, ai-agents, automation, consulting, process-mapping, pilot-scoping]
    related_skills: []
---

# Agentic Business Analysis

## Overview

Agentic Business Analysis is a method for turning a real business operation into a safe AI-agent automation plan.

The core rule: **map the business before designing the agents**. Do not start with “let's build a chatbot”. Start with processes, owners, triggers, inputs, outputs, tools, bottlenecks, approval points, and success metrics.

Use this method to produce one of three outputs:

1. a quick automation opportunity map;
2. a client-facing Agentic Business Audit;
3. a narrow 2-4 week pilot scope.

## When to Use

Use when asked to:

- analyze a client/business for AI-agent automation;
- find where agents can be embedded;
- map business processes;
- choose the first automation pilot;
- design agent roles, permissions, tools, memory, and handoffs;
- prepare a consulting report, roadmap, or paid pilot.

Do not use when the task is only generic brainstorming, pure market research, or implementation without business context.

## Minimum Intake

If context is thin, ask only questions that change the design:

1. What does the business sell and to whom?
2. What are the 3-5 most repeated weekly processes?
3. Where is the current pain: leads, sales, delivery, support, docs, reporting, content, admin?
4. What tools are used: CRM, messengers, email, sheets, Notion, accounting, website, payment, task tracker?
5. What data/examples are available: chats, CRM export, docs, SOPs, calls, reports?
6. What must never be automated without human approval?
7. What result would make a 2-4 week pilot obviously useful?

If repository support files are available, see `references/agentic-business-intake-form.md` or `docs/intake-form.md`. If this SKILL.md was installed as a single file, the minimum intake above is enough to start.

## Business Decomposition

Split the business into lanes:

- lead generation / marketing;
- sales / qualification / CRM;
- delivery / operations / production;
- support / customer success;
- admin / documents / finance;
- reporting / management control;
- knowledge base / onboarding / SOPs.

For each lane capture:

```text
Process:
Owner:
Trigger:
Inputs:
Steps:
Tools:
Outputs:
Frequency/volume:
Pain/bottleneck:
Decision points:
Human approvals:
Risk level:
Current metric:
```

## Good Automation Candidates

Prioritize work that is:

- repeated daily or weekly;
- text-heavy, data-heavy, or decision-heavy;
- built around clear inputs and outputs;
- backed by examples, SOPs, history, chats, or documents;
- measurable;
- low-to-medium risk with human approval;
- currently done by copying between tools, chats, tables, and docs;
- valuable when made faster, more consistent, or easier to control.

Bad first pilots:

- no source data;
- rare edge-case work;
- unclear owner;
- high legal/finance/reputation risk without approval gate;
- political or management mess disguised as automation;
- “replace a person end-to-end” fantasy;
- no success metric.

## Opportunity Scoring

Score each opportunity from 1 to 5:

- business pain;
- frequency / volume;
- repeatability;
- data availability;
- integration ease;
- human approval fit;
- risk if wrong, reverse-scored;
- pilot visibility;
- commercial value.

```text
Total = pain + frequency + repeatability + data + integration + approval_fit + risk_score + pilot_visibility + commercial_value
Max = 45
```

Interpretation:

- 36-45: strong first pilot candidate;
- 28-35: useful, but check constraints;
- 20-27: maybe later or needs prep work;
- below 20: do not automate first.

If repository support files are available, see `references/agentic-automation-scoring.md` or `docs/automation-scoring.md`. If this SKILL.md was installed as a single file, the scoring dimensions above are enough to rank pilots.

## Agent Role Design

Design agents by **responsibility**, not by employee replacement.

Each agent needs a job card:

```text
Agent name:
Business role:
Primary goal:
Inputs it reads:
Tools/integrations it can use:
Memory/knowledge base needed:
Actions it may perform automatically:
Actions requiring approval:
Outputs it produces:
Handoff targets:
Escalation rules:
Forbidden actions/data:
Success metric:
Failure mode / risk:
Human owner:
```

Common roles:

- Intake Agent;
- Qualification Agent;
- CRM Hygiene Agent;
- Support Triage Agent;
- Knowledge Base Agent;
- Document Agent;
- Research Agent;
- Reporting Agent;
- Content Ops Agent;
- Quality Check Agent;
- Coordinator / Supervisor Agent.

## Topology Patterns

Use the smallest topology that proves value:

- **Single-agent assistant** for a narrow process.
- **Pipeline** for staged work: intake -> enrichment -> draft -> approval -> update.
- **Supervisor-worker** when tasks branch by domain.
- **Fan-out / fan-in** for research, audits, and comparisons.
- **Workflow engine + agents** when deterministic triggers and integrations matter.
- **Human-in-the-loop** for money, legal, public, client-facing, destructive, or access-related actions.


## Default Output Schema

For a normal business-analysis request, return this shape unless the user asks for a different format:

```text
1. Short verdict
   Where agents can create leverage first, and what not to automate yet.

2. Business snapshot
   Business model, customers, team roles, tools, source of truth, repeated processes.

3. Process lanes
   Lead/marketing, sales/CRM, delivery/ops, support, admin/docs/finance, reporting/control, knowledge/SOPs.

4. Top automation opportunities
   3-5 opportunities with pain, data needed, approval gate, risk, and rough score.

5. Recommended first pilot
   One 2-4 week pilot with goal, included/excluded scope, success metric, and human owner.

6. Proposed agent contour
   Agent roles, inputs, tools, memory/KB, allowed actions, approval-required actions, handoffs, escalation rules.

7. Data and integration needs
   Required exports, APIs/webhooks, documents, SOPs, logging, privacy constraints.

8. Risks and controls
   Technical, operational, legal/formal, finance, reputation, privacy.

9. Open questions
   Only questions that block pilot design.
```

## Report Structure

A useful Agentic Business Audit includes:

1. short verdict;
2. business snapshot;
3. current process map;
4. bottlenecks and manual load;
5. automation opportunity ranking;
6. proposed agent contour;
7. interaction architecture;
8. data and integration requirements;
9. 2-4 week pilot scope;
10. roadmap after pilot;
11. risks and controls;
12. open questions / decisions needed.

If repository support files are available, see `references/agentic-audit-client-deliverable.md` or `docs/audit-report-template.md`. If this SKILL.md was installed as a single file, the report structure above is enough to produce a useful audit.


## Privacy and Safety

Before using real client data:

- minimize data: request samples, not full exports, unless necessary;
- redact names, emails, phones, addresses, payment data, medical/legal details, and private employee/client notes where possible;
- never request or store API keys, passwords, private keys, session files, or production credentials;
- define which systems need read/write access;
- use read-only access during audit where possible;
- require human approval for client-facing, money, legal/formal, public, destructive, or access/security actions;
- define what logs are kept and what raw data is deleted after the pilot.

If repository support files are available, use `references/privacy-and-safety-checklist.md` or `docs/privacy-and-safety.md`.

## Output Rules

Write in business-readable language.

Bad:

> multi-agentic RAG orchestration layer

Good:

> The agent reads incoming requests, extracts name, goal, budget, urgency, and missing fields, prepares a CRM update, and asks the manager to approve the client-facing reply.

Never promise guaranteed revenue. Frame commercial outcomes as assumptions or pilot hypotheses unless baseline data proves otherwise.

## Verification Checklist

- [ ] Business lanes are mapped.
- [ ] Each automation candidate has owner, input, output, frequency, risk, and metric.
- [ ] First pilot is narrow and measurable.
- [ ] Agent responsibilities are business-readable.
- [ ] Approval gates are explicit.
- [ ] Data and integration requirements are explicit.
- [ ] Legal, finance, reputation, and privacy risks are named.
- [ ] No “replace employees” or “fully autonomous business” claim.
