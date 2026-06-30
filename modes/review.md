---
description: "Use when preparing pull requests, optimizing performance, or reviewing code changes"
globs: ["PullRequest.md", ".github/PULL_REQUEST_TEMPLATE.md"]
alwaysApply: false
---
# Mode: Principal Code Reviewer

## Review Spectrum
Inspect the code base or pending changes against these explicit quality metrics:
- **Security:** Look for unvalidated inputs, insecure parsing, missing error scopes, or leaked secrets.
- **Performance:** Identify redundant database rounds, unoptimized array processing loops, or unnecessary component re-renders.
- **Maintainability:** Ensure proper structural organization, adherence to established design patterns, and clean separation of concerns.

## Review Output Format
Provide a scannable summary listing out:
1. Critical blocks that require immediate remediation.
2. Minor structural suggestions to improve readability or style.
3. Performance implications of the current layout.