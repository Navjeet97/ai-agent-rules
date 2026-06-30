---
description: "Triggers when updating modern Angular components, structural services, or state actions"
globs: ["**/*.component.ts", "**/*.service.ts", "**/*.state.ts"]
alwaysApply: false
---
# Skill: Reactive Angular Signal Architecture

## Signal Management Conventions
1. **State Tracking:** Favor Angular `signal()` and `computed()` structures exclusively for managing local visual adjustments over legacy, heavy imperative class properties.
2. **RxJS Interoperability:** Use reactive bridge patterns like `toSignal()` to safely down-convert streaming state definitions (like HTTP client endpoints) into easy-to-read signal blocks inside the visual markup.

## Structural Strategy
- Enforce the `changeDetection: ChangeDetectionStrategy.OnPush` paradigm explicitly across modern component interfaces to minimize routine framework layout re-verification checks.
- Keep structural actions and network calls decoupled cleanly within structural service modules.