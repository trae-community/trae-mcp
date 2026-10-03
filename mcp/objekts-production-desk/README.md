# objekts Production Desk

**objekts Production Desk** is a hosted remote MCP server built by [objekts](https://objekts.ai/), a visual-production studio working across AI/VFX, CGI/3D, motion, animation, advertising, film/series VFX, localization/versioning and production support for agencies.

It is designed for **production preflight**, not generic creative prompting.

## Remote MCP

```
https://mcp.objekts.ai/mcp
```

No API key or local runtime is required for production diagnosis or directional estimates.

## TRAE configuration

Add the server manually in TRAE MCP settings:

```json
{
  "mcpServers": {
    "objekts-production-desk": {
      "url": "https://mcp.objekts.ai/mcp"
    }
  }
}
```

The server uses Streamable HTTP.

## What it does

The primary read-only tool is `diagnose_production`.

It checks:
- hard visual locks;
- which reference controls which production property;
- unsafe AI/CGI/graphics routing;
- source-asset fitness;
- continuity risk across shots;
- versioning vs recomposition vs new production scope;
- revision/change impact;
- production readiness;
- the first PoC that should remove the most expensive uncertainty.

`estimate_production` should be used only when the user explicitly asks for price, budget, quote or budget fit.

A human-review handoff to the objekts production team is optional and requires explicit user confirmation plus a reply channel.

## Example prompts

- "We have an approved packshot and exact logo. Diagnose the production risks before making three AI/VFX hero shots."
- "We need a 15-second commercial plus a 9:16 version. Tell me whether the vertical is an export, recomposition or new production scope."
- "The same character must survive five shots. What should we prove before producing the sequence?"
- "Check whether these source assets are production-ready for the camera move we want."
- "We have a fixed budget. Diagnose the job first, then estimate only the scope that is actually defined."

## Public verification

- Studio: https://objekts.ai/
- Source: https://github.com/peach420fuzz/objekts-production-desk
- MCP overview: https://mcp.objekts.ai/about
- Public protocol test: https://mcp.objekts.ai/test
- Privacy: https://mcp.objekts.ai/privacy
- Terms: https://mcp.objekts.ai/terms
- Security: https://mcp.objekts.ai/.well-known/security.txt

Publisher: **objekts**
