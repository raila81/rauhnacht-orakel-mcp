# Rauhnacht-Orakel MCP server

Answers questions about the Rauhnächte 2026/27, the twelve nights between Christmas and Epiphany, in German: a personal January card from the birth date, the dates, names and rituals of the twelve nights with the month each one stands for, and the ritual of the 13 wishes step by step. Each answer links to the matching page on rauhnaechte-ritual.de.

- **Website:** [rauhnaechte-ritual.de](https://rauhnaechte-ritual.de)
- **Documentation:** [rauhnaechte-ritual.de](https://rauhnaechte-ritual.de/)
- **Endpoint:** `https://rauhnaechte-ritual.de/mcp` (MCP Streamable HTTP, public, no authentication, no API key)

## Tools

- `rauhnacht_karte`: Returns the same free January card as rauhnaechte-ritual.de: the 1st Rauhnacht (Nacht der Wurzeln, stands for January 2027) with sun sign, moon sign, the personal...
- `rauhnaechte_kalender`: Returns all twelve nights, each with its date, the month of 2027 it stands for, its name and a short ritual, in the wording of rauhnaechte-ritual.de
- `dreizehn_wuensche`: Returns the ritual step by step: what to prepare before the first night, what to do in each of the twelve nights and what happens with the last wish, with the dates...

All tools are read-only and stateless. The birth date is used only to compose the card and is not stored or logged; see the privacy page.

## Connect

Any MCP client that supports remote servers:

```json
{
  "mcpServers": {
    "rauhnacht-orakel": {
      "type": "streamable-http",
      "url": "https://rauhnaechte-ritual.de/mcp?src=mcp"
    }
  }
}
```

Quick test:

```bash
curl -s -X POST 'https://rauhnaechte-ritual.de/mcp?src=mcp' -H 'Content-Type: application/json' -H 'Accept: application/json, text/event-stream' -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

This repository holds the listing metadata only. The server itself is a hosted service run by the Rauhnacht-Orakel website (https://rauhnaechte-ritual.de); see [privacy](https://rauhnaechte-ritual.de/datenschutz/) and [terms](https://rauhnaechte-ritual.de/agb/).
