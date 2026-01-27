# Position Sizing Reference

Framework for determining position sizes based on conviction, edge, and portfolio context.

---

## Overview

Position sizing integrates:
1. **Conviction** - How confident are you?
2. **Edge** - How big is the gap between your view and market's?
3. **Portfolio context** - Correlations, exposures, limits

---

## Conviction-Based Sizing

### Base Size by Conviction

| Conviction Level | Base Size | Description |
|------------------|-----------|-------------|
| **Very High** | 150-250 bps | Clear edge, high-quality analysis done |
| **High** | 100-150 bps | Good edge, solid analysis |
| **Medium** | 50-100 bps | Some edge, thesis developing |
| **Low/Starter** | 25-50 bps | Monitoring, building thesis |

### Conviction Criteria

| Very High Conviction Requires |
|------------------------------|
| ✓ Primary clinical driver analyzed (reverend-bayes) |
| ✓ Commercial model built (john-snow) |
| ✓ Valuation framework applied (graham) |
| ✓ Positioning/sentiment checked (keynes) |
| ✓ Clear catalyst path |
| ✓ Defined exit criteria |

---

## Edge-Based Sizing

### The Edge Formula

```
Edge = Your PoS - Market Implied PoS
```

| Your PoS | Market PoS | Edge | Interpretation |
|----------|------------|------|----------------|
| 70% | 40% | +30pp | Large edge, size up |
| 60% | 50% | +10pp | Moderate edge, standard size |
| 55% | 50% | +5pp | Small edge, smaller size |
| 50% | 50% | 0pp | No edge, don't trade |

### Edge-Based Size Adjustments

| Edge | Size Adjustment |
|------|-----------------|
| >30pp | +50% to base size |
| 20-30pp | +25% |
| 10-20pp | No adjustment |
| 5-10pp | -25% |
| <5pp | -50% or skip |

---

## Kelly Criterion (Simplified)

### Formula
```
Optimal Size = Edge / Odds
            = (p × b - q) / b

Where:
- p = probability of winning
- q = probability of losing (1 - p)
- b = win/loss ratio (upside / downside)
```

### Biotech Example
```
- Your PoS: 60%
- Implied PoS: 40%
- Edge: 20% (60% - 40%)
- Upside: +50%
- Downside: -30%
- Odds: 1.67 (50/30)

Kelly = (0.6 × 1.67 - 0.4) / 1.67
     = (1.0 - 0.4) / 1.67
     = 36%
```

### Fractional Kelly
- Full Kelly is too aggressive for biotech
- Use 25-50% of Kelly (quarter to half Kelly)
- Example: 36% Kelly → 9-18% actual position

---

## Portfolio Context Adjustments

### Adjustment Checklist

Start with base size from conviction, then adjust:

| Factor | Check | Adjustment |
|--------|-------|------------|
| Gross headroom | Would exceed limit? | Reduce to fit |
| TA concentration | Would exceed 30%? | Reduce |
| Correlation | High with existing? | Reduce 20-30% |
| Catalyst clustering | Multiple events same window? | Reduce |
| Liquidity | >10% ADV daily? | Reduce to fit |

### Adjustment Documentation

```
SIZING DECISION:
│ Input                     │ Adjustment │ Running Size │
│ Keynes base recommendation│ -          │ 125 bps      │
│ Gross exposure headroom   │ OK         │ 125 bps      │
│ TA concentration          │ -15 bps    │ 110 bps      │
│ Correlation to book       │ -10 bps    │ 100 bps      │
│ Catalyst clustering       │ OK         │ 100 bps      │
│ Liquidity constraint      │ OK         │ 100 bps      │
│ FINAL SIZE                │            │ 100 bps      │
```

---

## Analysis-Constrained Sizing

### The Principle

**Don't full-size until the primary driver is analyzed.**

| Analysis Status | Max Size |
|-----------------|----------|
| Clinical driver not analyzed | 25% of target |
| Commercial model not built | 50% of target |
| No valuation framework | 75% of target |
| Full analysis complete | 100% of target |

### NUVB Example

If NUVL competitor data is the primary driver:
- Until NUVL analyzed: 25-50 bps max
- After NUVL analyzed: full conviction size

**Rationale:** The primary uncertainty is NUVL. Sizing before understanding NUVL is speculating, not investing.

---

## Scaling Into/Out of Positions

### Scale-In Rules

| Situation | Approach |
|-----------|----------|
| High conviction, good entry | Full position immediately |
| High conviction, uncertain entry | 50% now, 50% on pullback |
| Developing thesis | 25% starter, add on confirmation |
| Pre-catalyst accumulation | Build over 2-4 weeks |

### Scale-Out Rules

| Situation | Approach |
|-----------|----------|
| Hit price target | Trim 50%, hold remainder |
| Thesis playing out | Hold or add on pullbacks |
| Data positive but complex | Trim 25-50%, reassess |
| Data negative | Exit entirely |

---

## Risk-Based Sizing

### Volatility-Adjusted Size

Higher volatility = smaller position for same risk contribution.

```
Size = Target Risk Contribution / Position Volatility
```

| Stock Volatility | Size Adjustment |
|------------------|-----------------|
| <30% annualized | +25% |
| 30-50% | No adjustment |
| 50-70% | -20% |
| >70% | -40% |

### Max Loss Framework

Define max acceptable loss, then back-solve size:

```
Max Size = Max Acceptable Loss / Expected Downside

Example:
- Max loss: 50 bps of portfolio
- Expected downside: -40%
- Max size: 50 / 0.4 = 125 bps
```

---

## Position Sizing Checklist

```
POSITION SIZING CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━━━━

CONVICTION:
□ Analysis completeness: Clinical/Commercial/Valuation
□ Base conviction level: Very High/High/Medium/Low
□ Base size: ___ bps

EDGE:
□ Your PoS: ___%
□ Market implied PoS: ___%
□ Edge: ___ pp
□ Edge adjustment: ___

PORTFOLIO CONTEXT:
□ Gross exposure impact: OK / Reduce
□ TA concentration: OK / Reduce
□ Correlation to existing: Low/Medium/High → ___
□ Catalyst clustering: OK / Reduce
□ Liquidity: OK / Reduce

FINAL SIZE: ___ bps
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
