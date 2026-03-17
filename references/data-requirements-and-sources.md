## II. Data Requirements and Source Mapping (Mandatory Data Collection Checklist)

For technology companies, the following data is not “optional enrichment”; it is **required by default and must be analyzed**. Unless it is confirmed unavailable after multiple attempts across sources, it may not be skipped.

### Must Collect and Analyze
1. **Core financial data for the latest 4 quarters** (revenue, net income, gross profit, operating income, operating cash flow, capital expenditures, and core balance-sheet items)
2. **Gross margin**
3. **Operating margin**
4. **Free cash flow**
5. **Debt-to-asset ratio**
6. **Current share price**
7. **Current P/E / P/S / market capitalization**
8. **Historical annual P/E / P/S series**
9. **Same-period data for at least 2-3 comparable companies**
10. **Share-price time series** (at least 1 year, target 3-5 years by default)
11. **Segment revenue structure** (for example data center, cloud, software subscription, advertising, terminals, gaming, etc.)
12. **Capex / industry demand / major customer capex signals**
13. **Competitive substitution data** (in-house chips, open-source substitutes, platform substitutes, channel substitutes, etc.)
14. **SBC (stock-based compensation)**
15. **Diluted share count / diluted shares outstanding**
16. **Share repurchase-related fields and remaining authorization**
17. **ROIC / ROE / P/FCF / EV/Sales / EV/EBIT**

### Validated, Reusable Data Sources

The following sources have already been proven usable in the current environment and should be preferred.

#### Core Data Already Verified as Obtainable

In the current environment, the following data has already been verified as **directly retrievable or directly constructible**. Therefore, when performing value investing analysis on technology stocks, it should by default be included in the working papers:

- Historical share prices
- Current share price
- Core financial data for the latest 4 quarters
- Current P/E / P/S / market capitalization
- Historical annual P/E / P/S
- SBC (stock-based compensation)
- Diluted share count / diluted shares outstanding
- Entry points for share repurchase-related fields

For top-1% investment banking / buy-side style analysis, the significance of this data set is not just “looking at a few more metrics,” but lifting the analysis from **static valuation** to simultaneous checks of **per-share value, capital allocation quality, and market pricing position**.

#### 1. SEC Company Facts (Primary financial source for U.S. equities)

**URL pattern:**
```text
https://data.sec.gov/api/xbrl/companyfacts/CIK<10-digit-CIK>.json
```

**Primary uses:**
- Revenue for the latest 4 quarters
- Gross profit / operating income / net income
- Operating cash flow
- Capital expenditures
- Total assets / total liabilities / shareholders’ equity
- Shares outstanding
- SBC (stock-based compensation)
- Diluted share count / diluted shares outstanding
- Entry points for share repurchase-related fields

**Suitable derived metrics:**
- Gross margin
- Operating margin
- Free cash flow (FCF = CFO - Capex)
- Debt-to-asset ratio (Liabilities / Assets)
- EPS
- BVPS
- Graham Number

**Notes:**
- A descriptive `User-Agent` must be used
- XBRL concept naming differs by company; do not assume fields are uniform
- The common problem is usually not “no data,” but “different field names”
- SEC data often mixes single-quarter values and cumulative values; discrete quarters must be separated before comparison

**Example:**
```bash
curl -s -H 'User-Agent: YourName your@email.com' \
```

#### 2. Tencent Quote API (Current share price / real-time quote)

**URL pattern:**
```text
```

**Already verified as obtainable:**
- Current share price
- Real-time percentage change
- Some real-time market cap and quote-book fields

**Primary uses:**
- Use the current share price as the anchor for all valuation comparisons
- Compare Graham Number, DCF, current P/E / P/S against the market price
- Compare current peer pricing levels

**Notes:**
- The response is in GBK encoding and must be converted to UTF-8 first
- Suitable for obtaining the “current price,” but not long historical financials

**Example:**
```bash
```

#### 3. CompaniesMarketCap (Valuation multiples and historical annual series)

**Site:**
```text
https://companiesmarketcap.com
```

**Common pages:**
```text
https://companiesmarketcap.com/<slug>/pe-ratio/
https://companiesmarketcap.com/<slug>/ps-ratio/
https://companiesmarketcap.com/<slug>/marketcap/
```

**Already verified as obtainable:**
- Current TTM P/E
- Current TTM P/S
- Current market capitalization
- Historical annual P/E series
- Historical annual P/S series

