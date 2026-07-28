# CloudBase MCP

Tencent CloudBase MCP server for Trae — AI models, auth, NoSQL/PostgreSQL, cloud functions, storage, CloudRun, and WeChat Mini Program tooling via [`@cloudbase/cloudbase-mcp`](https://www.npmjs.com/package/@cloudbase/cloudbase-mcp).

## Status

Ready (npm package; Trae manual MCP config)

## Documentation

- Plugin / IDE setup: https://docs.cloudbase.net/ai/cloudbase-ai-toolkit/ai-agent-plugins
- Source: https://github.com/TencentCloudBase/CloudBase-AI-Toolkit
- Dedicated Open Plugin repo: https://github.com/TencentCloudBase/cloudbase-plugin

## Trae MCP config

Settings → MCP → Add → Manual:

```json
{
  "mcpServers": {
    "cloudbase-mcp": {
      "command": "npx",
      "args": ["-y", "@cloudbase/cloudbase-mcp@latest"],
      "env": {}
    }
  }
}
```

On first use the server opens a browser login / environment selection flow for your CloudBase account.

## License

MIT
