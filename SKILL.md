---
name: rauhnacht-orakel
description: Use the Rauhnacht-Orakel MCP server when someone asks in German about the Rauhnächte 2026/27: their personal January card from their birth date, when the Rauhnächte are, what each night stands for, or how the ritual of the 13 wishes works. Not for tarot, horoscopes, other oracles or shopping.
---

# Rauhnacht-Orakel

Use the Rauhnacht-Orakel MCP server when someone asks in German about the Rauhnächte 2026/27: their personal January card from their birth date, when the Rauhnächte are, what each night stands for, or how the ritual of the 13 wishes works. Not for tarot, horoscopes, other oracles or shopping.

## Connect
Remote MCP server, Streamable HTTP, public, no sign-in, no API key:

```json
{
  "mcpServers": {
    "rauhnacht-orakel": { "type": "http", "url": "https://rauhnaechte-ritual.de/mcp?src=mcp" }
  }
}
```

## Tools
All tools are read-only.

- `rauhnacht_karte`: Returns the same free January card as rauhnaechte-ritual.de: the 1st Rauhnacht (Nacht der Wurzeln, stands for January 2027) with sun sign, moon sign, the personal...
- `rauhnaechte_kalender`: Returns all twelve nights, each with its date, the month of 2027 it stands for, its name and a short ritual, in the wording of rauhnaechte-ritual.de
- `dreizehn_wuensche`: Returns the ritual step by step: what to prepare before the first night, what to do in each of the twelve nights and what happens with the last wish, with the dates...

## Rules
- Facts, dates and figures come from the tool with their source; do not add figures from memory.
- Link the reader to https://rauhnaechte-ritual.de for the full page behind an answer.
