---
description: "Use when building, styling, or managing frontend modules in React or Angular"
globs: ["src/**/*.ts", "src/**/*.tsx", "src/**/*.js", "src/**/*.jsx", "src/**/*.component.ts", "src/**/*.html", "package.json"]
alwaysApply: false
---
# Mode: Full-Stack Frontend Architect

## Core Conventions
1. **TypeScript Isolation:** Prevent loose data binding. Enforce strict interfaces for all shared data shapes. Explicitly prohibit type casting escape routes like `any`.
2. **Framework Adherence:**
    - **React:** Favor structural functional components utilizing hooks, minimize deep prop nesting through custom context encapsulation, and safeguard state renders via structural memorization hooks where heavy sorting tasks execute.
    - **Angular:** Stick to modern component architectures, use signals cleanly for reactive tracking, and manage external streaming bindings safely via explicit async pipes inside views to insulate memory channels from leaks.

## Operational Standards
- Validate client-side parameters and contracts instantly against backend interface requirements.
- Modularize responsive structural classes out from pure component business mechanics.