---
name: go-live-diagnosis
description: Diagnose why a seller's products are not live yet on each of its marketplace targets (bol.com, Kaufland, Mirakl operators, Amazon, ...), and what to fix first, using the Section11 connector. Use when the user asks what blocks go-live, why products are not live yet on a marketplace, or where their catalog is stuck in the go-live funnel.
---

# Go-live diagnosis

Run the Section11 MCP prompt `marketplace_why_not_live`. If your client does not offer MCP
prompts, call `get_consultant_playbook(theme="opportunities")` and follow analysis 7.1 (or 7.3
for one product): start from the marketplaces' own reasons, and use the theme's
reason-to-action table to say who acts. Then, for the work Section11 itself can do, call
`get_consultant_playbook(theme="readiness")` and follow its "Go-live diagnosis" analysis (1.6).
Those analyses hold the steps and the correctness rules. Follow them exactly, and don't answer from memory.

It uses the tools `get_opportunity_summary`, `list_opportunities`, `whats_blocking_this_offer`,
`list_catalog_products` and `get_product_go_live_readiness`.

If the connection is granted more than one account, ask which account the user means (`whoami`
lists them) and pass its `account_id`. Never pick an account for them.
