# kirans-ai

## Robinhood Trading MCP

This repo is configured to use the [Robinhood Trading MCP](https://agent.robinhood.com/mcp/trading)
server so an AI agent can interact with Robinhood Trading.

### Configuration

The server is defined as a project-scoped MCP server in [`.mcp.json`](./.mcp.json):

```json
{
  "mcpServers": {
    "robinhood-trading": {
      "type": "http",
      "url": "https://agent.robinhood.com/mcp/trading"
    }
  }
}
```

### Connect in Claude Code

When you open this project in Claude Code, it will detect the `.mcp.json`
server and prompt you to approve it. Alternatively, add it directly:

1. Run this command in your terminal:
   ```bash
   claude mcp add robinhood-trading --transport http https://agent.robinhood.com/mcp/trading
   ```
2. Enter `/mcp` in Claude Code.
3. Select `robinhood-trading` and authenticate.

For details, review the [Claude Code MCP documentation](https://code.claude.com/docs/en/mcp).

### Connect in Claude Desktop

1. Go to **Settings → Connectors → Add custom connector**.
2. Add this MCP link: `https://agent.robinhood.com/mcp/trading`

### Authentication

The Robinhood Trading MCP uses OAuth. The first time the agent connects,
you'll be prompted to sign in to your Robinhood Agentic account and authorize
access. No credentials or tokens are stored in this repository.
