# CI Review Prompt

Using the supplied repository summary, manifests, changed files, and build context, generate a high-level OWASP security review.

Output format:
- Executive summary
- Findings by severity
- Missing controls
- Fix now
- Fix soon
- Verify manually
- Limitations

Important:
- Use only the provided CI context.
- Do not claim runtime verification unless evidence is included.
- Keep the output suitable for a PR comment or release review note.
