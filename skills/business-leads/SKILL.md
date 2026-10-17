---
name: gm-labs-business-leads
description: Find fresh local-business leads with GM Labs Actors - newly issued liquor licenses and pending applications (California ABC, New York SLA, Texas TABC) and newly formed LLCs/corporations (Colorado, Connecticut, New York, Oregon). Use when the user asks for new liquor licenses, new bars/restaurants, new LLC or business formations.
---

# Business leads (GM Labs Data)

Tools come from the `gm-labs-data` MCP server (Apify). Each run bills the user's Apify account per result, so always set `maxResults` and confirm before large pulls.

| Need | Actor tool | Price |
|---|---|---|
| Newly issued liquor licenses / new applications (CA, NY, TX) | `appetizing_horsefly/liquor-license-feed` | ~$0.004 per license |
| Newly formed LLCs, corporations, partnerships (CO, CT, NY, OR) | `appetizing_horsefly/new-business-filings` | ~$0.003 per filing |

## Key inputs
- `liquor-license-feed`: `states` (CA/NY/TX), `recordTypes` (`issued`, `application`), `sinceDate` (YYYY-MM-DD, default last 14 days), `cityContains`, `countyContains`, `licenseTypeContains`, `maxResults` (default 100).
- `new-business-filings`: `states` (CO/CT/NY/OR), `sinceDate` (default last 7 days), `untilDate`, `entityKinds` (`llc`, `corporation`, `partnership`, `nonprofit`, `other`), `includeForeign`, `excludeRejected`, `nameContains`, `cityContains`, `maxResults` (default 200).

## Examples
- "Use GM Labs Data to list new liquor license applications in Austin, TX this week."
- "Get 50 new LLCs formed in Colorado since Monday with GM Labs Data."
- "Find newly formed construction companies in Oregon with GM Labs Data."

Tip: start with a small `maxResults` (e.g. 5) to see the output shape before larger pulls.
