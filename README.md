# AICTIONBOT™ Werkbank MCP server

[![AICTIONBOT™ Werkbank MCP server](https://mcprush.com/badge/aictionbot-werkbank-mcp/card.svg)](https://mcprush.com/to/aictionbot-werkbank-mcp?ref=badge)

Procurement functions for small and mid-sized businesses and for the AI agents companies already run, by [KULIC Advisory](https://www.kulicadvisory.com/) (Cologne), as a public remote MCP server.

- **Endpoint:** `https://www.kulicadvisory.com/mcp` (Streamable HTTP, stateless, JSON-RPC 2.0)
- **Version:** 1.12.0, **62 tools**
- **Open without sign-in:** 11 tools for looking things up and 4 for reading or editing an existing Shared Table.
- **37 checks without AI** (including NDA, RFQ, template fill and opening a Shared Table): with an AICTIONBOT™ Werkbank licence, trial week, contract key or partner key; without a licence one check per connection every 30 days is free after signing in with “Connect without a licence”.
- **10 tools with a licence:** AI analyses, negotiation sparring, the full Painpoint Atlas and the licence status.
- **Sign-in:** OAuth 2.1 (PKCE, CIMD, DCR).
- **Integration guide, partner terms and test keys:** https://www.kulicadvisory.com/workbench/partner/ (German: https://www.kulicadvisory.com/de/werkbank/partner/)
- **Registry name:** `com.kulicadvisory/aictionbot-werkbank`
- **Directory:** [mcprush.com/kulicadvisory/aictionbot-werkbank-mcp](https://mcprush.com/kulicadvisory/aictionbot-werkbank-mcp)

Nothing you pass in is stored. The checks without AI calculate by fixed rules and return a readable finding plus structured data (`structuredContent`). Not legal or tax advice.

## Feeding your company's agents

Agents for procurement, finance or service often lack the procurement rules that cost money when they are wrong: notice periods, sanctions lists, price indices, approval rules. Add the endpoint once and every agent that speaks MCP calls these functions and works on with a checked result instead of a guess. Vendors of procurement and finance software can add the checks to their own product; see the partner page.

## Looking things up, no sign-in (11)

| Tool | What it does |
|---|---|
| `list_categories` | List goods and service categories for the price increase check |
| `atlas_overview` | Painpoint Atlas: the map of 12 procurement fields and 49 recurring pain points from twenty years of practice |
| `find_painpoint` | Find the procurement pain points that match a situation described in the user's own words |
| `get_painpoint` | Read one pain point from the Painpoint Atlas: what happens, how often it was found, cause, lever and the matching tool |
| `find_scene` | Find scenes in the Painpoint Cinema: 100 documented scenes from twenty years of procurement, finance and sales |
| `get_scene` | Read one scene of the Painpoint Cinema: what happened, the figures and the link to watch it |
| `search_library` | Search the KULIC Advisory library: articles, signal reads, practice and proof cases, execution stories, guides and method pages |
| `get_article` | Read one article, practice case or method page from the KULIC Advisory library as text |
| `list_templates` | List the procurement and Source-to-Pay working templates of the KULIC Advisory Execution Toolkit Library |
| `get_template` | Read one template of the Execution Toolkit Library: what it is for, its structure and the download link |
| `find_comic` | Find comics from the KULIC Advisory Comic Library |

## Shared Table, no sign-in for an existing table (4)

| Tool | What it does |
|---|---|
| `read_table` | Read a Shared Table from its link |
| `add_to_table` | Add entries to a Shared Table or tick off open points |
| `change_table` | Change a Shared Table: edit or remove entries, connect cards on the board, rename |
| `delete_table` | Delete a Shared Table for both sides |

## Checks without AI (37)

| Tool | What it does |
|---|---|
| `check_price_increase` | Check a supplier price increase against official market data (Germany) |
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
| `fill_template` | Fill a table section of an Excel template or the placeholders of a Word template with the user's own values |
| `create_nda` | Draft a mutual or one-way non-disclosure agreement (NDA) from the KULIC Advisory NDA template |
| `open_table` | Open a new Shared Table: one encrypted file for two sides (need, scope, offers, decision, open points) |
| `check_contracts` | Check a whole contract list: notice deadlines in the next days, silent renewals, missed deadlines, contracts without an owner |
| `check_actions` | Check an action log or implementation tracker: overdue, blocked, no owner, no due date, duplicates, overload, traffic light per work package |
| `score_offers` | Score offers with weighted criteria: ranking, gap to the runner-up, the weight change that would flip the winner, suspiciously low prices |
| `rate_supplier` | Rate suppliers with a scorecard: points and class A to D, trend against the previous period, figures below target, three measures for the supplier meeting |
| `screen_supplier_risk` | Early warning check for a supplier list: red, yellow or green by KULIC Advisory's rules L-01 to L-10, plus sanctions screening |
| `track_value` | Prove savings: identified, signed, realised and what actually reached the budget or P&L, with the gaps in euros |
| `segment_suppliers` | Segment suppliers by business impact and supply risk: strategic, leverage, bottleneck, transactional, with the way to handle each |
| `compare_scenarios` | Compare commercial scenarios: volume against price, tiers, one-off costs, freight, rebate and cash discount, with the cheapest offer per volume range |
| `create_rfq` | Draft a request for quotation (RFQ) from the KULIC Advisory RFQ template: scope, requirements, response table, checklist, timeline, criteria, terms |
| `check_kpis` | Check source-to-pay KPIs as a traffic light: PO coverage, invoices without PO, after-the-fact POs, cycle times, exceptions, payment on time, cash discount |
| `process_lever` | Process lever: current and target minutes and rework per process step, turned into hours, full-time equivalents and euros per year |
| `check_portfolio` | Portfolio traffic light: progress against time and budget per project, overdue, over budget, no owner, reported green but calculating red, forecast at completion |
| `map_stakeholders` | Stakeholder map: influence and interest in four fields, attitude, who brings whom along, and a conversation plan in the right order |
| `plan_sourcing` | Sourcing plan for a category: field, approach (tender, partnership, secure supply, simplify), levers, negotiation style and a dated timeline to the contract |
| `audit_list` | Data X-ray for any list: fill rate per column, formats (email, IBAN, VAT ID, date, number), duplicates, spelling variants, outliers, personal data |
| `assess_team` | Capability gaps per person and team against a role profile: who is ready for more, who needs a coaching plan, three training priorities |
| `ai_readiness` | AI and digital readiness: score across eight fields, level, weakest field and the next concrete step |
| `check_ai_use_case` | Check a planned AI use case for completeness and control: card, data readiness, risk questions, controls, signal proceed, pilot, redesign or stop |
| `esg_questionnaire` | Sustainability evidence questions for suppliers by category, and a check of the answers against required evidence (no rating, no seal) |
| `weekly_status` | Weekly status as a traffic light: each figure against last week and target, what moved most |

## With a Werkbank licence (10)

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

## What it rests on

The rules come from more than 20 years of hands-on procurement and source-to-pay work by Dario Kulić, 40 handwritten notebooks and documented engagement files. Every rule the tools cite was signed off by him. The Painpoint Atlas collects 49 recurring procurement problems from that practice.

## Privacy and contact

Privacy notice: https://www.kulicadvisory.com/privacy/ · Contact: dario@kulicadvisory.com

This repository holds documentation, `server.json` and examples. The server itself runs on the KULIC Advisory website and is not open source.
