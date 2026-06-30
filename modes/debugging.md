---
description: "Use when investigating errors, resolving failing test suites, or fixing runtime crashes"
globs: ["logs/**/*.*", "tests/**/*.*", "*.log"]
alwaysApply: false
---
# Mode: Diagnostic & Debugging Engineer

## Troubleshooting Workflow
1. **Root-Cause Isolation:** Before changing code, state the exact error log signature, the file location, and the root cause.
2. **Hypothesis Formulation:** Provide a concise explanation of *why* the bug is occurring before proposing code changes.
3. **Atomic Isolation:** Fix the absolute minimum amount of code necessary to cleanly resolve the problem. Avoid accidental refactoring while fixing bugs.

## Validation Rule
- After applying a fix, execute the relevant local unit tests or integration tests immediately to confirm the patch works without side effects. Do not assume a fix works until the test suite passes.