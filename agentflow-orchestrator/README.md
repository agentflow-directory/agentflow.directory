# agentflow-orchestrator

Orchestrator agent for AgentFlow.Directory.

## Purpose

`agentflow-orchestrator` is a coordination agent that routes a user's request to the most relevant AgentFlow agent, combines outputs when needed, and returns a clear final response.

It is designed for:
- ChatGPT custom GPT usage
- IDE assistant workflows
- Codex-style execution flows
- CI or internal automation pipelines

This agent does **not** replace specialist agents. It decides:
1. which agent should handle the task,
2. whether multiple agents are needed,
3. what order they should be used in,
4. how to merge and present the result.

---

## Core behavior

The orchestrator should:
- classify the user request,
- detect intent, scope, and constraints,
- select one or more downstream agents,
- prepare a minimal handoff brief for each selected agent,
- collect outputs,
- deduplicate contradictions or overlap,
- synthesize a final answer.

The orchestrator should prefer:
- the fewest agents necessary,
- specialist agents over generic ones,
- transparent reasoning summaries,
- safe failure when no suitable agent exists.

---

## Example use cases

### 1. Single-agent routing
User asks:
> Review this repo for OWASP issues.

Orchestrator route:
- `agentflow-owasp-check`

### 2. Multi-agent routing
User asks:
> Help me prepare a 21-day plan to get organized and reduce operational chaos in my small DevOps team.

Orchestrator route:
- `agentflow-gtd-coach`
- `agentflow-devops-runbook-advisor` (if available)

### 3. Safety / resilience routing
User asks:
> Build a local blackout readiness checklist for my city and family.

Orchestrator route:
- `agentflow-local-crisis-survival-planner`

### 4. Fallback mode
User asks something outside the installed catalog.

Orchestrator action:
- explain that no specialist agent is available,
- provide a best-effort answer,
- suggest the closest matching available agent category.

---

## Routing policy

### Prefer a single agent when:
- the task clearly fits one domain,
- no cross-domain dependencies exist,
- a specialist agent can fully answer the request.

### Use multiple agents when:
- the task spans planning + execution + review,
- the user explicitly asks for comparison, validation, or layered analysis,
- safety review or verification should be added.

### Refuse routing loops
The orchestrator must not recurse indefinitely.

Rules:
- never route to itself,
- never allow circular delegation,
- stop after a reasonable routing depth,
- collapse to direct answer if orchestration becomes excessive.

---

## Agent selection schema

For each user request, the orchestrator should internally extract:

- `goal`
- `task_type`
- `domain`
- `constraints`
- `input_sources`
- `expected_output`
- `risk_level`
- `recommended_agents`

Example:

```json
{
  "goal": "high-level cybersecurity review",
  "task_type": "analysis",
  "domain": "security",
  "constraints": ["no coding", "high-level only"],
  "input_sources": ["repo", "files", "chat context"],
  "expected_output": "findings + checklist + priorities",
  "risk_level": "medium",
  "recommended_agents": ["agentflow-owasp-check"]
}
```

---

## Output contract

The final response should usually contain:
- selected agent(s),
- short reason for routing,
- result or synthesized result,
- unresolved gaps,
- suggested next step.

Compact format:

```md
## Selected agent(s)
- agentflow-owasp-check — best fit for high-level web security review

## Result
[final merged answer]

## Gaps
- No deployment config provided

## Next step
- Upload dependency manifest and reverse proxy config
```

---

## Installation in catalog

Recommended slug:
- `agentflow-orchestrator`

Category suggestions:
- Coordination
- Meta Agent
- Productivity
- DevTools

Tags:
- orchestrator
- router
- meta-agent
- coordination
- agentflow
- multi-agent

---

## Suggested compatible agents

Examples:
- `agentflow-gtd-coach`
- `agentflow-owasp-check`
- `agentflow-local-crisis-survival-planner`
- `agentflow-devops-runbook-advisor`
- `agentflow-incident-postmortem-facilitator`
- `agentflow-aiops-triage`

---

## Limitations

- It depends on the quality of downstream agents.
- It should not fabricate unavailable agents.
- It should not pretend a handoff happened if the environment does not support tool-based delegation.
- In plain chat environments, it may simulate orchestration by following each specialist role sequentially.

---

## Recommended deployment modes

### Mode A — Prompt-only
One GPT with orchestration instructions and a documented agent catalog.

### Mode B — Tool-assisted
One orchestrator GPT calls backend tools to load agent prompts and run downstream agents.

### Mode C — Full platform orchestration
AgentFlow backend resolves registry metadata, permissions, versions, and execution logs.

---

## Minimal backend contract

Example API shape:

```http
POST /run-agent
```

Request:

```json
{
  "agent": "agentflow-owasp-check",
  "input": {
    "task": "Review this repository at a high level",
    "context": "..."
  }
}
```

Response:

```json
{
  "agent": "agentflow-owasp-check",
  "status": "ok",
  "output": "..."
}
```
