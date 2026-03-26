# agentflow-observability-designer

Open-source, no-code starter agent for **AgentFlow.Directory**.

`agentflow-observability-designer` helps users design pragmatic observability for services, systems, and teams without drowning in noisy metrics and alerts.

This starter pack is intentionally minimal. It is designed for DevOps teams, SREs, platform engineers, and engineering leads who want a practical observability design agent with **little or no coding**.

---

## What this agent does

A user can come in with inputs such as:
- “What should we monitor for this service?”
- “Help me define SLI/SLO for this product.”
- “Design alerts that won’t create constant noise.”
- “We have logs and dashboards, but no clear observability strategy.”

The agent then helps structure the design into:
- service objectives,
- critical user journeys,
- important signals,
- SLI/SLO candidates,
- alerting rules,
- dashboard sections,
- on-call usability,
- telemetry gaps.

---

## Core outcome

By the end of a session, the user should have:
- a clearer observability strategy,
- a practical set of signals to collect,
- initial SLI/SLO definitions,
- less noisy alert ideas,
- dashboard and runbook direction.

---

## Best use cases

This agent is useful for:
- new services going to production,
- observability redesign,
- alert fatigue reduction,
- SLO adoption,
- platform standardization,
- reliability reviews.

---

## What the agent produces

Depending on the prompt, the agent can produce:
- observability plan,
- SLI/SLO draft,
- alerting strategy,
- dashboard outline,
- telemetry gap analysis,
- service health checklist,
- on-call signal map.

---

## Suggested workflow

### Phase 1 — Define what matters
- identify user-facing outcomes,
- identify critical paths,
- identify failure modes.

### Phase 2 — Map signals
- metrics,
- logs,
- traces,
- events,
- dependencies.

### Phase 3 — Design actionability
- define SLI/SLO,
- design alerts for response, not noise,
- outline dashboards and review cadence.

---

## No-code MVP setup

You can build this as:
1. a **prompt-only Custom GPT**, or
2. a **Custom GPT + one knowledge file** containing monitoring templates.

Useful knowledge file sections:
- SLI/SLO examples,
- alerting anti-patterns,
- dashboard templates,
- golden signals checklist,
- service review template.

---

## Repository structure

```text
agentflow-observability-designer/
├── README.md
├── LICENSE
├── system-prompt.md
└── agent-card.json
```

---

## Example prompts

- “Design observability for this API service.”
- “Help me define practical SLI/SLO for our checkout flow.”
- “What alerts should we actually page on?”
- “Create a low-noise dashboard and alerting plan.”
