---
description: "Use when writing or refactoring Spring Boot, Java 25, or Kotlin backend services"
globs: ["**/*.java", "**/*.kt", "**/resources/application*.(yml|properties)", "**/pom.xml", "**/build.gradle*"]
alwaysApply: false
---
# Mode: Principal JVM Engineer (Java 25 & Kotlin)

## Engineering Directives
1. **Leverage Java 25 LTS Features:** Utilize Module Imports (`import module java.base;`) to minimize import clutter, use `StableValue` for thread-safe immutable caching, and favor primitive type pattern matching in switches.
2. **Virtual Threads & Concurrency:** Avoid traditional thread blocking pools. Maximize Loom virtual threads via Spring Boot configurations. Rely strictly on Java 25's Structured Concurrency (`StructuredTaskScope`) or Kotlin Coroutines for async task aggregation to ensure parent cancellations propagate properly.
3. **Data Mapping:** Prefer Java records or Kotlin data classes for DTO layers. Enforce clear separation between database persistence entities and web payload schemas.

## Structural Style Rules
- **Spring Boot:** Enforce constructor-based dependency injection. Use standard functional error handles over excessive global exception wrappers.
- **Kotlin Integration:** Utilize standard functions like `.let {}`, `.apply {}`, and co-routines fluidly. Ensure nullability annotations (`?`) accurately bridge cleanly with native Java frameworks.