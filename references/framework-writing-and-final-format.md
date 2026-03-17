## IV. How to Write the Analysis (Execute by Framework)

### A. Graham Margin-of-Safety Valuation: must write
- Graham Number
- DCF under 3 scenarios
- Comparison against the current price
- Margin of safety percentage
- A clear Graham-style conclusion (Buy / Hold / Sell)

### B. Buffett Moat Analysis: must write
- Sources of moat
- Switching costs
- Network effects / ecosystem effects (if applicable)
- Cost / scale / data / supply-chain advantages (adapt to company type)
- A moat rating of Wide / Narrow / None

#### General Rewrite Rules for Technology Companies


##### 1. Semiconductor / AI infrastructure companies
Focus on:
- Software ecosystem / developer ecosystem
- Architectural standards and compatibility
- Supply chain and access to advanced process technology
- Platform integration capability
- Customer migration cost

##### 2. SaaS / software companies
Focus on:
- Degree of workflow embedment
- Data accumulation
- User habits and organizational switching cost
- API / plugin / third-party integration ecosystem
- Brand mindshare and distribution channels

##### 3. Cloud computing / platform companies
Focus on:
- Scale advantages
- Network effects
- Developer ecosystem
- Degree of customer lock-in
- Cross-product upsell ability

##### 4. Consumer internet / platform companies
Focus on:
- User network effects
- Advertiser / merchant ecosystem
- Data advantages
- Traffic acquisition cost
- Brand and distribution entry-point control

##### 5. Hardware technology companies
Focus on:
- Brand premium
- Supply chain control
- Hardware-software integration
- Channel and after-sales system
- User ecosystem stickiness

When writing the output, express the sources of moat in the target company’s own business language instead of using generic template wording.

### C. Howard Marks Cycle Judgment: must write
- Industry cycle stage
- Market sentiment indicators (at minimum historical positioning of P/E / P/S)
- Key cycle signals among capex / credit / inventory / demand
- Risk assessment

#### General Checklist for Technology Companies

Common cycle signals for technology stocks include:
1. **Valuation cycle**: whether P/E / P/S / P/FCF is far from historical center
2. **Capex cycle**: whether cloud vendors, enterprise IT, and AI infrastructure are expanding or contracting
3. **Inventory cycle**: whether inventory is building up or being digested in semiconductors, hardware, servers, terminals, etc.
4. **Demand cycle**: whether downstream customers have pulled forward purchases
5. **Competitive cycle**: whether many new entrants are rushing in, creating future pricing pressure
6. **Narrative cycle**: whether the market has formed one-sided consensus around a story (for example “AI will grow at a high rate forever”)

When writing the output, do not stop at saying “the industry is overheated.” Try to answer:
- what exactly is hot
- whether earnings are hot or valuation is hot
- whether demand is truly strong or expectations have simply run ahead too fast
- which variable is most likely to reverse first

---

## V. Final Report Format (Mandatory Detailed Version)

### Overall Writing Requirements

- Clearly distinguish: **real-time fetched data**, **locally computed results**, and **qualitative analytical judgment**
- When data is missing, explicitly write “not found” or “current sources insufficient”; do not fabricate
- If the DCF is highly sensitive to assumptions, say so directly
- For technology stocks, do not perform only static value analysis; you must add the time dimension and industry validation
- Unless the user explicitly asks for a shorter version, the valuation section must by default present at the same time:
  - current share price
  - historical share-price context
  - current P/E / P/S / market cap
  - historical annual P/E / P/S comparison
  - capital-quality information such as SBC / dilution / repurchases
- When writing about capital quality, do not just list fields; answer:
  - whether the company is offsetting dilution through repurchases
  - whether SBC materially erodes per-share value
  - whether per-share metrics and aggregate profit metrics are improving consistently
- Do not pretend certainty in the conclusion. You may explicitly state:
  - how a strict value investor would judge it
  - how a growth investor would judge it
  - what a cycle investor would worry about

### The Final Markdown Report Must Include

The final investment memo output must be a **structured, detailed, and fully reasoned** version, and must fully cover the original master structure. At minimum, it must include:

