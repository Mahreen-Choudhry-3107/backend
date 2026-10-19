# 05. JWT vs Sessions

Sessions and JSON Web Tokens (JWTs) are two ways to carry or maintain authentication state. The right choice depends on architecture, revocation needs, and browser security.

## Session flow

- User submits credentials; the server verifies them.
- The server creates a session in server-side storage.
- The client receives a session ID, commonly in a cookie.
- The client sends the cookie with later requests; the server looks up the session.

## JWT flow

- Server verifies credentials and issues a token.
- A typical JWT has a header, payload, and signature.
- The client sends the token according to the application's security design.
- The server validates signature and relevant claims such as issuer, audience, and expiration.

## Comparison

- **Sessions:** state is usually server-side; central invalidation is often straightforward; shared session storage may be needed across instances.
- **JWTs:** claims travel in the token; validation can reduce session lookups in suitable designs; immediate revocation requires additional design.
- A signed JWT is not automatically encrypted; its payload is generally readable by anyone who has it.

## Security practices

- Use HTTPS and short-lived access tokens where appropriate.
- Protect refresh tokens and avoid sensitive secrets in token claims.
- Carefully choose cookie or browser storage strategies.
- Consider CSRF risks with cookies and XSS risks when tokens are accessible to JavaScript.

> **Interview:** Neither JWT nor sessions are universally better. Choose based on revocation, scaling, browser threat model, and identity-provider integration.
