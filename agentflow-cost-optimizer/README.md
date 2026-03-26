# agentflow-cost-optimizer

Open-source, no-code starter agent for **AgentFlow.Directory**.

`agentflow-cost-optimizer` helps users review infrastructure and platform spending for practical savings without blindly harming reliability.

This starter pack is intentionally minimal. It is designed for DevOps teams, platform teams, founders, and engineering managers who want a pragmatic cost review agent with **little or no coding**.

---

## What this agent does

A user can come in with inputs such as:
- “Help me find cloud waste in this setup.”
- “Where are we likely overprovisioned?”
- “Review this infra for cost optimization opportunities.”
- “Give me a FinOps-style checklist that won’t break production.”

The agent then helps structure the review into:
- workload summary,
- likely cost drivers,
- overprovisioning signals,
- idle or waste patterns,
- storage and data transfer concerns,
- environment hygiene,
- rightsizing candidates,
- savings opportunities,
- risk-aware optimization order.

---

## Core outcome

By the end of a session, the user should have:
- a shortlist of likely savings opportunities,
- a sense of cost vs reliability tradeoffs,
- prioritized optimization ideas,
- practical next checks to run,
- a safer FinOps review process.

---

## Best use cases

This agent is useful for:
- startup cloud cost reviews,
- pre-scale optimization,
- infra cleanup,
- rightsizing discussions,
- environment hygiene reviews,
- platform cost governance.

---

## What the agent produces

Depending on the prompt, the agent can produce:
- cost optimization review,
- likely waste summary,
- rightsizing candidates,
- environment cleanup checklist,
- savings roadmap,
- risk-aware optimization plan,
- questions for billing review.

---

## Suggested workflow

### Phase 1 — Map the spend drivers
- identify core workloads,
- identify stateful services,
- identify environment sprawl,
- identify traffic and storage patterns.

### Phase 2 — Find waste
- overprovisioned compute,
- idle resources,
- duplicate environments,
- poor storage lifecycle,
- unnecessary data transfer,
- unused managed services.

### Phase 3 — Prioritize safe savings
- quick wins,
- medium-risk savings,
- changes requiring validation,
- changes that should wait.

---

## No-code MVP setup

You can build this as:
1. a **prompt-only Custom GPT**, or
2. a **Custom GPT + one knowledge file** containing FinOps checklists.

Useful knowledge file sections:
- cloud cost review checklist,
- rightsizing checklist,
- storage lifecycle checklist,
- environment cleanup checklist,
- savings prioritization rubric.

---

## Repository structure

```text
agentflow-cost-optimizer/
├── README.md
├── LICENSE
├── system-prompt.md
└── agent-card.json
```

---

## Example prompts

- “Review this infra for likely cloud waste.”
- “Where are we probably overprovisioned?”
- “Give me a safe cost optimization plan for this setup.”
- “Create a FinOps-style checklist for a small platform team.”
