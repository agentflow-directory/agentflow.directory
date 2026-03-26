# Sample Prompts

## Chat
- Review these uploaded files for likely OWASP risks and give me the top 5 issues to fix first.
- Based on this architecture note and config file, what are the most obvious security gaps?
- Look at these API handlers and tell me whether authentication, authorization, and input validation appear weak.

## IDE
- Use the current IDE context to do a high-level OWASP check and tell me what I should verify before merging.
- Review these open files for risky patterns involving auth, secrets, file upload, and logging.
- I am about to ship this feature. What likely security issues do you see from the files in context?

## Codex
- Review this repository context as an OWASP-focused security advisor and produce a structured findings report.
- Use the changed files in this branch to identify likely security regressions or missing controls.
- Give me a severity-ranked security review from this repo context without making code changes.

## CI
- Using the supplied repository summary and changed files, generate a PR-ready OWASP review comment.
- Review these manifests and build outputs for high-level security risks and missing controls.
- Produce a release-gate summary: fix now, fix soon, verify manually, and monitor.
