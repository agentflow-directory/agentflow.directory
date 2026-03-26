# Context Checklist

Provide as much of this as you can. Partial context is still fine.

## Helpful inputs
- Relevant source files
- Configuration files
- Dependency manifests
- Environment variable examples with secrets removed
- API route definitions
- Authentication / authorization flow notes
- Architecture diagram or summary
- CI logs or build summaries
- Pull request diff or changed files
- Known constraints or deadlines

## Especially useful for a stronger review
- How users authenticate
- How roles/permissions are enforced
- Where secrets are stored
- How file uploads are handled
- What external services are trusted
- Whether logs contain sensitive data
- Whether security headers / CSP / CORS are configured
- What sits on the public internet

## Good prompt pattern
“Review this context for high-level OWASP risks. Separate observed evidence from inference. Rank findings by severity and tell me what to fix now versus verify manually.”
