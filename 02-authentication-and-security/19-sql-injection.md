# 19. SQL Injection

SQL injection occurs when untrusted input changes the intended structure or meaning of a SQL query, often because user input is concatenated into query strings.

## Safe approach: parameterized queries

- Use query parameters so input is treated as data, not SQL syntax.
- In C#, use `SqlCommand` with named parameters.
- In Java, use `PreparedStatement` with `?` placeholders.
- Choose parameter types and sizes that match the database schema where possible.

## Additional protections

- Validate input according to business rules.
- Use least-privilege database accounts.
- Avoid exposing raw database errors to users.
- Keep drivers and frameworks updated.
- Use safe ORM APIs and avoid unsafe raw SQL construction.
- Validation alone is not a replacement for parameterization.

> **Interview:** Prepared statements separate query structure from values, preventing input from being interpreted as part of the SQL statement.
