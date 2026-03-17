---
name: value-investing-analysis
description: Perform value investing analysis on publicly listed technology companies: use real-time public data to collect the latest 4 quarters of financials, compare peers, run Graham margin-of-safety valuation, Buffett moat analysis, and Howard Marks cycle positioning, then output a structured investment memo. Use for requests such as “value investing analysis,” “valuation analysis,” “margin of safety,” “DCF,” “moat,” “cycle position,” and “investment memo,” especially for technology companies such as semiconductors, software, cloud computing, internet platforms, and AI infrastructure.
---

# Value Investing Analysis

When conducting value investing analysis on a technology company, the goal is not merely to answer “is this a good company,” but to answer all of the following at the same time:
1. What have this company’s fundamentals actually looked like over the most recent 4 quarters?
2. Is the current valuation implied by the share price reasonable?
3. Does it have durable competitive advantages?
4. What stage of the cycle is its industry and market sentiment currently in?
5. What type of investor is or is not suitable to hold it?

---

## I. Master Structure (Mandatory, Must Not Be Reduced)

The core of this skill is not a “suggested framework,” but a **mandatory master structure**. It may be generalized into broader terms, and deeper analysis may be added, but **nothing may be removed, omitted, or weakened**.

### Fixed 5-Part Output

By default, and **mandatorily**, output the analysis in the following 5 sections. No section may be omitted, renamed into vague wording, or reduced to a passing sentence:

1. **I. Data Collection**
2. **II. Graham Margin-of-Safety Valuation**
3. **III. Buffett Moat Analysis**
4. **IV. Howard Marks Cycle Thinking**
5. **V. Investment Memo**

If the user does not specify a format, this structure must still be used.

### Title Lock Rule (Mandatory)

The final report must use the section titles above by default, in the exact order shown. Reordering is not allowed. If extra sections such as “Executive Summary,” “Data Sources,” or “Missing Data Checklist” are added, they may only appear as subsections under these main sections and may not replace any main section.

### Missing Any Required Item Means Incomplete (Mandatory)

If the final output is missing any main section, any hard-required subsection, any specified comparison target, or any required judgment sentence, then the analysis is considered **incomplete** and must be supplemented. It is not acceptable to present it as a formal delivery by saying “here is a preliminary version first” or “see if this is enough.” Unless the user explicitly asks for a draft, the default target is a complete formal version.

### Original Master Requirements (Locked Item by Item)


#### 1. The Data Collection section must include
- Key financial data for the latest 4 quarters
- Revenue
- Net income
- Gross margin
- Operating margin
- Free cash flow
- Debt-to-asset ratio
- Data for 2-3 major competitors for the same period as comparison
- For each metric, clearly state the basis used (TTM / single quarter / latest fiscal quarter end / latest four-quarter aggregate)
- For each real-time value, label the source or source group (for example SEC / Tencent Quotes / CompaniesMarketCap / StockAnalysis / Stooq)

#### 2. The Graham Margin-of-Safety Valuation section must include
- Graham Number
- DCF under 3 scenarios (conservative / base / optimistic)
- Comparison against the current share price
- Margin of safety percentage
- A clear Buy / Hold / Sell judgment
- Clearly separate the “Graham Number result” from the “DCF result”; do not merge them into a single value
- If the Graham Number has limited applicability to high-growth technology companies, **calculate it first, then explain the limitations**; do not skip it on the grounds that “it is not very meaningful”
- The DCF must explicitly list the key assumptions: starting cash flow definition, growth rates, discount rate, and terminal growth rate

#### 3. The Buffett Moat Analysis section must include
- Brand moat
- Switching costs
- Network effects / ecosystem lock-in
- Cost advantage / scale advantage / supply chain advantage (adapt to company type)
- A moat rating of Wide / Narrow / None
- The rating must include a clear conclusion sentence; vague wording such as “the moat is fairly deep” or “there are some barriers” is not sufficient

