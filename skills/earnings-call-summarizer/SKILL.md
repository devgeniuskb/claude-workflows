---
name: earnings-call-summarizer
description: Turn an earnings call transcript or press release into a structured summary - key metrics vs. expectations, forward guidance, management tone, and analyst Q&A highlights - for educational and informational purposes only. Use when the user has an earnings call transcript or report and wants it distilled.
---

# Earnings Call Summarizer

## Purpose
Earnings calls bury the material information in an hour of prepared remarks and Q&A. This skill extracts what actually moved or matters - numbers versus expectations, guidance changes, and what management dodged or emphasized in Q&A - as a factual summary, without translating any of it into a trade signal.

## When to use
The user provides (or references) an earnings call transcript, press release, or report and wants a distilled summary.

## Process
1. **Confirm the source material.** Work from the actual transcript/release text provided; if only asked about a company's "latest earnings" with no text given, say the transcript wasn't provided and ask for it or state that results are based on general knowledge which may not reflect the most recent quarter.
2. **Extract headline metrics**: revenue, EPS, and other metrics the company itself emphasizes, each compared against prior period and against analyst expectations where stated in the source - with the reporting period clearly labeled.
3. **Extract forward guidance**: any updated guidance for future periods, and explicitly note whether it was raised, lowered, maintained, or newly introduced/withdrawn compared to prior guidance if that context is available in the source.
4. **Characterize management tone** from the prepared remarks - confident, cautious, hedging - grounded in specific word choices or claims quoted from the transcript, not a vibe-based label with no evidence.
5. **Summarize the Q&A section** separately: which analyst questions got direct answers, which got deflected or vague responses, and any information disclosed in Q&A that wasn't in the prepared remarks - this section often contains the most informative material in the whole call.
6. **List any red flags or notable risks** mentioned (litigation, guidance cuts, margin pressure, customer concentration, management changes) factually, without editorializing into investment implications.

## Output format
- Source and reporting period
- Headline metrics vs. prior period / expectations
- Forward guidance (and how it changed, if known)
- Management tone (with supporting quotes/paraphrases)
- Q&A highlights (direct answers vs. deflections)
- Red flags/risks noted
- Disclaimer (see Guardrails)

## Guardrails
This is not financial advice and does not include a buy/sell/hold recommendation or price prediction - state this explicitly. Do not fabricate figures, quotes, or guidance not present in the provided source material; if a detail isn't in the transcript, say it wasn't disclosed rather than filling the gap.
