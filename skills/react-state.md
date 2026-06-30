---
description: "Triggers when working on complex React state management, hooks, or context APIs"
globs: ["**/store/**/*.ts", "**/hooks/**/*.ts", "**/context/**/*.tsx", "**/*Context.tsx", "**/state/**/*.ts"]
alwaysApply: false
---
# Skill: Advanced React Component State Architecture

## Component Separation of Concerns
1. **Dumb UI Components:** Keep presentation components strictly pure. They must ingest data solely via typed props and communicate changes up using stateless callbacks.
2. **Custom Hook Extraction:** Isolate API data-fetching loops, input event validations, and intricate processing mechanics out from the visual tree into self-contained custom hooks (e.g., `useOrderWorkflow.ts`).

## Component Performance Optimizations
- Wrap high-compute transformation functions safely inside the structural `useMemo` hook.
- Implement explicit return garbage sweeps inside `useEffect` hook triggers (e.g., clearing tracking intervals, aborting fetch streams via an `AbortController`) to insulate memory tracks from expanding leaks.