# AICTIONBOT™ Werkbank MCP server

[![AICTIONBOT™ Werkbank MCP server](https://mcprush.com/badge/aictionbot-werkbank-mcp/card.svg)](https://mcprush.com/to/aictionbot-werkbank-mcp?ref=badge)

Procurement tools for small and mid-sized businesses, by [KULIC Advisory](https://www.kulicadvisory.com/) (Cologne), as a public remote MCP server.

- **Endpoint:** `https://www.kulicadvisory.com/mcp` (Streamable HTTP, stateless, JSON-RPC 2.0, MCP 2025-06-18)
- **Tools:** 35. 15 deterministic checks without AI and 10 tools for looking things up work without sign-in, rate limited per sender. 10 tools need an AICTIONBOT™ Werkbank licence (OAuth 2.1 with PKCE).
- **Integration guide and partner terms:** https://www.kulicadvisory.com/workbench/partner/ (German: https://www.kulicadvisory.com/de/werkbank/partner/)
- **Registry name:** `com.kulicadvisory/aictionbot-werkbank`
- **Directory:** [mcprush.com/kulicadvisory/aictionbot-werkbank-mcp](https://mcprush.com/kulicadvisory/aictionbot-werkbank-mcp)

Nothing you pass in is stored. The checks without AI return a readable finding and structured data (`structuredContent`). Not legal or tax advice.

## Checks without AI, no sign-in

| Tool | What it does |
|---|---|
| `check_price_increase` | Check a supplier price increase against official market data (Germany) |
| `list_categories` | List goods and service categories for the price increase check |
| `screen_sanctions` | Screen a company or person against public sanctions lists |
| `calculate_notice_deadline` | Calculate the last day to give notice on a contract |
| `check_discount_window` | Find early-payment discounts (Skonto) that expire in the next days, and which payment run still catches them |
| `check_approval_matrix` | Check an approval matrix against the people list: who approves although they left, lack a role or have no deputy |
| `check_invoice_payment` | Check an invoice against the vendor master before paying: new bank account, unknown supplier, blocked vendor |
| `check_rasci_matrix` | Check a RASCI matrix against the people list: tasks without an A, several A, no R, roles without an active person |
| `check_catalog` | Check a supplier's new price list against the old one before loading it: increases per item, hidden unit changes, new and dropped items |
| `build_category_profile` | Build a category profile from a spend list and contracts: volume, suppliers, concentration, next notice date, levers |
| `find_in_list` | Find a document number, order number, supplier number, name or keyword in a list and return the matching rows |
| `analyse_spend` | Analyse a spend or order export: who carries the volume, small orders, bundling, tail and possible duplicate postings |
| `match_documents` | Match purchase requisition, purchase order, order confirmation, goods receipt and invoice: 2-way and 3-way match with ready-made queries |
| `check_vendor_master` | X-ray a vendor master list: duplicates, invalid IBAN and VAT ID, gaps, dormant vendors and risk signals |
| `build_business_case` | Business case for a procurement improvement: annual value band, ROI band, payback band and where the value comes from |

## Looking things up, no sign-in

| Tool | What it does |
|---|---|
| `search_library` | Search the KULIC Advisory library: articles, practice cases and method pages on procurement, Source-to-Pay and execution |
| `get_article` | Read one article, practice case or method page from the KULIC Advisory library as text |
| `list_templates` | List the procurement and Source-to-Pay working templates of the KULIC Advisory Execution Toolkit Library |
| `get_template` | Read one template of the Execution Toolkit Library: what it is for, its structure and the download link |
| `fill_template` | Fill a table section of an Excel template or the placeholders of a Word template with the user's own values |
| `atlas_overview` | Painpoint Atlas: the map of 12 procurement fields and 49 recurring pain points from twenty years of practice |
| `find_painpoint` | Find the procurement pain points that match a situation described in the user's own words |
| `get_painpoint` | Read one pain point from the Painpoint Atlas: what happens, how often it was found, cause, lever and the matching tool |
| `find_scene` | Find scenes in the Painpoint Cinema: 100 documented scenes from twenty years of procurement, finance and sales, in six languages |
| `get_scene` | Read one scene of the Painpoint Cinema: what happened, the figures and the link to watch it |

## With a Werkbank licence

| Tool | What it does |
|---|---|
| `werkbank_licence` | Show my AICTIONBOT™ Werkbank licence: plan, period and remaining AI analyses |
| `review_contract` | Review a contract or terms and conditions from the buyer side (AICTIONBOT™ clause radar) |
| `compare_offers` | Compare two or three supplier offers like a buyer (AICTIONBOT™ offer comparison) |
| `check_invoice` | Check a supplier invoice against order and goods receipt (AICTIONBOT™ invoice check) |
| `write_scope_of_work` | Turn one sentence into a scope of work for a request for quotes (AICTIONBOT™ scope writer) |
| `write_meeting_minutes` | Write minutes and commitments from notes of a supplier meeting (AICTIONBOT™ minutes) |
| `plan_negotiation` | Prepare a supplier negotiation: goal, alternative, opening position, concessions and answers to objections (AICTIONBOT™ negotiation sparring) |
| `negotiation_round` | Practise the negotiation: plays the supplier, answers the buyer's last message and coaches it (AICTIONBOT™ negotiation sparring) |
| `evaluate_negotiation` | Evaluate the practised negotiation: grade, what went well, what to improve and one sentence for the real meeting (AICTIONBOT™ negotiation sparring) |
| `get_painpoint_full` | Read any pain point of the full Painpoint Atlas with its findings (AICTIONBOT™ Werkbank licence) |

## Quick start

Add the server to any MCP client that speaks Streamable HTTP (Claude, ChatGPT, Cursor, your own agent):

```json
{ "mcpServers": { "aictionbot-werkbank": { "type": "http", "url": "https://www.kulicadvisory.com/mcp" } } }
```

List the tools:

```bash
curl -s -X POST https://www.kulicadvisory.com/mcp \
  -H 'content-type: application/json' -H 'accept: application/json, text/event-stream' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list","params":{}}'
```

## Privacy and contact

Privacy notice: https://www.kulicadvisory.com/privacy/ · Contact: dario@kulicadvisory.com

This repository holds documentation, `server.json` and examples. The server itself runs on the KULIC Advisory website and is not open source.
