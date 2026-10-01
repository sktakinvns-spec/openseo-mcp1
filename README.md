# OpenSEO MCP

This repository contains a minimal, safe setup for using the official hosted OpenSEO MCP server with compatible AI clients such as Codex, Cursor, Claude Code, and other MCP clients.

## Official OpenSEO MCP endpoint

```text
https://app.openseo.so/mcp
```

The first OAuth connection opens OpenSEO login/authorization. After approval, the client can use the OpenSEO tools allowed by your OpenSEO account and project.

## Codex CLI

```bash
codex mcp add openseo --url https://app.openseo.so/mcp
```

Then approve the OpenSEO login in your browser.

To verify:

```bash
codex mcp list
```

## Cursor / generic MCP client

Use the included `mcp.json`.

## Optional API-key authentication

For headless/CI usage, create an OpenSEO API key in OpenSEO Settings. Never commit a real key to this repository.

```bash
export OPENSEO_API_KEY=oseo_YOUR_KEY
codex mcp add openseo --url https://app.openseo.so/mcp --bearer-token-env-var OPENSEO_API_KEY
```

## OpenSEO capabilities

Depending on your OpenSEO plan/project, MCP can expose workflows for keyword research, live Google SERPs, competitor/domain research, backlinks, rank tracking, saved keywords, Google Search Console performance and URL inspection, local SEO research, and shared project context/reports.

## Security

Do not commit OpenSEO API keys, Google credentials, WordPress credentials, or any other secrets.
