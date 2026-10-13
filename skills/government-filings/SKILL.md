---
name: gm-labs-government-filings
description: Pull US government filings with GM Labs Actors - TTB alcohol producer/importer permits, new UCC-1 lien filings, and state DOT (WSDOT, Caltrans) bid results. Use when the user asks for TTB permits, UCC filings, or DOT bid tabs.
---

# Government filings (GM Labs Data)

Tools come from the `gm-labs-data` MCP server (Apify). Each run bills the user's Apify account per result, so start with defaults or small limits and confirm before large pulls.

| Need | Actor tool |
|---|---|
| Licensed US wineries, distillers, brewers, importers | `appetizing_horsefly/ttb-alcohol-permits` |
| Newly filed UCC-1 liens | `appetizing_horsefly/ucc-filings-feed` |
| DOT bid tabulations / contract awards | `appetizing_horsefly/dot-bid-results` |

## Examples
- "Use GM Labs Data to list new TTB distillery permits in Texas."
- "Get this week's new UCC-1 filings with GM Labs Data."
- "Show the latest Caltrans bid results with GM Labs Data."

Tip: each Actor's input schema is shown by the MCP tool; run with default input first to see the output shape.
