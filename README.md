# mcp

Model Context Protocol (MCP) Server for the *mcp* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=mcp&utm_campaign=mcp-typescript"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
> [!IMPORTANT]
> This MCP Server is not yet ready for production use. Delete this notice before publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary


<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [mcp](#mcp)
  * [Installation](#installation)
  * [Development](#development)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start Installation [installation] -->
## Installation

> [!TIP]
> To finish publishing your MCP Server to npm and others you must [run your first generation action](https://www.speakeasy.com/docs/github-setup#step-by-step-guide).

<details>
<summary>Cursor</summary>

[![Install MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/install-mcp?name=SDK&config=eyJtY3BTZXJ2ZXJzIjp7IlNESyI6eyJjb21tYW5kIjoibnB4IiwiYXJncyI6WyJtY3AiLCJzdGFydCIsIi0tYXBpLWtleSIsIi4uLiIsIi0tYXBpLXNlY3JldCIsIi4uLiIsIi0tb2F1dGgyIiwiLi4uIiwiLS1jbG91ZC1uYW1lIiwiLi4uIl19fX0=)

Or manually:

1. Open Cursor Settings
2. Select Tools and Integrations
3. Select New MCP Server
4. If the configuration file is empty paste the following JSON into the MCP Server Configuration:

```json
{
  "mcpServers": {
    "SDK": {
      "command": "npx",
      "args": [
        "mcp",
        "start",
        "--api-key",
        "...",
        "--api-secret",
        "...",
        "--oauth2",
        "...",
        "--cloud-name",
        "..."
      ]
    }
  }
}
```

</details>

<details>
<summary>Claude Code CLI</summary>

```bash
npx mcp start --api-key ... --api-secret ... --oauth2 ... --cloud-name ...
```

</details>
<details>
<summary>Claude Desktop</summary>
Claude Desktop doesn't yet support SSE/remote MCP servers.

However, you can run the MCP server locally by cloning this repository. Once cloned, you'll need to install dependencies (`npm install`) and build the server (`npm run build`).

Then, configure your server definition to reference your local clone. For example:

```json
{
  "mcpServers": {
    "SDK": {
      "command": "node",
      "args": [
        "./bin/mcp-server.js",
        "start",
        "--api-key",
        "...",
        "--api-secret",
        "...",
        "--oauth2",
        "...",
        "--cloud-name",
        "..."
      ]
    }
  }
}
```

</details>
<!-- End Installation [installation] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

## Development

Run locally without a published npm package:
1. Clone this repository
2. Run `npm install`
3. Run `npm run build`
4. Run `node ./bin/mcp-server.js start --api-key ... --api-secret ... --oauth2 ... --cloud-name ...`

To use this local version with Cursor, Claude or other MCP Clients, you'll need to add the following config:

```json
{
  "mcpServers": {
    "SDK": {
      "command": "node",
      "args": [
        "./bin/mcp-server.js",
        "start",
        "--api-key",
        "...",
        "--api-secret",
        "...",
        "--oauth2",
        "...",
        "--cloud-name",
        "..."
      ]
    }
  }
}
```

Or to debug the MCP server locally, use the official MCP Inspector: 

```bash
npx @modelcontextprotocol/inspector node ./bin/mcp-server.js start --api-key ... --api-secret ... --oauth2 ... --cloud-name ...
```



## Contributions

While we value contributions to this MCP Server, the code is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### MCP Server Created by [Speakeasy](https://www.speakeasy.com/?utm_source=mcp&utm_campaign=mcp-typescript)
