<div align="center">

<a href="https://sharpapi.io"><img src="https://sharpapi.io/icon-192x192.png" width="84" alt="SharpAPI logo"></a>

# SharpAPI

**The real-time sports betting odds API for developers.**

Build with live odds, fair probabilities, and betting opportunities from 45+ sportsbooks.
Access normalized data through our SDKs, REST API, or real-time streams.

[![PyPI](https://img.shields.io/pypi/v/sharpapi?label=pypi%20sharpapi&color=06b6d4)](https://pypi.org/project/sharpapi/)
[![npm](https://img.shields.io/npm/v/%40sharp-api%2Fclient?label=npm%20%40sharp-api%2Fclient&color=06b6d4)](https://www.npmjs.com/package/@sharp-api/client)
[![Docs](https://img.shields.io/badge/docs-docs.sharpapi.io-06b6d4)](https://docs.sharpapi.io)
[![Free tier](https://img.shields.io/badge/free%20tier-no%20credit%20card-06b6d4)](https://sharpapi.io/pricing)

[Website](https://sharpapi.io) · [Documentation](https://docs.sharpapi.io) · [Pricing](https://sharpapi.io/pricing) · [Discord](https://discord.com/invite/vz3yX5dJpv) · [X](https://x.com/Sharp_API)

</div>

**[Get a free API key](https://sharpapi.io/pricing)** · [Read the documentation](https://docs.sharpapi.io)

The free tier includes DraftKings and FanDuel. No credit card required.

## Quick start

```bash
npm install @sharp-api/client        # TypeScript / JavaScript
pip install sharpapi                 # Python
```

```ts
import { SharpAPI } from '@sharp-api/client'

const api = new SharpAPI('sk_live_...')
const { data: odds } = await api.odds.get({
  sportsbook: 'draftkings',
  league: 'nba',
})
console.log(odds)
```

```python
from sharpapi import SharpAPI

client = SharpAPI("sk_live_...")
odds = client.odds.get(sportsbook="draftkings", league="nba")
print(odds.data)
```

`GET /odds` returns paginated odds across supported sportsbooks and markets in one
schema. The API also
serves pre-computed opportunities: `/opportunities/ev` (Pinnacle no-vig reference),
`/opportunities/arbitrage`, and `/opportunities/middles`, plus player props, game state,
and historical odds with closing lines.

## Repositories

| Repository | Description |
|---|---|
| [SharpAPI-Python](https://github.com/Sharp-API/SharpAPI-Python) | Python SDK · `pip install sharpapi` |
| [SharpAPI-TS](https://github.com/Sharp-API/SharpAPI-TS) | TypeScript / JavaScript SDK · `@sharp-api/client` |
| [SharpAPI-MCP](https://github.com/Sharp-API/SharpAPI-MCP) | MCP server for compatible AI applications |
| [SharpAPI-R](https://github.com/Sharp-API/SharpAPI-R) | R client · submitted to CRAN, review pending |
| [SharpAPI-Sample-Data](https://github.com/Sharp-API/SharpAPI-Sample-Data) | World Cup and MLB odds samples · CC BY 4.0 |

[API reference and guides](https://docs.sharpapi.io) · Available in English, German, Spanish, and Brazilian Portuguese.

## Sample datasets

The [sample dataset](https://github.com/Sharp-API/SharpAPI-Sample-Data) is free under
CC BY 4.0: real multi-book odds snapshots ready for pandas or R, with a citation block for
research use. The live feed behind it starts at $0: [get a free API key](https://sharpapi.io/pricing),
no credit card required.

---

<div align="center">
<sub>Odds are informational market data, not betting advice. Sports betting involves financial
risk, is legal only where permitted, and is restricted to those of legal age (21+ in most US
states). Please wager responsibly.</sub>
</div>
