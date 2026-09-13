---
trigger: always_on
---

# Project Structure

app/
├── Contracts/
│   └── Repositories/
├── Repositories/
│   └── Eloquent/
├── Services/
├── DTOs/
├── Enums/
├── Models/
└── Http/
    └── Controllers/

Rules:
- Contracts define behavior
- Repositories handle data access only
- Services contain business logic
- Controllers orchestrate requests
