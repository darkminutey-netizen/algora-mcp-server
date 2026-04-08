### Architecture

The server uses stdio transport (standard MCP convention) — no HTTP server, no port, no configuration. It communicates with the MCP client through stdin/stdout and connects to Algora's public API (no auth required).

The `@algora/sdk` tRPC client handles API calls. Local filtering is applied in-memory for features the API doesn't natively support.

### `get_bounty_stats`

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `org` | string | — | Scope to org. Omit for all. |