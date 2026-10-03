# Installing the Adrails MCP server

Adrails is a hosted remote MCP server. Nothing is installed locally.

1. Add a remote MCP server named `adrails` with the URL `https://adrails.ai/api/mcp` and the Streamable HTTP transport.
2. Use OAuth. Do not set a client ID or secret: the client registers itself through dynamic client registration (authorization code with PKCE, S256, `resource` set to `https://adrails.ai/api/mcp`).
3. The user signs in to Adrails in the browser, chooses a workspace and the permissions, and allows access. An Adrails account is required.
4. Check the connection by calling the `integrations_status` tool, which only reads.

Advertising changes are returned as proposals with an `approvalUrl`; show that link to the user. Nothing reaches Meta or Google Ads until they approve it.

Reference: https://adrails.ai/docs/mcp/connect
