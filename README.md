# afterns MCP

US stock earnings data for AI assistants. Ask in Korean or English how a stock moved after its earnings, whether it beat estimates, and when it reports next.

- Remote endpoint (Streamable HTTP): `https://afterns.com/api/mcp`
- No sign-in, no API key, read-only
- Covers 1,270+ US-listed stocks
- Website: [afterns.com](https://afterns.com)

## Tools

| Tool | What it returns |
|---|---|
| `get_earnings_reactions` | For each recent report (up to 12 per answer, about three years): the next-day price move, EPS vs. estimate and surprise %, revenue growth, and whether it reported before the open or after the close. Plus how often the stock rose, its average move, how many times it fell after beating estimates, and the next report date in Korea and US Eastern time |
| `get_earnings_calendar` | Upcoming US earnings for up to 14 days, biggest names first, with Korea time and session. Filter by group: big tech, semiconductors, software, memory, healthcare, space |
| `get_earnings_call_summary` | The latest earnings call in a few lines: one-line takeaway, positives, concerns, and up to three management quotes |
| `search_stocks` | Ticker lookup by name, including Korean names and nicknames (엔비디아 → NVDA, 구글 → GOOGL) |

The next-day move is measured from the right session: same-day close for reports before the open, next trading day for reports after the close.

Every result links to the stock's afterns page as the source. Historical data only; it does not predict prices.

## Try asking

- "How did Nvidia's stock move after its recent earnings?"
- "What big tech earnings are coming up next week?"
- "Summarize Microsoft's latest earnings call."
- "엔비디아 실적 발표 언제야? 한국시간으로"

## Connect

Add `https://afterns.com/api/mcp` as a custom (remote) MCP connector in your client.

## 한국어

미국 주식 1,270여 종목의 실적 발표 기록을 AI에게 바로 물어볼 수 있는 MCP 서버입니다. 발표 다음 날 주가가 어떻게 움직였는지, 기대치를 넘었는지, 다음 발표가 한국시간 언제인지, 최근 어닝콜에서 무슨 말이 나왔는지 알려 줍니다. 로그인 없이 읽기 전용으로 씁니다.

## Data

Earnings figures from SEC EDGAR filings, estimates and prices from Yahoo Finance aggregates. This repository holds only the registry metadata (`server.json`); the server runs on afterns.com.
