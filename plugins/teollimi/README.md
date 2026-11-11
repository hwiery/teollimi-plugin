# Teollimi

Ask Claude, ChatGPT or Codex about data breaches and get answers from [Teollimi](https://teollimi.com): incidents confirmed by press reports and official announcements in Korea, Japan, the US and elsewhere, each with its source.

- **Was this company breached?** Date, number affected, leaked data, compensation and fines, with the source.
- **Check the services I use**: up to 10 at once.
- **Recent breaches**, by country.
- **US class action settlements** still taking claims, with deadlines and the official claim site.
- **What to do after a breach notice**, by the kind of data that leaked, with official help in Korea, the US and Japan.

Read-only, free, no sign-in. The plugin connects the remote MCP server `https://teollimi.com/mcp` and adds the `data-breach-check` skill.

## Install

- **Claude Code**: `/plugin marketplace add hwiery/teollimi-plugin`, then `/plugin install teollimi@teollimi`. Or the server alone: `claude mcp add --transport http teollimi https://teollimi.com/mcp`
- **Codex**: `codex plugin marketplace add hwiery/teollimi-plugin`, or add the server to `~/.codex/config.toml`:
  ```toml
  [mcp_servers.teollimi]
  url = "https://teollimi.com/mcp"
  ```
- **Claude and ChatGPT apps**: add `https://teollimi.com/mcp` as a custom connector (no authentication). Guide: https://teollimi.com/en/ai

## Tools

| Tool | What it returns |
|---|---|
| `search_breaches` | Up to 5 most recent breaches of a company, with sources |
| `recent_breaches` | Up to 10 breaches from the last 1-60 days, optionally by country |
| `check_services` | Breach history of up to 10 services |
| `open_settlements` | Up to 5 US settlements still taking claims |
| `breach_response_steps` | Steps and official help by leaked data type |

All tools are read-only.

## Privacy Policy

The server receives only the tool arguments your assistant sends (such as a company name), uses them to answer and does not store them. It never receives your conversation, files or account. To limit repeated requests, a salted hash of the IP address is counted per minute in server memory only. The site is hosted on Vercel, which keeps access logs under its own policy. Full policy: <https://teollimi.com/en/privacy>. Terms: https://teollimi.com/en/terms

## Support

goldenrod8888@gmail.com
