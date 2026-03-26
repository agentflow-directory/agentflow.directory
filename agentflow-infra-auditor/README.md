# agentflow-infra-auditor

Open-source, no-code starter agent for **AgentFlow.Directory**.

`agentflow-infra-auditor` helps users review infrastructure architecture, configuration patterns, and operational risks at a high level.

This starter pack is intentionally minimal. It is designed for platform teams, DevOps engineers, founders, and technical leads who want a practical infrastructure review agent with **little or no coding**.

---

## What this agent does

A user can come in with inputs such as:
- “Review this Terraform approach at a high level.”
- “Audit this infrastructure design for resilience and scaling issues.”
- “What are the risky infra anti-patterns in this setup?”
- “Give me a practical checklist before we move this to production.”

The agent then helps structure the review into:
- architecture summary,
- assumptions,
- critical dependencies,
- availability risks,
- security and networking gaps,
- scalability bottlenecks,
- operational gaps,
- cost-risk tradeoffs,
- remediation priorities.

---

## Core outcome

By the end of a session, the user should have:
- a clearer view of infra risks,
- a prioritized remediation list,
- production-readiness concerns,
- practical questions for deeper technical review,
- a cleaner path to hardening the system.

---

## Best use cases

This agent is useful for:
- pre-production infrastructure reviews,
- architecture sanity checks,
- Terraform or IaC review at the design level,
- platform hardening,
- migration planning,
- cloud setup reviews for small teams.

---

## What the agent produces

Depending on the prompt, the agent can produce:
- infra review summary,
- production-readiness checklist,
- scalability concerns,
- resilience gaps,
- networking and dependency review,
- remediation plan,
- prioritized risk register.

---

## Suggested workflow

### Phase 1 — Map the system
- summarize components,
- identify dependencies,
- identify critical paths.

### Phase 2 — Find risks
- check availability and recovery,
- inspect scaling assumptions,
- inspect networking and secrets handling,
- inspect operational supportability.

### Phase 3 — Prioritize
- distinguish critical from nice-to-have,
- propose practical fixes,
- order remediation by impact.

---

## No-code MVP setup

You can build this as:
1. a **prompt-only Custom GPT**, or
2. a **Custom GPT + one knowledge file** containing infra review checklists.

Useful knowledge file sections:
- cloud architecture review checklist,
- production readiness questions,
- Terraform anti-pattern examples,
- resilience and backup checklist.

---

## Repository structure

```text
agentflow-infra-auditor/
├── README.md
├── LICENSE
├── system-prompt.md
└── agent-card.json
```

---

## Example prompts

- “Audit this cloud architecture for resilience risks.”
- “Review this Terraform plan at a high level.”
- “What could break in production in this infra setup?”
- “Give me a prioritized infra hardening plan.”
