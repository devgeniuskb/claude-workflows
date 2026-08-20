---
name: stock-research-brief
description: Research a public company or ticker and produce a structured, sourced research brief - business overview, recent financials, recent news, and bull/bear points - for educational and informational purposes only. Use when the user wants to understand a company or stock better, not when they want a buy/sell recommendation.
---

# Stock Research Brief

## Purpose
This skill organizes publicly available information about a company into a structured brief - it does not predict price movement or tell the user what to do with their money. The value is in comprehensive, sourced, balanced research; the decision stays entirely with the user (and, given the stakes, ideally a licensed financial advisor).

## When to use
The user wants to understand a company or stock better - its business, recent performance, and current narrative - for their own research process.

## Process
1. **Identify the company and ticker precisely** - confirm which entity/exchange if there's any ambiguity (common names can map to multiple tickers).
2. **Business overview**: what the company actually does, its main revenue segments, and its position relative to competitors - in plain language, not jargon copied from a press release.
3. **Recent financials**, sourced from available data: revenue/earnings trend over recent periods, margin trend, and balance sheet notes (debt load, cash position) if available - explicitly note the as-of date/period for every figure, since financials go stale fast.
4. **Recent news and catalysts**: material recent developments (earnings releases, guidance changes, product launches, litigation, management changes, macro exposure) with dates and sources.
5. **Bull case and bear case**, presented with genuine symmetry: the strongest reasonable argument for optimism and the strongest reasonable argument for concern, each grounded in the facts gathered above - not hedged into meaninglessness, but not one-sided either.
6. **State data recency and gaps** explicitly: what's current as of the research, what's missing or hard to verify, and that markets move faster than any static brief.

## Output format
- Company/ticker identification
- Business overview
- Recent financials (with as-of dates, sourced)
- Recent news/catalysts (with dates, sourced)
- Bull case / bear case (symmetric)
- Data recency and gaps note
- Disclaimer (see Guardrails)

## Guardrails
This is not financial advice, an investment recommendation, or a prediction of future performance. Always close the brief with an explicit statement to that effect and a suggestion to consult a licensed financial advisor before making investment decisions. Never state a price target, "buy"/"sell"/"hold" recommendation, or probability of a specific outcome. Do not fabricate financial figures - cite sources and clearly flag any figure that couldn't be verified.
