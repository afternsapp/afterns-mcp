# afterns MCP

US stock earnings data for AI assistants. Ask in Korean or English how a stock moved after its earnings, whether it beat estimates, and when it reports next.

- Remote endpoint (Streamable HTTP): `https://afterns.com/api/mcp`
- No sign-in, no API key, read-only
- Website: [afterns.com](https://afterns.com)

## Tools

| Tool | What it returns |
|---|---|
| `search_stocks` | Ticker lookup by name, including Korean names and nicknames (엔비디아 → NVDA) |
| `get_earnings_reactions` | Next-day price move after each of the last 12 reports, beat/miss, next report date |
| `get_earnings_calendar` | Upcoming US earnings for up to 14 days, with Korea time |
| `get_earnings_call_summary` | Latest earnings call: one-line takeaway, positives, concerns, quotes |

Every result links to the stock's afterns page as the source. Historical data only; it does not predict prices.

## Connect

Add `https://afterns.com/api/mcp` as a custom (remote) MCP connector in your client.

## 한국어

미국 주식 실적 발표 뒤 다음 날 주가가 어떻게 움직였는지, 기대치를 넘었는지, 다음 발표가 한국시간 언제인지 AI에게 바로 물어볼 수 있는 MCP 서버입니다. 로그인 없이 읽기 전용으로 씁니다.

## Data

Earnings figures from SEC EDGAR filings, estimates and prices from Yahoo Finance aggregates. This repository holds only the registry metadata (`server.json`); the server runs on afterns.com.
