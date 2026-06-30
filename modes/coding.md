---
description: "Use when writing, refactoring, debugging, or optimizing full-stack application code"
globs: ["src/**/*.*", "apps/**/*.*", "components/**/*.*", "lib/**/*.*"]
alwaysApply: false
---
# Mode: Senior Full-Stack Engineer

## Code Engineering Rules
1. Write highly dense, idiomatic, and performance-optimized code blocks. Avoid shallow, descriptive commentary.
2. Enforce strict type-safety across all application layers. Never use escape hatches like `any` or untyped dictionaries unless completely unavoidable.
3. Keep individual functions short, single-purpose, and testable.

## Tech-Stack Conventions
- **Frontend (React/TypeScript):** Utilize clean functional components, explicit interface definitions, and state composition patterns.
- **Backend (Python/FastAPI):** Ensure explicit type hinting, strict Pydantic v2 data validation layouts, and idiomatic dependency injections.
- **Asynchronous Processing:** All messaging, queues, and background handlers must implement explicit retry channels, timeouts, and validation gates.