## VI. Acceptance Criteria (If Not Met, the Task Is Incomplete)

### Final Locked Rules

- This skill must fully contain all core information from the original prompt. Generalization is allowed; reduction is not.
- In any run, if the final report is missing any core information point from the original master prompt, it is considered **incomplete**.
- Additional analytical modules may be added, but they may only enhance the report and may not replace original master requirements.
- If the user explicitly requests “follow the skill strictly,” “locked format,” or “must contain all requirements,” then this section must be treated as the highest-priority execution constraint.

### Cases That Do Not Meet This Skill’s Standard

If the report is missing any of the following, it fails to meet this skill’s standard:
- the six core financial indicators in the Data Collection section
- the basis explanation for the latest 4 quarters
- user-specified peer comparison targets
- Graham Number / DCF / margin of safety / buy-sell judgment
- sources of moat / switching costs / network effects / cost advantages / moat rating
- cycle stage / historical P/E-P/S positioning / capex-credit cycle signals / risk assessment
- key data table / three-framework comparison / overall judgment and risk / investor suitability
- implications for investors with no position / with an existing position
- explanation of missing data, sources already tried, and impact on the conclusion (if there are missing items)

If any of the above is missing, the report is considered **incomplete** and must return to the earlier data-collection or analysis stage to be supplemented.

---

## VII. Reusable Prompt Template

```text
Please conduct a complete value investing analysis on [company name / ticker]. Requirements:

## I. Data Collection
Obtain the company’s key financial data for the latest 4 quarters from public data sources:
- revenue, net income, gross margin, operating margin
- free cash flow, debt-to-asset ratio
- if applicable, also add: R&D expense ratio, capex, share dilution, segment revenue structure
- at the same time, obtain same-period data for [2-3 major competitors] for comparison

## II. Graham Margin-of-Safety Valuation
Use Benjamin Graham’s method for valuation:
- calculate the Graham Number
- use a DCF model to estimate intrinsic value under three scenarios (conservative / base / optimistic)
- compare with the current share price and calculate the margin of safety percentage
- give a Buy / Hold / Sell judgment from the Graham perspective

## III. Buffett Moat Analysis
Analyze the company’s competitive barriers from Warren Buffett’s perspective:
- brand moat / technical standard / platform mindshare
- switching costs: migration costs for customers, developers, enterprises, ecosystem partners
- network effects: developer ecosystem, user ecosystem, platform ecosystem, partner ecosystem
- cost advantage / scale advantage / data advantage / channel advantage / supply chain advantage
- moat rating: Wide / Narrow / None, with explanation

## IV. Howard Marks Cycle Thinking
Use Howard Marks’ cycle framework to judge the current position:
- what stage of the cycle the current industry is in (early / mid / overheated / downturn)
- market sentiment indicators: P/E / P/S / P/FCF compared with historical percentiles
- signals from the credit cycle, capex cycle, inventory cycle, and demand cycle
- risk assessment from the Marks perspective

## V. Investment Memo
Based on the three frameworks above, output a detailed, professional, and structured investment memo (in .md format):
- key data summary table
- conclusion comparison across the three frameworks
- overall judgment and key risks
- what type of investor it is suitable for

Notes:
- all data must come from real-time queries; do not use stale training-data values
- if a data point cannot be found, clearly mark it instead of fabricating it
- if the target company is a technology company, try to add time-series context, industry positioning, and competitive landscape; do not look only at static financial statements
```
