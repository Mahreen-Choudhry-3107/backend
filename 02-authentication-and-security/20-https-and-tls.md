# 20. HTTPS & TLS

HTTPS is HTTP protected by Transport Layer Security (TLS). It helps protect data in transit from interception and tampering.

## What TLS provides

- **Confidentiality:** encrypts communication.
- **Integrity:** helps detect unauthorized modification.
- **Authentication:** certificates and the handshake help authenticate the server; client authentication is also possible in some configurations.

## Simplified flow

- Client connects to the server.
- Server presents a certificate.
- Client validates certificate and hostname.
- The parties negotiate cryptographic parameters and establish session keys.
- HTTP data is exchanged through the protected connection.

## Best practices

- Use valid certificates and current TLS configurations.
- Redirect HTTP to HTTPS where appropriate.
- Use `Secure` cookies for sensitive browser sessions.
- Consider HSTS and avoid mixed content.
- Continue to implement authorization, validation, and secure business logic.

> **Interview:** HTTPS protects data in transit, but does not automatically prevent broken authorization, SQL injection, insecure business logic, or exposed secrets.
