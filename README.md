# Value Investing Analysis

**An AI agent skill for structured value investing analysis on tech stocks**  
(Graham valuation + Buffett moat + Howard Marks cycle thinking → clean Markdown report, easily extendable to visualizations)

**Visualization Examples** (Tesla analysis, paired with [Data Analyst skill](https://github.com/openclaw/skills/tree/main/skills/oyi77/data-analyst))

<table>
  <tr>
    <td><img src="examples/tesla_value_investing_visual_report 1.png" alt="Tesla Value Investing Report - Part 1" width="100%"></td>
    <td><img src="examples/tesla_value_investing_visual_report 2.png" alt="Tesla Value Investing Report - Part 2" width="100%"></td>
  </tr>
</table>

These screenshots show interactive dashboard outputs generated from the skill's Markdown report.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![ClawHub](https://img.shields.io/badge/Install%20on-ClawHub-blue)](https://clawhub.ai/skills/value-investing-analysis)

## Overview
This skill performs deep value investing analysis on publicly listed **technology companies** using classic frameworks, with real-time public data collection and strict no-fabrication rules.

## What it does
- Collects latest 4-quarter financials (revenue, margins, FCF, debt etc.) from public sources
- Compares key metrics with 2-3 major competitors
- Runs Graham margin-of-safety valuation
- Performs Buffett-style economic moat assessment
- Applies Howard Marks cycle positioning
- Produces a professional Markdown investment memo

## Final Output
Structured Markdown report with 5 mandatory sections:

1. Data Collection  
2. Graham Margin-of-Safety Valuation  
3. Buffett Moat Analysis  
4. Howard Marks Cycle Thinking  
5. Investment Memo  

(Easily convert to interactive HTML dashboards/charts using compatible visualization skills.)

## Recommended Usage
Prompt example:  
`Analyze TSLA using value-investing-analysis skill`

Install via ClawHub (recommended for OpenClaw agents):  
`clawhub install value-investing-analysis`

Or clone this repo and use directly.

## Core Frameworks
- Graham Margin-of-Safety Valuation
- Buffett Moat Analysis
- Howard Marks Cycle Thinking

## Repository Structure
- `SKILL.md` — main skill definition & execution flow
- `references/` — data sources, prompt templates, acceptance criteria
- `examples/` — sample visualization outputs (screenshots)

## Notes
- Real-time public data only (SEC, Yahoo Finance, CompaniesMarketCap etc.)
- Missing data explicitly marked — never fabricated
- Focused on tech/semiconductor/AI/cloud/internet stocks

Feedback, forks, or your own visualization examples welcome! 🚀
