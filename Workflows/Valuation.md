# Valuation Workflow

Business valuation methodologies for fundraising, M&A, or strategic planning.

## Valuation Context

### Key Questions First
1. **Purpose**: Fundraising? Sale? Internal? Estate?
2. **Stage**: Pre-revenue? Early revenue? Growth? Mature?
3. **Type**: SaaS? Service? Product? Asset-heavy?
4. **Control**: Minority stake? Majority? 100%?
5. **Liquidity**: Public? Private? Restricted?

### Valuation Hierarchy by Stage

| Stage | Primary Method | Secondary |
|-------|---------------|-----------|
| Pre-revenue | Venture Method, Scorecard | Comparables |
| Early Revenue | Revenue Multiples | Venture Method |
| Growth | Revenue/EBITDA Multiples | DCF |
| Mature | DCF, EBITDA Multiples | Asset-based |
| Distressed | Asset-based, Liquidation | DCF |

## Valuation Methods

### 1. Comparable Company Analysis (Comps)

**Process:**
1. Identify 5-10 comparable public companies
2. Calculate relevant multiples
3. Apply to target company metrics
4. Adjust for size, growth, risk differences

**Common Multiples:**
| Multiple | When to Use | Typical Range |
|----------|-------------|---------------|
| EV/Revenue | High growth, unprofitable | 1-20x |
| EV/EBITDA | Profitable, established | 5-15x |
| P/E | Mature, stable earnings | 10-25x |
| EV/ARR | SaaS businesses | 5-15x |
| Price/Book | Asset-heavy, financial | 1-3x |

**SaaS-Specific Multiples:**
- ARR Multiple: Enterprise value / Annual Recurring Revenue
- Rule of 40 Score: Revenue Growth % + EBITDA Margin %
- NTM Revenue Multiple: Based on next twelve months

### 2. Precedent Transactions

**Process:**
1. Find relevant M&A transactions (last 3-5 years)
2. Calculate transaction multiples
3. Adjust for market conditions, strategic premium
4. Apply to target

**Control Premium:**
- Typical range: 20-40% above trading price
- Higher for strategic buyers
- Lower in competitive auctions

**Sources:**
- PitchBook, Crunchbase (private deals)
- SEC filings (public deals)
- Press releases
- Industry reports

### 3. Discounted Cash Flow (DCF)

**Framework:**
```
Enterprise Value = Σ (FCF_t / (1+WACC)^t) + Terminal Value / (1+WACC)^n
```

**Steps:**
1. **Project Free Cash Flow** (5-10 years)
   - Revenue projections
   - Operating margins
   - Working capital changes
   - Capital expenditures

2. **Determine Discount Rate (WACC)**
   ```
   WACC = (E/V × Re) + (D/V × Rd × (1-T))

   Where:
   E = Market value of equity
   D = Market value of debt
   V = E + D
   Re = Cost of equity (CAPM)
   Rd = Cost of debt
   T = Tax rate
   ```

3. **Calculate Terminal Value**
   - Gordon Growth: FCF × (1+g) / (WACC - g)
   - Exit Multiple: Final year EBITDA × multiple

**Sensitivity Analysis:**
Create matrix varying WACC and terminal growth rate.

### 4. Venture Capital Method

**For Pre-Revenue/Early Stage:**
```
Post-Money Valuation = Exit Value / Target Return Multiple

Pre-Money = Post-Money - Investment Amount

Where:
Exit Value = Revenue at Exit × Expected Multiple
Target Return = Usually 10-30x for early stage
```

**Example:**
```
Year 5 Revenue Projection: £10M
Exit Multiple: 5x revenue
Exit Value: £50M
Required Return: 10x
Post-Money Valuation: £5M
Investment: £500K
Pre-Money: £4.5M
```

### 5. Scorecard Method (Angel/Seed)

Compare to average pre-money valuation in region, adjust for:

