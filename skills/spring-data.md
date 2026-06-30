---
description: "Triggers when editing Spring Data repositories, JPA entities, or transactional logic"
globs: ["**/repository/**/*.java", "**/entity/**/*.java", "**/service/**/*.java", "**/*Repository.java", "**/*Entity.java"]
alwaysApply: false
---
# Skill: Spring Data JPA & Hibernate Optimization

## Data Mapping & Associations
1. **Lazy Loading First:** Always use `FetchType.LAZY` for `@OneToMany` and `@ManyToMany` relationships to avoid severe performance degradation.
2. **Lombok with JPA:** Never use Lombok's `@Data` or `@EqualsAndHashCode` on JPA `@Entity` classes; it breaks Hibernate collections and causes unexpected memory overflows. Use explicit getters/setters and custom, identifier-safe `equals()` / `hashCode()` overrides.
3. **DTO Projections:** Avoid retrieving full entities for read-only query views. Use Java 25 records with Spring Data constructor projections to bypass persistence context caching overhead.

## Transactional Boundaries
- Always annotate write-operations or multi-repository updates with `@Transactional`.
- For pure read paths, optimize database interaction with `@Transactional(readOnly = true)` to skip Hibernate dirty checking runs.