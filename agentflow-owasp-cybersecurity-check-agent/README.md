# OWASP Cybersecurity Check Agent

Open-source, no-code starter agent for **AgentFlow.Directory**.

OWASP Cybersecurity Check Agent helps a user perform a **high-level application security review** from whatever context they can provide, including:
- files uploaded in chat,
- IDE context,
- repository context from GitHub,
- PR/build context in a CI workflow.

This starter pack is intentionally lightweight. It is designed for teams that want a practical **first-pass security check** without building a full security platform.

---

## What this agent does

A user can provide a mix of:
- source files,
- architecture notes,
- environment/config examples,
- dependency manifests,
- API descriptions,
- screenshots or build logs,
- GitHub repository context,
- IDE context.

The agent then turns that into a structured review with:
- executive summary,
- likely OWASP-aligned risks,
- missing controls,
- severity and confidence,
- remediation priorities,
- assumptions and limitations.

---

## What this agent does **not** do

- It does not execute code, scan infrastructure, or run exploits.
- It does not replace a penetration test, secure code review, or compliance audit.
- It should not invent evidence; findings should be tied to the supplied context.

---

## Suggested usage modes

### 1. Directly in chat
Paste snippets, upload files, or describe the system.
Ask for a high-level OWASP review with prioritized remediation.

### 2. In the IDE
Use the current file set, open tabs, or project summary as context.
Ask for a pre-commit or pre-release security sanity check.

### 3. In Codex
Feed the repository or changed files as context and request a structured security review.
Use it as an advisory reviewer, not as an autonomous security authority.

### 4. In CI workflow
Pass build artifacts, manifests, changed files, or repository summaries into the prompt.
Use the output as a review report or pull-request comment draft.

---

## Included files

- `agent-card.json` — metadata for AgentFlow.Directory
- `system-prompt.md` — core operating instructions for the agent
- `examples/sample-prompts.md` — ready-to-use prompts
- `templates/review-report-template.md` — reusable reporting format
- `templates/context-checklist.md` — what users should provide
- `prompts/` — prompt wrappers for chat, IDE, Codex, and CI use
- `.github/workflows/owasp-review.yml.example` — optional starter workflow example
- `README.md` — this file
- `LICENSE` — Apache-2.0

---

## Recommended MVP

Use this as a **prompt-only Custom GPT** first.

Then optionally add:
- a small knowledge file with your internal security standards,
- secure coding guidelines,
- architecture conventions,
- release review checklist.

---

## Example outcomes

This agent is best for questions like:
- “What are the most likely OWASP risks in this repo?”
- “What obvious auth, validation, secret, or logging issues do you see?”
- “What should we fix before release?”
- “What high-level security gaps appear in these changed files?”

---

## Suggested repo structure

```text
owasp-cybersecurity-check-agent/
├── .github/
│   └── workflows/
│       └── owasp-review.yml.example
├── examples/
│   └── sample-prompts.md
├── prompts/
│   ├── chat-review-prompt.md
│   ├── ci-review-prompt.md
│   ├── codex-review-prompt.md
│   └── ide-review-prompt.md
├── templates/
│   ├── context-checklist.md
│   └── review-report-template.md
├── agent-card.json
├── LICENSE
├── README.md
└── system-prompt.md
```

---

## Setup

1. Create a new Custom GPT.
2. Paste `system-prompt.md` into the instructions field.
3. Optionally upload your internal security checklist or architecture guidance as knowledge files.
4. Reuse the prompt wrappers from `prompts/` based on where you are working.
5. For CI, adapt the example workflow and route its context into your preferred review step.

---

## License

Apache-2.0
