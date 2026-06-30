---
description: "Triggers when configuring event queues, message consumers, or event payload handlers"
globs: ["**/*mq*/**", "**/*messaging*/**", "**/*consumer*/**", "**/*producer*/**", "**/*event*/**/*.py", "**/*event*/**/*.java"]
alwaysApply: false
---
# Skill: Distributed Asynchronous Messaging (RabbitMQ)

## System Design Patterns
1. **Message Versioning:** Every messaging event payload contract must be explicitly versioned via the naming scheme (e.g., `v1.order.created`).
2. **Idempotency Check:** Because distributed messaging platforms operate on an *at-least-once* delivery guarantee, all consumers must run an explicit deduplication validation loop using a fast distributed cache before executing internal business updates.

## Failure Isolation & Recovery
- **Dead Letter Exchanges (DLX):** Never discard failed event reads silently. Configure specific Dead Letter Exchanges to intercept unparseable, malformed, or repeatedly crashed message envelopes.
- **Circuit Breaking:** Wrap event-driven client interaction hooks inside retry thresholds to preserve downstream services from being overwhelmed during unexpected traffic spikes.