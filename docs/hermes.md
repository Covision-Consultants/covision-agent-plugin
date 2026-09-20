# Hermes setup

Hermes can load this portable bundle for the Covision skill and MCP declaration.
Use the pre-registered production OAuth client for a complete login configuration:

```yaml
mcp_servers:
  covision:
    url: https://connector.covisionperformance.com/mcp
    auth: oauth
    oauth:
      client_id: covision-hermes
      redirect_host: localhost
      redirect_port: 27890
```

Then run:

```bash
hermes mcp login covision
hermes mcp test covision
```

The browser login requires a Covision account, membership in an organization that
has enabled the connector, and individual consent. The current grant is read-only
and can be revoked in Covision.