#### 4. The Howard Marks Cycle Thinking section must include
- What stage the current industry is in (early / mid / overheated / downturn)
- Market sentiment indicators: at minimum P/E and P/S versus historical percentiles
- Credit-cycle and capex-cycle signals (if the tech industry is better explained through inventory / demand / capex / narrative cycles, that must also be stated)
- Risk assessment from a Marks-style perspective
- It must answer whether what is hot is earnings, valuation, or narrative
- It must clearly state which cycle variable is most likely to reverse first, rather than only giving generic risk warnings

#### 5. The Investment Memo section must include
- A key data summary table
- A conclusion comparison across the three frameworks (**must be written explicitly as: Graham Margin-of-Safety Valuation, Buffett Moat Analysis, Howard Marks Cycle Thinking**; do not rewrite these into generic framework names)
- An overall judgment and key risks
- What type of investor it is suitable for
- What it means for investors with no position
- What it means for investors with an existing position
- **A clear action recommendation**: there must be an actionable conclusion, at minimum explicitly landing on one of the following or an equivalent expression — **Buy / Hold / Watch / Reduce / Sell**. It is not acceptable to say only “the company is good but the valuation is not cheap” without an action recommendation
- A clear distinction between: real-time queried data / locally computed results / qualitative analytical judgment

#### 5.1 Hard Output Structure for the Final Markdown Result (New Locked Rule)
Regardless of how detailed the intermediate analysis is, the **final delivered `.md` report must explicitly contain the following 4 result blocks, and none may be omitted, weakened, or folded vaguely into other paragraphs:**

1. **Key Data Summary Table**
2. **Conclusion Comparison of the Three Frameworks (Graham Margin-of-Safety Valuation, Buffett Moat Analysis, Howard Marks Cycle Thinking)**
3. **Overall Judgment and Key Risks**
4. **What Type of Investor It Is Suitable For**

If the final `.md` does not fully contain the 4 result blocks above, the delivery is considered **incomplete** and must be rewritten before it can be submitted as the formal result.

#### 6. Notes must include
- All data must come from real-time queries
- Do not directly use stale values from training data as if they were real-time data
- If a data point cannot be found, explicitly mark that fact; do not fabricate it

### Enforcement Principles

- This is not an “optional suggestion”; it is a **mandatory analysis architecture**.
- You may only enhance this architecture, never reduce information or omit any core requirement.
- You may only add value on top, never leave out required information.
- If some data point has not yet been obtained, the default action is not to stop the analysis, but to:
  1. Continue trying the sources listed in the skill
  2. Switch to other feasible public sources
  3. Try different field names / disclosure definitions / page paths
  4. Only after confirming it is truly unavailable may it be marked as “not found”
- **Do not output a half-finished conclusion early just because scraping is troublesome, pages are blocked, or field names are difficult to locate.**
- Only after “multiple rounds of exhaustive attempts across public sources” may you acknowledge that some data is temporarily unavailable.

---

---

## Reference Map (Added Navigation Only)

The content moved below is **not deleted**; it is relocated verbatim into `references/` files so that the skill keeps 100% of its information while making the main `SKILL.md` easier to scan.

Read the following files as needed, in addition to the mandatory master structure above:

1. **`references/data-requirements-and-sources.md`**
   - Read when you need the mandatory data checklist, source mapping, source-specific notes, gap-handling rules, and execution flow.
   - This file contains the original text of:
     - `## II. Data Requirements and Source Mapping (Mandatory Data Collection Checklist)`
     - `## III. Execution Flow (Mandatory Working Order)`

2. **`references/framework-writing-and-final-format.md`**
   - Read when you need the framework-specific writing rules and the full final markdown report format.
   - This file contains the original text of:
     - `## IV. How to Write the Analysis (Execute by Framework)`
     - `## V. Final Report Format (Mandatory Detailed Version)`

3. **`references/acceptance-and-prompt-template.md`**
   - Read when you need the acceptance criteria and the reusable prompt template.
   - This file contains the original text of:
     - `## VI. Acceptance Criteria (If Not Met, the Task Is Incomplete)`
     - `## VII. Reusable Prompt Template`
