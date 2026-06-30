# Skill: Distributed Asynchronous Messaging (RabbitMQ)
- **Convention:** All event payloads must be explicitly versioned (e.g., `v1.order.created`).
- **Resilience:** Implement explicit retry channels and Dead Letter Exchanges (DLX) for failure containment.
- **Testing:** Mock message brokers explicitly during unit testing loops to maintain isolated test environments.