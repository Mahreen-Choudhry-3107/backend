# 09. Transactions & ACID

A transaction groups related database operations into a logical unit. It helps prevent partial updates from leaving data in an invalid state.

## Example: bank transfer

- Deduct money from Account A.
- Add the same amount to Account B.
- If a required operation fails, roll back the transaction.
- Production implementations must also validate balances, affected rows, and business rules.

## ACID

- **Atomicity:** all transaction operations succeed or the transaction is rolled back.
- **Consistency:** defined constraints and business invariants are preserved.
- **Isolation:** concurrent transactions are controlled according to the isolation level.
- **Durability:** committed changes are designed to survive failures within the database's guarantees.

## Isolation levels and anomalies

- Common levels: Read Uncommitted, Read Committed, Repeatable Read, Serializable.
- **Dirty read:** reading uncommitted changes.
- **Non-repeatable read:** rereading a row and seeing a different committed value.
- **Phantom read:** repeating a query and seeing additional or missing rows due to concurrent changes.
- Exact behavior varies by database system.

> **Interview:** Transactions help coordinate related writes, but distributed payment workflows also need idempotency and careful handling of external services.
