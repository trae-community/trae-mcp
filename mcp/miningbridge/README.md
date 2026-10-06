# MiningBridge Intelligence MCP

Critical-mineral and rare-earth trade intelligence for Trae: commodity snapshots, UN Comtrade trade flows, supplier screening, supply-risk scores, evidence search and MiningBridge market reports. Nine read-only tools; none can change data.

## When to use

- Checking where a mineral (cobalt, lithium, nickel, rare earths and others) is produced and traded, and how concentrated supply is.
- Screening suppliers or counterparties for a commodity and country.
- Pulling sourced figures into research, reports or code without copying them by hand.

## Status

Ready (hosted remote Streamable HTTP server; OAuth 2.1 sign-in with a MiningBridge account, dynamic client registration and PKCE).

## Documentation

- Setup for all apps: https://intel.miningbridge.in/connect
- Docs: https://github.com/miningbridge/intel-mcp
- Official MCP Registry name: `in.miningbridge/intel`

## Trae MCP config

Settings → MCP → Add → Manual:

```json
{
  "mcpServers": {
    "miningbridge": {
      "url": "https://intel.miningbridge.in/api/mcp"
    }
  }
}
```

On first use Trae opens a MiningBridge sign-in page; a free account works (headline figures; paid plans add full reports).

## Example

> Using MiningBridge, what is the supply risk for cobalt, and which countries dominate refined output?

## Notes

Figures are screening magnitudes from public sources, not price targets or investment advice. Support: support@miningbridge.in

## License

Documentation in this folder: MIT. The hosted service is operated by MiningBridge Private Limited.
