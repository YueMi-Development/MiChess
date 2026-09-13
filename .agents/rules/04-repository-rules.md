---
trigger: always_on
---

# Repository Rules

## Interface First
- Every repository MUST have an interface
- Depend on interfaces, not implementations

## Repository Responsibilities
- Data access only
- No business logic
- No validation
- No Request, Auth, Session, or HTTP references

## Method Rules
- Accept primitives, arrays, or DTOs
- Return typed models or collections
- Generic naming only

Bad:
- getUsersForDashboard()

Good:
- findByStatus(UserStatus $status)
