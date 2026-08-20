---
name: portfolio-review-checklist
description: Given a list of investment holdings, produce a structured, educational review - diversification, concentration risk, sector/asset-class exposure, and questions worth asking - without recommending trades. Use when the user wants a structured look at their existing portfolio's composition and risk exposure.
---

# Portfolio Review Checklist

## Purpose
This skill organizes an existing portfolio's composition so the user can see their own exposure clearly - concentration, overlap, sector tilt - and surfaces questions worth asking. It does not recommend buying, selling, or rebalancing into specific positions; that crosses from organizing information into giving investment advice, which is outside what this skill should do.

## When to use
The user provides a list of holdings (stocks, funds, crypto, etc., with rough position sizes) and wants a structured review of composition and risk exposure - not a trade recommendation.

## Process
1. **Take the holdings list as given** - don't second-guess or fill in missing positions; work only with what's provided, and note explicitly if position sizes are missing (composition analysis needs weights, not just tickers).
2. **Categorize by asset class and sector/theme**: equities vs. bonds vs. cash vs. crypto vs. other, and within equities, sector or thematic groupings - to reveal exposure that isn't obvious from a flat list of tickers.
3. **Compute concentration**: largest single positions as a percentage of the whole portfolio, and flag where a small number of holdings dominate total exposure - concentration isn't inherently wrong, but it should be a deliberate choice, not an accident of not looking.
4. **Check for overlap**: holdings that are effectively correlated or redundant (e.g. multiple funds tracking similar indices, or several individual stocks in the same narrow sector) which understate true concentration if counted as "diversified" just because the ticker count is high.
5. **Note diversification gaps**: asset classes, geographies, or sectors entirely absent from the portfolio, stated as an observation ("no international equity exposure") rather than a directive ("you should buy international funds").
6. **List questions worth the user asking themselves or an advisor**: e.g. "does this concentration match your risk tolerance and time horizon?", "is this sector tilt intentional?" - framed as prompts for the user's own decision process, not recommendations.

## Output format
- Portfolio composition table (asset class / sector / position / % of total)
- Concentration findings
- Overlap/correlation findings
- Diversification gaps (observations, not directives)
- Questions worth asking
- Disclaimer (see Guardrails)

## Guardrails
This is not financial advice and does not recommend buying, selling, or rebalancing any position - always state this explicitly and suggest a licensed financial advisor for actual decisions. Never suggest specific replacement securities or a target allocation; describe the current composition and risk exposure only, and leave the "what to do about it" entirely to the user.
