# Configure Memory

Bring saved project requirements, decisions, and preferences into your current coding task.

Configure keeps useful context in a profile controlled by the user. A connected assistant can search for the details relevant to a task and save new decisions when asked. This is useful when continuing a project whose brief was developed in another AI app.

## Connection

- Hosted endpoint: `https://mcp.configure.dev/`
- Transport: Streamable HTTP
- Account: Configure sign-in and user authorization are required for profile access.
- Public package and connection guide: https://github.com/configure-dev/configure-mcp-plugin
- Documentation: https://docs.configure.dev

In TRAE's MCP settings, add an HTTP server using the endpoint above. Follow the current [TRAE MCP setup documentation](https://docs.trae.ai/ide/add-mcp-servers). Profile access requires the client's supported OAuth or Configure connection flow; do not put a personal access token into a shared configuration file.

## Usage examples

- "Use my saved Configure project requirements to plan the onboarding flow."
- "Check Configure for the decisions I saved about this project's first release."
- "Remember in Configure that this project should support keyboard navigation."

The general MCP offers targeted profile search, profile retrieval, explicit single and batch saves, deletion, user-provided imports, and project operations. Optional linked apps have separate connections and permissions.

## Data and verification

Only context available to the connected Configure account can be retrieved. This connector does not automatically read another assistant's private chat history. Users manage their saved context and connections in Configure.

The public MCP endpoint responds to initialization and exposes nine tools without credentials; profile operations require authorization. **A native TRAE installation and signed-in tool call have not yet been tested.** This entry is submitted for community review and integration testing, not as a certified TRAE integration.

## License

This documentation and the linked public wrapper use MIT. Configure's hosted backend and user data are not included in the wrapper and remain subject to their applicable terms.

[Privacy](https://configure.dev/privacy.html) | [Terms](https://configure.dev/terms.html)
