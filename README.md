# AICTIONBOT™ Werkbank MCP server

Seven deterministic procurement checks for small and mid-sized businesses, by [KULIC Advisory](https://www.kulicadvisory.com/) (Cologne), exposed as a public MCP server.

- **Endpoint:** `https://www.kulicadvisory.com/mcp` (Streamable HTTP, JSON-RPC 2.0, MCP 2025-06-18)
- **Auth:** none for the public tier, rate limited per sender. Partner keys for higher volume and white label.
- **Integration guide and partner terms:** https://www.kulicadvisory.com/workbench/partner/ (German: https://www.kulicadvisory.com/de/werkbank/partner/)
- **Registry name:** `com.kulicadvisory/aictionbot-werkbank`

No AI inside the checks. Nothing you pass in is stored. Findings are written in German, with structured data (`structuredContent`) for your own interface; input keys may be German or English. Not legal or tax advice.

## Tools

| Tool | What it does |
|---|---|
| `check_price_increase` | Compares a supplier's price increase with the official Eurostat producer price indices for Germany. |
| `list_categories` | Lists the categories `check_price_increase` knows, with their index codes. |
| `screen_sanctions` | Screens a supplier name against the EU, UN, US and UK sanctions lists. |
| `calculate_notice_deadline` | Gives the last day a contract can still be terminated. |
| `check_discount_window` | Reads an open-items list and says which early-payment discounts (Skonto) expire within the window, which are blocked, and which payment run still catches them. |
| `check_approval_matrix` | Checks an approval matrix against the people list: approvers who left, missing deputies, missing system roles, limit gaps. |
| `check_invoice_payment` | Matches an invoice to the vendor master and flags a new or unknown bank account before a payment goes out. |

## Quick start

Add the server to any MCP client that speaks Streamable HTTP (Claude, ChatGPT connectors, Cursor, your own agent):

```json
{
  "mcpServers": {
    "aictionbot-werkbank": {
      "url": "https://www.kulicadvisory.com/mcp"
    }
  }
}
```

List the tools:

```bash
curl -s -X POST https://www.kulicadvisory.com/mcp \
  -H 'content-type: application/json' \
  -H 'accept: application/json, text/event-stream' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

Run a check (see `examples/` for complete request bodies):

```bash
curl -s -X POST https://www.kulicadvisory.com/mcp \
  -H 'content-type: application/json' \
  -H 'accept: application/json, text/event-stream' \
  --data-binary @examples/check_discount_window.json
```

## What this repository contains

Documentation only: this README, the registry `server.json`, and example request bodies. The checking engines themselves run on the server and in the AICTIONBOT™ Werkbank apps (browser, Mac, Windows) and are not published here.

## Contact

Dario Kulić, KULIC Advisory, Cologne · dario@kulicadvisory.com

© KULIC Advisory. AICTIONBOT™ is a trademark of KULIC Advisory. Documentation in this repository may be quoted with attribution.
