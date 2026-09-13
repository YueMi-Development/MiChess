---
trigger: always_on
---

# Reusability Guardrails

## Forbidden
- Feature-specific repository methods
- Request-aware repositories
- Hard-coded assumptions

## Required
- Generic method naming
- Stateless services
- Composable logic

Ask: "Can this be reused in another feature?"
If no → redesign.
