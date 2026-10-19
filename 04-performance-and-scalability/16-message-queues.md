# 16. Message Queues

A message queue or event-streaming platform lets one component publish work or events for another component to process asynchronously.

## Example: order processing

- Order API validates and records an order.
- A message is published for downstream processing.
- A consumer sends confirmation email.
- Other consumers may update analytics or notify a warehouse.

## Common technologies

- **RabbitMQ:** message broker with queueing and routing features.
- **Apache Kafka:** distributed event-streaming platform with durable streams and consumer groups.
- **Amazon SQS:** managed queue service.
- Delivery, ordering, retention, and operations differ by technology.

## Important concepts

- **Producer** publishes messages; **consumer** processes them; **broker** distributes them.
- **Acknowledgment** records processing progress according to the protocol.
- **Dead-letter queue** stores messages that cannot be processed under the configured policy.
- **Idempotent consumers** handle duplicate delivery without repeating unintended effects.

## Delivery semantics

- **At-most-once:** a message may be lost, but is not redelivered under the guarantee.
- **At-least-once:** a message may be delivered more than once.
- **Exactly-once** behavior is limited to defined system boundaries and does not automatically guarantee exactly-once effects in every external system.

> **Interview:** Queues buffer work and reduce coupling, but reliable processing still requires persistence, acknowledgments, retries, idempotency, monitoring, and dead-letter handling.