| Factor | Range | Weight |
|--------|-------|--------|
| Team | 0.5-1.5x | 30% |
| Market Size | 0.5-1.5x | 25% |
| Product | 0.5-1.5x | 15% |
| Competition | 0.5-1.5x | 10% |
| Partnerships | 0.5-1.5x | 10% |
| Need for Funding | 0.5-1.5x | 10% |

### 6. Asset-Based Valuation

**Book Value:**
Total Assets - Total Liabilities = Book Value

**Adjusted Book Value:**
- Mark assets to fair market value
- Add intangibles not on balance sheet
- Adjust for contingent liabilities

**Liquidation Value:**
- Forced sale discounts (typically 20-50%)
- Transaction costs
- Priority of claims

## Valuation Adjustments

### Discounts
| Discount Type | Typical Range | When Applied |
|---------------|---------------|--------------|
| Lack of Marketability | 15-35% | Private companies |
| Minority Interest | 15-25% | Non-controlling stakes |
| Key Person | 5-20% | Founder dependency |
| Customer Concentration | 5-15% | >20% single customer |

### Premiums
| Premium Type | Typical Range | When Applied |
|--------------|---------------|--------------|
| Control | 20-40% | Acquiring control |
| Strategic | 10-50% | Synergy value |
| Scarcity | Variable | Unique assets/IP |

## Output Template

```
💰 VALUATION ANALYSIS: [Company Name]
Date: [Analysis Date]
Purpose: [Fundraising/Sale/Internal]

═══════════════════════════════════════
EXECUTIVE SUMMARY
═══════════════════════════════════════
Valuation Range: £X.XM - £X.XM
Midpoint: £X.XM
Primary Method: [Method used]

═══════════════════════════════════════
COMPANY OVERVIEW
═══════════════════════════════════════
Revenue: £X.XM (Growth: X%)
EBITDA: £X.XM (Margin: X%)
Stage: [Stage]
Key Assets: [IP, customers, team, etc.]

═══════════════════════════════════════
COMPARABLE COMPANIES
═══════════════════════════════════════
| Company | Revenue | EV/Rev | EV/EBITDA |
|---------|---------|--------|-----------|
| Comp A  | £XXM    | X.Xx   | X.Xx      |
| Comp B  | £XXM    | X.Xx   | X.Xx      |
| Comp C  | £XXM    | X.Xx   | X.Xx      |
| Mean    |         | X.Xx   | X.Xx      |
| Median  |         | X.Xx   | X.Xx      |

Applied Multiple: X.Xx (adjusted for [factors])
Implied Value: £X.XM

═══════════════════════════════════════
DCF ANALYSIS
═══════════════════════════════════════
[5-year projection summary]
WACC: X.X%
Terminal Growth: X.X%
Enterprise Value: £X.XM

Sensitivity:
        | Growth 2% | 3% | 4% |
WACC 10%|   £X.XM   |    |    |
WACC 12%|           |    |    |
WACC 14%|           |    |    |

═══════════════════════════════════════
ADJUSTMENTS
═══════════════════════════════════════
Base Value: £X.XM
- Marketability Discount (X%): -£X.XM
- Customer Concentration (X%): -£X.XM
Adjusted Value: £X.XM

═══════════════════════════════════════
VALUATION SUMMARY
═══════════════════════════════════════
| Method | Value |
|--------|-------|
| Comps (Revenue) | £X.XM |
| Comps (EBITDA) | £X.XM |
| DCF | £X.XM |
| Precedent Transactions | £X.XM |
| **Weighted Average** | **£X.XM** |

═══════════════════════════════════════
KEY ASSUMPTIONS & RISKS
═══════════════════════════════════════
• [Assumption with sensitivity]
• [Risk with impact on value]

═══════════════════════════════════════
RECOMMENDATIONS
═══════════════════════════════════════
[Negotiation strategy, value drivers to highlight, etc.]
```

## Quality Checklist

- [ ] Multiple methods used for triangulation
- [ ] Comparables are truly comparable
- [ ] DCF assumptions clearly stated and reasonable
- [ ] Appropriate discounts/premiums applied
- [ ] Sensitivity analysis on key assumptions
- [ ] Range provided, not single point estimate