1. **Executive Summary / Investment Conclusion**
2. **Key Data Summary Table**
3. **Data Sources and Definition Notes**
4. **Latest 4-Quarter Financials and Peer Comparison**
5. **Full display of the originally required items in the Data Collection section** (revenue, net income, gross margin, operating margin, free cash flow, debt-to-asset ratio, peer comparison)
6. **Graham Valuation (Graham Number, DCF under 3 scenarios, margin of safety, Buy/Hold/Sell judgment)**
7. **Buffett Moat Analysis**
8. **Howard Marks Cycle Judgment**
9. **Conclusion Comparison of the Three Frameworks** (the framework names must be written exactly here as: **Graham Margin-of-Safety Valuation / Buffett Moat Analysis / Howard Marks Cycle Thinking**)
10. **Overall Judgment and Key Risks**
11. **What Type of Investor It Is Suitable For**
12. **Missing Data Checklist, sources already tried, and impact on the conclusion** (if any)
13. **Actionable implications for investors with no position / with an existing position**

### Final Markdown Result Block Acceptance (Mandatory)

In addition to the full master structure, the **final `.md` file delivered to the user must also clearly contain the following 4 block titles or extremely close equivalents in the result section, and the content may not be missing:**

- **Key Data Summary Table**
- **Conclusion Comparison of the Three Frameworks (Graham Margin-of-Safety Valuation, Buffett Moat Analysis, Howard Marks Cycle Thinking)**
- **Overall Judgment and Key Risks**
- **What Type of Investor It Is Suitable For**

These 4 blocks are hard constraints for the final result page. Even if related analysis has already appeared earlier, these result blocks must still summarize it again clearly so the user can inspect the conclusion directly.

### Action Recommendation Acceptance (New Mandatory Rule)

In the final `.md` result, **an explicit action recommendation must be given**. Do not make the user infer it. Requirements:

- At least one primary action recommendation must be given: **Buy / Hold / Watch / Reduce / Sell** (or a semantically equivalent expression)
- Ideally distinguish at the same time: **what investors with no position should do** and **what investors with an existing position should do**
- Do not output only analytical conclusions without translating them into action
- If the conclusion depends on scenarios (for example conservative, base, optimistic), it must still ultimately be summarized into one clear recommendation rather than stopping at conditional analysis

If an explicit action recommendation is missing, the report is considered **incomplete**.

### Recommended Final Markdown Skeleton (Use by Default)

```markdown
# [Company Name / Ticker] Value Investing Analysis Memo

## Executive Summary / Investment Conclusion

## I. Data Collection
### 1. Data Sources and Definition Notes
### 2. Key Financial Data for the Latest 4 Quarters
### 3. Peer Comparison (2-3 companies; if the user specified names, use those named targets)

## II. Graham Margin-of-Safety Valuation
### 1. Graham Number
### 2. DCF (Conservative / Base / Optimistic)
### 3. Comparison Against Current Share Price and Margin of Safety
### 4. Graham-Style Conclusion (Buy / Hold / Sell)

## III. Buffett Moat Analysis
### 1. Brand / Technology / Platform Moat
### 2. Switching Costs
### 3. Network Effects / Ecosystem Lock-in
### 4. Cost / Scale / Data / Supply Chain Advantages
### 5. Moat Rating (Wide / Narrow / None)

## IV. Howard Marks Cycle Thinking
### 1. Cycle Stage Judgment
### 2. Market Sentiment Indicators (Historical Position of P/E / P/S / P/FCF)
### 3. Credit / Capex / Inventory / Demand Cycle Signals
### 4. Marks-Style Risk Assessment

## V. Investment Memo
### 1. Key Data Summary Table
### 2. Conclusion Comparison of the Three Frameworks
### 3. Overall Judgment and Key Risks
### 4. What Type of Investor It Is Suitable For
### 5. Implications for Investors With No Position / With an Existing Position
### 6. Missing Data Checklist, Sources Already Tried, and Impact on the Conclusion (if any)
```

Unless the user explicitly requests a shorter version or a different template, organize the final output according to the skeleton above by default. You may add subsections, but you may not delete any main section or hard-required subsection.

### Professional Standard

The final markdown must not stay at the shallow level of “the company is good, but the valuation is not cheap.” It must try to answer:
- what expectations are currently implied by the share price
- which data supports the bull case
- which data supports the bear case or risk case
- what it means separately for investors with no position and investors with an existing position

### Default Conclusion Style

Write the conclusion across these three layers:
1. **Company quality**: is it an excellent company?
2. **Valuation position**: is it expensive or not?
3. **Investor fit**: who is suitable to hold it, and who is not?

For example:
- “This is a high-quality company, but not a classically cheap stock.”
- “Fundamentals are strong, but valuation already reflects a large amount of optimism.”
- “Suitable for long-term growth investors, not suitable for pure value investors who require a high margin of safety.”

---
