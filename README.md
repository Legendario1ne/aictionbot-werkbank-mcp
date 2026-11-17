# AICTIONBOT™ Werkbank MCP server

[![AICTIONBOT™ Werkbank MCP server](https://mcprush.com/badge/aictionbot-werkbank-mcp/card.svg)](https://mcprush.com/to/aictionbot-werkbank-mcp?ref=badge)

Procurement functions for small and mid-sized businesses and for the AI agents companies already run, by [KULIC Advisory](https://www.kulicadvisory.com/) (Cologne), as a public remote MCP server.

- **Endpoint:** `https://www.kulicadvisory.com/mcp` (Streamable HTTP, stateless, JSON-RPC 2.0)
- **Version:** 1.33.0, **100 tools**
- **Open without sign-in:** 12 tools for looking things up and 4 for reading or editing an existing Shared Table.
- **74 checks without AI** (including NDA, contract drafts, RFQ, template fill and opening a Shared Table): with an AICTIONBOT™ Werkbank licence, trial week, contract key or partner key; without a licence one check per connection every 30 days is free after signing in with “Connect without a licence”.
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
| `explain_term` | Explain a procurement term in plain words: the Purchasing Glossary of the AICTIONBOT™ Workbench (164 terms, German and English) |
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

## Checks without AI (73)

| Tool | What it does |
|---|---|
| `check_price_increase` | Check a supplier price increase against official market data (Germany) |
| `screen_sanctions` | Screen a company or person against public sanctions lists |
| `calculate_notice_deadline` | Calculate the last day to give notice on a contract |
| `check_discount_window` | Find early-payment discounts (Skonto) that expire in the next days, and which payment run still catches them; with `critical_suppliers` a payment run priority (critical suppliers first, blocked invoices with the reason and who clears the block) |
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
| `create_contract_draft` | Draft a contract from the KULIC Advisory templates: service agreement, service level agreement, framework agreement for call-offs, master service agreement with statements of work, or supply agreement for production materials and related services, in German or English (a draft, not legal advice) |
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
| `describe_role` | Role profile from a job title, level, approval limit and RACI per activity: purpose, KPIs, skills, segregation-of-duties checks and a job advertisement in German and English |
| `write_buying_policy` | One-page buying policy from three value limits: five questions before every purchase (quotes, specification, award note, contract, approval), answer for one purchase, and a check of an order list against the rules with possible order splitting |
| `build_service_catalogue` | Service catalogue for a procurement team in three levels with requester, response and cycle time in working days and what the department must provide; or a check of the team's own list |
| `build_handover_file` | Handover file when someone leaves or goes on holiday: what to settle before the last day (approvals tied to the person, deadlines in the absence, overdue items), what falls due during the absence, contacts, load per deputy |
| `check_switchover` | Switch-over check for a new system or a new supplier: twelve-point checklist dated from the go-live, readiness traffic light from the team's own list, gaps and a Q&A sheet for staff |
| `analyse_issues` | Issue radar: groups a list of procurement or invoice problems into ten recurring causes, with share, open cases, the fix per cause, typical age, cases older than 30 days, open cases per owner and repeat suppliers |
| `sort_categories` | Category sorter: assigns order or booking texts to a category tree of 30 categories in nine groups, with spend per group and category and rows left open |
| `suggest_accounts` | Account helper: suggested general ledger account under the German standard charts SKR03 or SKR04 per invoice line, uncertain lines marked, total per account (not tax advice) |
| `navigate_symptoms` | Symptom navigator: nine procurement symptoms rated 0 to 5 become, strongest first, what each costs, the first step for this week, the matching tools and the matching step of the KULIC ladder |
| `build_buying_tiles` | Buying tiles: an internal page of twelve tiles that tells employees where to order what, with the channel, the rule and the owner per tile, and an answer to a single question such as where to order toner |
| `write_invoice_letter` | Invoice letter: a letter to suppliers in German and English with the invoice requirements, the purchase order number rule, the e-invoice format and the invoice address, with missing details marked (not legal or tax advice) |
| `check_einvoice` | E-invoice checker: reads the XML of an XRechnung or ZUGFeRD invoice (UBL or CII) and checks mandatory details, net plus tax against gross, the lines against the net total and tax per rate (not a full schema validation, not tax advice) |
| `plan_request_to_offer` | Request to offer: a dated route from a customer request through supplier quotes to the own offer, with validity checks, the cheapest valid quote, the selling price with mark-up and RFQ and reminder texts in German and English |
| `check_expenses` | Expense checker: travel expense claims against the official German per diem, mileage and overnight rates as of 1 January 2026 (Germany and all 214 destinations of the Federal Finance Ministry letter of 5 December 2025), with double submissions, overlaps, missing receipts and weekend trips; without a list, the rates for one destination (not tax advice) |
| `create_einvoice` | Write an invoice: a German e-invoice as ZUGFeRD/Factur-X EN 16931 or XRechnung 3.0 (UN/CEFACT CII XML), calculated in cents, with the mandatory details of section 14 UStG, the EN 16931 rules and the XRechnung rules (BR-DE) checked; small business, reverse charge, intra-community supply and export with the exemption reason; the Workbench page turns it into a PDF/A-3 with the XML embedded (not tax advice) |
| `reconcile_supplier_statement` | Statement reconciliation: a supplier's statement against your own open items and payments; per document paid (with date), open, blocked with the reason, unknown on your side, listed twice or with a different amount; credit notes the supplier has not deducted; totals and a ready reply letter to the supplier |
| `check_approval_backlog` | Approval backlog radar: open approvals per approver with number, amount and oldest age in days; documents overdue, with an expiring cash discount, waiting too long or with an absent approver; discount at risk in euros; remind or reroute to the deputy; a ready reminder |
| `check_blanket_orders` | Blanket order guard: remaining budget, share used and use per month per blanket or limit order; the day the budget is expected to run out against the end of the term; open invoices without cover; next step (top up, renegotiate, framework contract, follow-up order) |
| `compare_contracts` | Contract comparison: old and new version of a contract side by side, section by section; changed, new, removed and renumbered clauses with the sentence before and now; numbers, deadlines and dates before and after; price, payment, termination, liability and penalty changes flagged red; ready questions for the other side. Not legal advice |
| `compare_offer_to_contract` | Offer against contract: price, payment, term, termination, warranty and liability from the offer next to the contract; what is missing in the contract, what is only in the contract, agreed points ticked off one by one; ready message to the other side. Not legal advice |
| `compare_vendor_master` | Vendor master old against new: changed bank details (red before the next payment), account country changes, new vendors with gaps, the same bank account with two vendors, removed vendors; next step per case. Bank details are shortened in the result |
| `compare_offer_rounds` | Revised offer: is round 2 really cheaper? The difference between first and revised offer split into price, quantity, removed and new items; every item that became more expensive; ready questions for the supplier |
| `compare_spend_periods` | Spend year against year: price effect and volume effect per article, category or supplier, new and dropped entries, the largest price increases first, next step |
| `claim_price_reduction` | Claim a price reduction: has the market fallen since the last price agreement? Official Eurostat index for Germany, the claim in percent and euros per year, a ready message to the supplier and the objections to expect. Says plainly when the index gives no claim |
| `compare_invoices` | Invoice against previous invoice: every item that is more expensive than last time, new items, quantity jumps, the difference split into price, quantity, new and dropped; ready questions for the supplier |
| `compare_invoice_to_contract` | Invoice against contract: every item billed above the agreed price with the overbilled amount, items that are not in the contract, the invoice total at contract prices and a ready message asking the supplier for a credit note |
| `compare_approval_matrix` | Approval matrix old against new: limits raised, deputies removed, approvers who are their own deputy, areas left without an approver, new and removed approval rights, who may approve more than before; the questions to answer before the matrix is loaded |
| `supplier_error_profile` | Supplier error profile: which supplier makes which errors in a list of clarification cases (nine error types by keywords), hours and cost of clarification, the five suppliers with the most cases and a ready letter per supplier with their three most frequent errors |
| `order_to_payment_status` | Order-to-payment status overview: from one export of requisitions, orders, goods receipts and invoices what is stuck where (invoice waiting for goods receipt, blocked, open to order, open to receive, goods receipt without invoice), open cases per cost centre and the next steps with who has to act |
| `compare_sourcing_plans` | Sourcing plan old against new: categories dropped from the plan, targets removed or lowered, due dates moved, changed approach, the planned effect per year before and after and the questions before approval |
| `check_nda` | Check their NDA: a non-disclosure agreement from the other side against twelve standard points by keywords (German and English texts), what goes beyond the usual (penalty, non-solicitation, non-compete, transfer of rights, unlimited liability, no end date) and what is missing. Not legal advice |
| `compare_scope_of_work` | Scope of work old against new: dropped sections, changed figures, quantities and deadlines, new restrictions such as not included or at extra cost, new duties for the customer, ready questions for the other side |
| `automation_portfolio` | Automation portfolio: per use case the hours and euros saved per year, the one-off cost and the payback in months from your own figures, sorted into three phases, with the cases that save no time and the ones that already work without AI |
| `check_quantities` | Quantity and unit check: ordered against received quantity per line with the cause (different unit with the probable factor, over-delivery, lot size, under-delivery), the amount and the fix |
| `find_responsible` | Who is responsible: from your own list of topics, people in charge, deputies and value limits, the answer to who to ask and who may sign an amount, a notice sorted by topic and the gaps (two people in charge, no deputy, amount above every limit) |
| `sort_questions` | Question sheet for your own purchasing help: collected questions sorted into nine topics, near-identical ones merged with a count, the answer next to each, open ones marked with the tool that helps. Sorts your questions and answers, writes none itself |

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
