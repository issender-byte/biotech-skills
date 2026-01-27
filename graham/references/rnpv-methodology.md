# rNPV Methodology Reference

## Basic rNPV Formula

```
rNPV = Σ (Peak Sales × Margin × Multiple × PoS × Discount Factor) - Development Costs

Components:
- Peak Sales: From commercial-peak-sales skill
- Margin: 70-85% for biotech (gross to operating)
- Multiple: Revenue multiple at peak (3-5x typical)
- PoS: From clinical-trial-pos skill
- Discount Factor: 10-15% rate, years to peak
```

## Valuation Shortcuts

| Shortcut | Formula | Accuracy |
|----------|---------|----------|
| Peak multiple | Peak × 4x × PoS | ±30% |
| Royalty value | Peak × Royalty% × 10x × PoS | ±20% |
| $/Patient | Deal comps × eligible patients | ±40% |

## Valuation Floor Analysis

From ALMS exchange:

> "At $1.2bn cap and $850mm EV, and an MOA that is almost certain to hit stats, the skew seems up to me."

### Floor Components

| Floor Type | How to Calculate |
|------------|------------------|
| Cash | Net cash on balance sheet |
| Other pipeline | Sum of non-lead asset rNPVs |
| Platform | Value of technology/capabilities |
| Acquisition | Strategic premium (20-50% typical) |

### Implied PoS Back-Solve

```
Current EV = NPV(100% PoS) × Implied PoS
Implied PoS = Current EV / NPV(100%)

If your PoS > Implied PoS → Stock is cheap
If your PoS < Implied PoS → Stock is expensive
```

## Catalyst Asymmetry

### Expected Value Calculation

| Scenario | Probability | Move | EV Contribution |
|----------|-------------|------|-----------------|
| Beat | P1 | +X% | P1 × X |
| Meet | P2 | +Y% | P2 × Y |
| Miss | P3 | -Z% | P3 × (-Z) |
| **Weighted EV** | 100% | | Sum |

**For short to work:** Weighted EV must be negative.

### Common Mistake

"Drug is mediocre, short it"
- But if trial likely hits stats, stock may rally
- Even on underwhelming data
- Must calculate weighted EV, not just qualitative view

## Multi-Asset Valuation

| Asset | Indication | Phase | PoS | Peak | NPV | Prob-Adj |
|-------|------------|-------|-----|------|-----|----------|
| Lead | A | 3 | 50% | $2B | $5B | $2.5B |
| Second | B | 2 | 30% | $1B | $2B | $0.6B |
| Early | C | 1 | 15% | $0.5B | $1B | $0.15B |
| **Pipeline** | | | | | | **$3.25B** |

+ Cash $500M
- Debt $0
- Dev costs $(200M)
= **Fair Value $3.55B**
