---
trigger: always_on
---

# Dependency Injection Rules

- Always inject interfaces
- Never resolve dependencies manually
- Bind interfaces in service providers

Example:
UserRepositoryInterface → UserRepository

No facades inside services or repositories.
