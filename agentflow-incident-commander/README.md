# agentflow-incident-commander

Open-source, no-code starter agent for **AgentFlow.Directory**.

`agentflow-incident-commander` helps users run incidents with less chaos by turning messy signals into a clear response workflow.

This starter pack is intentionally minimal. It is designed for operators, SREs, DevOps teams, SecOps teams, and founders who want a working incident coordination agent with **little or no coding**.

---

## What this agent does

A user can come in with inputs such as:
- “Production is down. Help me run the incident.”
- “We have elevated error rates after deploy.”
- “Create a structured incident update and response plan.”
- “Help me keep the timeline, owners, and next steps straight.”

The agent then helps structure the situation into:
- incident severity,
- impact summary,
- working hypotheses,
- immediate containment steps,
- role assignment,
- communication cadence,
- status updates,
- timeline,
- next checkpoints,
- post-incident handoff notes.

---

## Core outcome

By the end of a session, the user should have:
- a clear incident brief,
- a simple command structure,
- prioritized response actions,
- stakeholder-ready updates,
- a running timeline,
- a cleaner handoff into postmortem.

---

## Best use cases

This agent is useful for:
- production outages,
- degraded performance events,
- failed deploys,
- infra instability,
- service dependencies failing,
- security incidents that need coordinated response.

It is especially useful when the team:
- is under stress,
- has incomplete information,
- needs clean status communication,
- wants to avoid duplicated work,
- needs to move fast without losing structure.

---

## What the agent produces

Depending on the prompt, the agent can produce:
- incident command brief,
- severity assessment,
- first 15-minute action plan,
- stakeholder status updates,
- war-room checklist,
- timeline draft,
- role assignment template,
- post-incident handoff summary.

---

## Suggested workflow

### Phase 1 — Stabilize
- define the incident,
- summarize impact,
- identify likely blast radius,
- choose severity.

### Phase 2 — Coordinate
- assign owners,
- separate investigation from communication,
- create a short action plan,
- set the next checkpoint.

### Phase 3 — Communicate
- generate internal update,
- generate external/customer-safe update if needed,
- maintain a running timeline.

### Phase 4 — Transition
- summarize what changed,
- capture decisions,
- prepare postmortem inputs.

---

## No-code MVP setup

You can build this as:
1. a **prompt-only Custom GPT**, or
2. a **Custom GPT + one knowledge file** containing incident templates.

Useful knowledge file sections:
- severity matrix,
- incident role definitions,
- update templates,
- escalation checklist,
- postmortem questions.

---

## Example prompts

- “Help me run a SEV-1 incident for elevated 500s.”
- “Turn this outage summary into an incident command brief.”
- “Draft a 15-minute incident response plan and status update.”
- “Create a clean stakeholder update from this messy incident context.”