**Primary uses:**
- Assess the current valuation level
- Estimate historical relative position and rough percentile
- Judge whether the market has already priced future growth aggressively
- Provide evidence of “valuation heat / sentiment temperature” for the Howard Marks framework

**Positioning:**
- Suitable for supplementary judgment on valuation heat, historical percentile, and market sentiment
- Not equivalent to institutional databases such as Bloomberg or FactSet

#### 4. Stooq (Daily historical share prices)

**URL pattern:**
```text
https://stooq.com/q/d/l/?s=<ticker>.us&i=d
```

**Already verified as obtainable:**

**Primary uses:**
- 1-year / 3-year / 5-year price range and drawdown analysis
- Judge where the current share price sits within the long-term trend
- Use together with valuation series to identify whether the situation is “high fundamental growth + overheated valuation” or “repriced after earnings slowdown”
- Support investment-banking / buy-side style price context instead of reporting only a spot price

**Notes:**
- Confirm whether stock splits have already been adjusted before use
- For rigorous long-term return comparison, check the handling of corporate actions and dividends

#### 5. StockAnalysis (Supplementary valuation / statistics entry point)

**Site:**
```text
https://stockanalysis.com/stocks/<ticker>/financials/ratios/
https://stockanalysis.com/stocks/<ticker>/statistics/
```

**Already verified as accessible:**
- ratios page
- statistics page

**Primary uses:**
- Supplement additional valuation and statistical definitions
- Provide supporting entry points for P/FCF, capital structure, per-share metrics, and cross-sectional valuation comparison

**Positioning:**
- Suitable as a supplement to CompaniesMarketCap, not a replacement for SEC as the primary financial source

#### 6. Sources Not Recommended as the Main Workflow in the Current Environment

The following sources are not entirely unusable, but are not stable enough in the current environment and are not recommended as the main chain:

- **Yahoo Finance / yfinance**: TLS issues occur in the current environment
- **Macrotrends**: anti-scraping or blocking leads to unstable retrieval

### Gap Handling and Re-Collection Rules (Mandatory)

- Each item above must, by default, enter the final report; it may not be omitted just because it is troublesome.
- If an item is not obtained on the first attempt, you must continue trying:
  - switch source
  - switch company disclosure entry point
  - switch field concept
  - switch page path
  - switch to a proxy metric for comparable analysis
- Only after multiple rounds of attempts may the report state:
  - which item was not obtained
  - which sources were tried
  - why it is still unavailable at present
  - how that affects the reliability of the conclusion
- **During the analysis phase, if any conclusion is found to lack necessary data support, you must return to the data-collection phase and continue searching; do not finalize the report with insufficient evidence.**
- For the 17 hard-required data items, all of them must be found by default. Unless they are confirmed unavailable after exhaustive attempts across public sources, the analysis may not end.
- For the 17 hard-required data items, all of them must be explicitly used in the final analysis by default. Do not merely collect them without explaining them or incorporating them into the conclusion chain.

### Optional Enhancements (Nice to Have)
18. **Inventory cycles, price wars, ASP changes**
19. **Policy / geopolitical / regulatory risk**

Note: Items 1-17 are **hard requirements**; only items 18-19 are enhancement items. Do not make the enhancements fancy while missing hard requirements.

---

## III. Execution Flow (Mandatory Working Order)

1. Confirm the target company and comparable companies
2. Pull the latest 4 quarters of core financials
3. Compute derived metrics (gross margin, operating margin, FCF, debt-to-asset ratio, EPS, BVPS)
4. Pull the current share price
5. Pull the historical share-price series (at least 1 year, ideally 3-5 years)
6. Pull current P/E / P/S / market cap and historical annual P/E / P/S series
7. Supplement capital-quality data (SBC, diluted share count / diluted shares outstanding, share repurchase-related fields)
8. Supplement segment revenue structure, industry demand / major customer capex, and competitive substitution data
9. Perform the Graham Number and DCF
10. Write the moat analysis in light of the business model
11. Write the cycle assessment in light of industry context and valuation position
12. Check whether all 17 hard-required data items have entered the report
13. Only after confirming all hard-required items are covered may the work be summarized into a Markdown investment memo

### Mandatory Checkpoints

Before entering the final report, confirm item by item:
- Have all hard-required data items been obtained?
- Has the obtained data been analyzed, rather than merely dumped into the file?
- Has the impact of missing data on the conclusion been explained?
- Are there still public sources worth trying further?

If the answer to any of the above is negative, the default action is to continue the research rather than wrapping up early.

---
