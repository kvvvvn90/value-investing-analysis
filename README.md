# value-investing-analysis

An AI agent skill for value investing analysis, valuation, moat assessment, cycle positioning, and investment memo writing for listed technology companies.

## Overview
This skill is designed for structured value investing analysis of publicly listed technology companies. It combines financial data collection, valuation frameworks, moat analysis, cycle positioning, and final investment memo writing into a single workflow.

## What it does
- Collects the latest financial data for the most recent 4 quarters
- Compares key metrics with major competitors
- Runs Graham margin-of-safety valuation
- Performs Buffett-style moat analysis
- Applies Howard Marks-style cycle thinking
- Produces a final investment report in `.md` format

## Final output
The final deliverable is a structured investment report in Markdown (`.md`) format.

By default, the report includes:
1. Data Collection
2. Graham Margin-of-Safety Valuation
3. Buffett Moat Analysis
4. Howard Marks Cycle Thinking
5. Investment Memo

## Recommended usage
This skill focuses on structured investment reasoning and Markdown report generation.

If you want charts, dashboards, or a more presentation-oriented output, it is recommended to pair this skill with any visualization skill.

## Core frameworks
- Graham Margin-of-Safety Valuation
- Buffett Moat Analysis
- Howard Marks Cycle Thinking

## Repository structure
- `SKILL.md` — main skill definition
- `references/` — detailed supporting references and templates

## Notes
- The skill is designed for real-time public data usage
- Missing data should be explicitly marked rather than fabricated
- The final output should follow a structured five-part analysis format
