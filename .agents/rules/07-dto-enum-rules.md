---
trigger: always_on
---

# DTO & Enum Rules

## DTOs
- final and readonly
- No logic beyond mapping
- No database access
- Must be reusable

## Enums
- Preferred over constants
- Used for statuses, types, modes

DTOs protect services from API changes.
