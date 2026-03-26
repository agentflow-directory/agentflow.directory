# IDE Review Prompt

Use the current IDE context to perform a high-level OWASP security check.

Focus on:
- authentication,
- authorization,
- input validation,
- secrets,
- insecure configuration,
- logging / monitoring gaps,
- risky file handling,
- dependency and supply-chain concerns.

Return:
1. Executive summary
2. Key findings
3. Missing controls
4. Prioritized remediation
5. Blind spots caused by missing context
