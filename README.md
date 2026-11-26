# GetEstimatED — South African building cost estimates (MCP server)

Remote [Model Context Protocol](https://modelcontextprotocol.io) server for **South African building costs**, by [GetKonnektED](https://getkonnekted.com) (Konnektivity (Pty) Ltd t/a GetKonnektED, reg. 2026/363576/07).

**Server URL:** `https://getestimated.co.za/api/mcp/estimate`. It uses Streamable HTTP. The four cost-guide tools are free and need **no sign-in**. The account tools use the person's own GetEstimatED sign-in (OAuth).

Listed on the [official MCP Registry](https://registry.modelcontextprotocol.io) as `za.co.getestimated/sa-estimate`.

## Tools

| Tool | Sign-in | What it does |
|---|---|---|
| `sa_building_rate_lookup` | no | Approximate all-in South African rate for an item of work, per unit |
| `sa_material_price_index` | no | Indicative retail price of a building material, by region |
| `sa_quick_estimate` | no | Ballpark cost to build a house or addition from its floor area (low, expected, high) |
| `sa_check_quote` | no | Marks each line of a building quote as below, in or above the usual range |
| `list_my_projects` | yes | The person's own projects and latest estimates |
| `get_my_bill` | yes | One of their estimates (bill of quantities by Estie), with download links |
| `compare_bill_to_quote` | yes | A builder's quote compared line by line with their own estimate |
| `estimate_from_brief` | yes | A new priced bill of quantities from a written brief (two steps, uses an estimate credit) |
| `buy_estimate_pack` | yes | Buy estimate credits via a Paystack payment link (two steps) |

All figures are indicative estimates. They are not a quotation and not a quantity surveyor's sign-off.

## Connect

- **Claude:** Settings → Connectors → add a custom connector with the server URL.
- **ChatGPT:** Settings → Apps & Connectors → developer mode → create a connector with the server URL.
- **Gemini CLI:** `gemini extensions install https://github.com/Getkonnekted-AI/getestimated-mcp`, or `gemini mcp add --transport http getestimated https://getestimated.co.za/api/mcp/estimate`
- **Claude Code:** `claude mcp add --transport http getestimated https://getestimated.co.za/api/mcp/estimate`

## Example questions

- "Roughly what does it cost to build a 180 m² house in Pretoria?"
- "What's the going rate for 230 mm brickwork per m² in Gauteng?"
- "Here's my builder's quote — are any of these rates out of line?"

## Terms and privacy

- Terms: https://getkonnekted.com/terms.html
- Privacy: https://getkonnekted.com/privacy.html
- Support: support@getkonnekted.com

This repository holds listing files only (server metadata, a Gemini CLI extension manifest and client examples). The server itself is hosted by GetKonnektED.
