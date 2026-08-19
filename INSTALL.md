# Instalação rápida

CPFL: Download é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_contas_cpfl_download`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `CPFL: Download` / `https://api.mcp.ai/p_contas_cpfl_download`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "contas_cpfl_download": { "type": "http", "url": "https://api.mcp.ai/p_contas_cpfl_download" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=contas_cpfl_download&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jb250YXNfY3BmbF9kb3dubG9hZCJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "contas_cpfl_download": { "url": "https://api.mcp.ai/p_contas_cpfl_download" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=contas_cpfl_download&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_contas_cpfl_download%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "contas_cpfl_download": { "type": "http", "url": "https://api.mcp.ai/p_contas_cpfl_download" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_contas_cpfl_download
```

Dúvidas? [contas_cpfl_download@mcp.ai](mailto:contas_cpfl_download@mcp.ai)
