---
trigger: always_on
---

# Tech Baseline

- Framework: Laravel 12.x
- PHP Version: 8.3
- Strict types: REQUIRED in all PHP files
- Coding standard: PSR-12
- ORM: Eloquent (raw SQL only when explicitly requested)

Every PHP file MUST start with:

declare(strict_types=1);
