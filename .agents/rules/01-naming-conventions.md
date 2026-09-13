---
trigger: always_on
---

# Naming Conventions

## Classes (PascalCase)
- Controllers, Models, Services, Repositories, DTOs, Enums

Examples:
- UserController
- UserService
- UserRepository
- UserData
- UserStatus

## Methods & Variables (camelCase)
- findById()
- createUser()
- $createdAt
- $isActive

## Interfaces
- PascalCase + Interface suffix
- Example: UserRepositoryInterface

## Constants (UPPER_SNAKE_CASE)
- Only when enum is NOT suitable
- Example: MAX_LOGIN_ATTEMPTS

## Database
- Tables: snake_case plural
- Columns: snake_case
- Pivot tables: alphabetical order

## Routes
- kebab-case
- RESTful naming
