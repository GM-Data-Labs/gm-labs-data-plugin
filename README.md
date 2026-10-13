# GM Labs Data (Grok plugin)

One-step access from Grok to GM Labs' public, pay-per-result Apify Actors through Apify's hosted MCP server.

## Included Actors
| Family | Actor |
|---|---|
| Government filings | `appetizing_horsefly/ttb-alcohol-permits`, `appetizing_horsefly/ucc-filings-feed`, `appetizing_horsefly/dot-bid-results` |
| Jobs | `appetizing_horsefly/ats-jobs-scraper` |
| Web capture | `appetizing_horsefly/fast-full-page-screenshot` |

## Setup
1. Create a free Apify account and copy your API token (Apify Console → Settings → API & Integrations).
2. `export APIFY_TOKEN=apify_api_...` in the shell that launches Grok. The token is never stored in this plugin.
3. Install the plugin. Runs are billed to your Apify account at each Actor's published pay-per-result price.

## Network endpoints & credentials
- Only endpoint: `https://mcp.apify.com` (Apify hosted MCP), which runs the Actors on Apify.
- Only credential: `APIFY_TOKEN`, sent as `Authorization: Bearer` to mcp.apify.com.
- The MCP URL is scoped with `?tools=` to exactly the five Actors above. Apify's hosted MCP also adds 4 run/dataset helper tools (`get-actor-run`, `get-dataset-items`, `get-key-value-store-record`, `abort-actor-run`) to fetch results or stop a run; no store search, generic `call-actor`, or docs tools are loaded.
- No hooks, scripts, commands, or telemetry.

## License
MIT
