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


---

## Pattern 4: Position Sizing vs Catalyst Proximity

### Core Framework (from DYN/NUVB analysis)

**Start smaller before near-term catalysts, add after resolution.**

The intuition: Binary events create asymmetric information. Before the event, you're betting on outcome. After the event, you're investing with known data.

### Sizing by Catalyst Status

| Catalyst Status | Recommended Size | Rationale |
|-----------------|------------------|-----------|
| **<1 month to catalyst** | 25-50% of target | High uncertainty, binary risk |
| **1-3 months to catalyst** | 50-75% of target | Building conviction, monitoring |
| **Catalyst resolved (positive)** | 100%+ of target | Known data, can analyze |
| **Catalyst resolved (negative)** | Exit or reassess | Thesis invalidation |

### Add Triggers

| Type | Description | Example |
|------|-------------|---------|
| **Catalyst trigger** | Add after event resolves favorably | NUVL data positive → add NUVB short |
| **Price trigger** | Add on technical level breach | Stock enters teens → add |
| **Combined** | Both conditions must be met | Data positive AND price hits target |

### DYN Worked Example

**Context:** NUVB short thesis depends on NUVL competitor success. SRPT/PEPG data expected.

**Sizing approach:**
- Current size: 150 bps (75% of 200 bps target)
- Rationale: Competitor data unresolved
- Add trigger: SRPT/PEPG positive + NUVB enters teens
- Target after resolution: 200-250 bps

```
Timeline:
Now ─────────────────────► SRPT/PEPG data ──────────► 
     75% size (150bps)        Resolution point
                                    │
                                    ▼
                          [If positive + teens]
                                    │
                                    ▼
                          Full size (200+ bps)
```

### Common Mistakes

| Mistake | Problem | Correct Approach |
|---------|---------|------------------|
| Full-sizing before catalyst | Binary risk not compensated | Scale to 50-75% pre-event |
| Not adding after positive data | Missed opportunity | Have explicit add triggers |
| Waiting for "perfect" entry | Never reach target size | Set realistic triggers |
| Ignoring catalyst clustering | Multiple binaries compound | Reduce size if multiple events |

### Integration with Competitor-Contingent Analysis

For competitor-dependent theses (NUVB depends on NUVL):

1. **Pre-competitor data:** 50-75% of target
2. **Competitor data positive:** Add to full size on your stock's price weakness
3. **Competitor data negative:** Reassess thesis entirely

This framework prevents thesis creep. You define ahead of time:
- What competitor outcome you need
- What price level triggers adding
- What invalidates the thesis

### Checklist

```
CATALYST PROXIMITY SIZING
━━━━━━━━━━━━━━━━━━━━━━━━━

PRE-CATALYST:
□ Catalyst date: ___________
□ Days to catalyst: ___
□ Current size: ___ bps
□ Target size (if positive): ___ bps
□ Sizing discount applied: ___% 

ADD TRIGGERS:
□ Catalyst outcome required: ___________
□ Price level for add: ___
□ Combined or either: ___

EXIT TRIGGERS:
□ Catalyst outcome that invalidates: ___________
□ Price level for exit: ___

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
