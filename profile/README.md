<div align="center">

<a href="https://sharpapi.io"><img src="https://sharpapi.io/icon-192x192.png" width="84" alt="SharpAPI logo"></a>

# SharpAPI

**The real-time sports betting odds API for developers.**

Live odds from 45+ US sportsbooks in one normalized schema, with built-in no-vig fair odds,
+EV and arbitrage detection, and sub-89ms P50 SSE streaming.

[![PyPI](https://img.shields.io/pypi/v/sharpapi?label=pypi%20sharpapi&color=06b6d4)](https://pypi.org/project/sharpapi/)
[![npm](https://img.shields.io/npm/v/%40sharp-api%2Fclient?label=npm%20%40sharp-api%2Fclient&color=06b6d4)](https://www.npmjs.com/package/@sharp-api/client)
[![Docs](https://img.shields.io/badge/docs-docs.sharpapi.io-06b6d4)](https://docs.sharpapi.io)
[![Free tier](https://img.shields.io/badge/free%20tier-no%20credit%20card-06b6d4)](https://sharpapi.io/pricing)

[Website](https://sharpapi.io) · [Documentation](https://docs.sharpapi.io) · [Pricing](https://sharpapi.io/pricing) · [Discord](https://discord.com/invite/vz3yX5dJpv) · [X](https://x.com/Sharp_API)

</div>

## Quick start

```bash
npm install @sharp-api/client        # TypeScript / JavaScript
pip install sharpapi                 # Python
```

```ts
import { SharpAPI } from '@sharp-api/client'

const api = new SharpAPI('sk_live_...')
const { data: odds } = await api.odds.get({ league: 'nba' })
const { data: arbs } = await api.arbitrage.get({ min_profit: 1 })
```

```python
from sharpapi import SharpAPI

client = SharpAPI("sk_live_...")  # free key at sharpapi.io
evs = client.ev.get(min_ev=3.0, sport="basketball")
```

`GET /odds` returns paginated odds across supported sportsbooks and markets in one
schema. The API also
serves pre-computed opportunities: `/opportunities/ev` (Pinnacle no-vig reference),
`/opportunities/arbitrage`, and `/opportunities/middles`, plus player props, game state,
and historical odds with closing lines.

## Repositories

| Repo | What it is |
|---|---|
| [SharpAPI-TS](https://github.com/Sharp-API/SharpAPI-TS) | Official TypeScript/JavaScript SDK (`@sharp-api/client` on npm) |
| [SharpAPI-Python](https://github.com/Sharp-API/SharpAPI-Python) | Official Python SDK (`sharpapi` on PyPI) |
| [Documentation](https://docs.sharpapi.io) | API reference and guides (EN, DE, ES, PT-BR) |
| [SharpAPI-Sample-Data](https://github.com/Sharp-API/SharpAPI-Sample-Data) | Free odds dataset: 2026 FIFA World Cup + MLB, 23 sources (sportsbooks + prediction markets), CC BY 4.0 |
| [SharpAPI-R](https://github.com/Sharp-API/SharpAPI-R) | R client, CRAN submission in progress |

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
