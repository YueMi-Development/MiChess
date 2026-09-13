---
trigger: always_on
---

# Service Layer Rules

## Purpose
- Business logic lives here
- Coordinates multiple repositories
- Handles transactions

## Rules
- Services SHOULD be final
- Accept DTOs, not Request objects
- No HTTP concerns
- Can throw domain exceptions

## Transactions
- Allowed ONLY in services
