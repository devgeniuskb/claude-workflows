---
name: deep-research
description: Conduct multi-round web research on a question or topic and produce a structured, cited report - using iterative search-and-summarize passes to keep token usage low on large research tasks while preserving accuracy. Use when the user needs a well-sourced answer to a non-trivial research question, not a single quick lookup.
---

# Deep Research

## Purpose
A single search-and-answer pass misses nuance, conflicting sources, and follow-up questions the first results raise. This skill runs research as multiple rounds - each narrowing or verifying the last - and compresses findings incrementally rather than carrying every raw source in context, so large research tasks stay accurate without ballooning token usage.

## When to use
The question requires synthesizing multiple sources, checking claims against each other, or exploring a topic the user doesn't already have a narrow answer for - not a single fact lookup.

## Process
1. **Decompose the question** into 2-5 sub-questions that together answer the main question. A vague broad query returns vague broad results; specific sub-questions return checkable claims.
2. **Round 1 - broad pass**: search each sub-question, and instead of keeping full page contents in context, extract and record only the claim, the source, and a confidence note (well-supported / single-source / contradicted) before moving to the next sub-question. This is the key token-efficiency move: summarize-then-discard per source rather than accumulating raw pages.
3. **Identify gaps and contradictions** after the broad pass: sub-questions with only one weak source, or claims that conflict across sources.
4. **Round 2 - targeted pass**: search specifically to resolve the gaps and contradictions found, not to re-cover ground already well-supported. This is what makes it "deep" rather than "wide" - effort concentrates where the answer is still uncertain.
5. **Weigh source quality**, not just source count: prefer primary sources, official documentation, or named-expert analysis over aggregator content or unattributed claims; note when a claim rests only on lower-quality sources.
6. **Synthesize the report** from the accumulated claim-source-confidence notes, not by re-reading raw pages - organize by sub-question or theme, state where sources agree versus disagree, and cite every non-obvious claim.

## Output format
- Research question and sub-questions
- Findings organized by sub-question/theme, each claim cited
- Explicit notes on disagreement between sources, where it exists
- Confidence assessment per major claim (well-supported / limited evidence / disputed)
- Open questions that remain unresolved after research

## Guardrails
Never state a claim as fact without a source behind it - if research doesn't turn up a clear answer, say so rather than filling the gap with plausible-sounding inference. Attribute claims to sources accurately; do not merge or misattribute findings between sources when compressing notes.
