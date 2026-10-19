# 01. Client–Server Architecture

Client–Server Architecture is a model in which a client sends a request to a server, and the server processes the request and returns a response. The client may be a browser, mobile app, or another service.

## How it works

- The user performs an action in an application.
- The client sends a request to the backend.
- The backend validates and processes the request.
- The backend communicates with a database if needed.
- The server returns a response and the client displays the result.

## Example: login flow

- Client submits credentials.
- Backend verifies them against stored credential data.
- The application creates an authenticated session or issues a token.
- The client receives the result and loads the user's permitted content.

## Important components

- **Client:** initiates requests and displays results.
- **Server:** processes requests and applies business rules.
- **Database:** stores and retrieves application data.
- **Network:** carries requests and responses between systems.

## Common architectures

- **Two-tier:** client communicates with a server or data layer.
- **Three-tier:** presentation, application logic, and data layers are separated.
- **Multi-tier:** the application is split into additional services or layers.

> **Interview:** When a URL is entered, the browser may resolve DNS, establish a connection, negotiate TLS for HTTPS, send an HTTP request, receive a response, and render the returned resources. The exact sequence varies with caching and connection reuse.
