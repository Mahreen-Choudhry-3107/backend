# 10. Database Normalization

Normalization organizes relational data to reduce duplication and prevent insert, update, and delete anomalies.

## Example

- If customer name and email are repeated on every order, changing an email requires multiple updates.
- A `CUSTOMERS` table can store `customer_id`, `name`, and `email` once.
- An `ORDERS` table can reference `customer_id`.

## Normal forms

- **1NF:** fields contain single values from their intended domains; repeating groups are avoided.
- **2NF:** in 1NF, with every non-key attribute depending on the whole candidate key rather than part of a composite key.
- **3NF:** in 2NF, with no prohibited transitive dependency of non-key attributes on a candidate key.

## Denormalization

- Intentionally introduces duplication or precomputed data to improve reads or simplify access patterns.
- Can help analytics and high-read workloads.
- Adds consistency, refresh, and maintenance complexity.

> **Interview:** Normalization improves integrity and maintainability; selective denormalization may be useful when measurement shows a performance need.
