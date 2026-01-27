# Correlation Clusters Reference

Framework for understanding and managing correlations between positions.

---

## Overview

Understanding correlations between positions is essential for portfolio construction. Two positions can be diversifying, redundant, or hedging.

---

## Correlation Drivers in Biotech

### Primary Factors

| Factor | Correlation Driver | Strength |
|--------|-------------------|----------|
| **Same target** | Mechanism validation/failure | Very high |
| **Same indication** | TA sentiment, M&A waves | High |
| **Same phase** | Risk-on/off flows | Medium-high |
| **Same market cap** | Factor flows | Medium |
| **Same mechanism class** | Class validation | High |

### Correlation Interpretation

| Correlation | Interpretation |
|-------------|----------------|
| >0.8 | Essentially same position |
| 0.6-0.8 | Highly correlated (same bet) |
| 0.4-0.6 | Moderately correlated (related) |
| 0.2-0.4 | Loosely correlated |
| <0.2 | Effectively uncorrelated |

---

## Common Correlation Clusters

### Same Target
- Two IL-13 antibodies
- Multiple KRAS inhibitors
- Several GLP-1 analogs

**Implication:** Data on one affects all; effectively single position.

### Same Indication (Different Mechanism)
- Multiple AD therapies (anti-amyloid, tau, symptom management)
- Multiple CAR-T in same cancer

**Implication:** TA news flow correlated, but mechanism data uncorrelated.

### Same Phase
- Multiple Phase 3 stocks
- Multiple preclinical platforms

**Implication:** Risk-on/off flows affect similarly.

### Competitor Set
- Long best-in-class, short inferior competitor
- Long market leader, short challenger

**Implication:** May be hedging or doubling down depending on direction.

---

## Pair Trade Dynamics

### When Long and Short in Same TA

| Scenario | Long | Short | Net Effect |
|----------|------|-------|------------|
| TA rallies | Gains | Loses | Partially hedged |
| TA sells off | Loses | Gains | Partially hedged |
| Long wins, short loses | Gains | Gains | Best case |
| Long loses, short wins | Loses | Loses | Worst case |

### Key Questions
1. Is this a **spread** (betting on relative performance)?
2. Or **directional** (net long/short the TA)?
3. What's the **correlation** between the two names?

---

## Pair Trade Effectiveness

| Correlation | Hedge Effectiveness | Risk Level |
|-------------|---------------------|------------|
| >0.8 | Excellent hedge | Low |
| 0.6-0.8 | Good hedge | Medium |
| 0.4-0.6 | Partial hedge | Medium-high |
| <0.4 | Not a true pair | High |

---

## Effective Exposure Calculation

### Why It Matters
Two 100 bps positions with 0.8 correlation ≈ 180 bps effective exposure, not 200 bps.

### Formula
```
Effective Gross = Σ √(Σ(wi × wj × ρij))

Simplified:
- Uncorrelated positions: Add absolute values
- Perfectly correlated: Add signed values
- Partially correlated: Between the two
```

### Practical Approach
| Positions | Correlation | Effective Exposure |
|-----------|-------------|-------------------|
| 100 bps + 100 bps | 1.0 | 200 bps (double count) |
| 100 bps + 100 bps | 0.0 | ~141 bps (sqrt rule) |
| 100 bps + 100 bps | 0.5 | ~170 bps |
| 100 bps L, 100 bps S | 0.8 | ~60 bps net (hedge) |

---

## Correlation Risk Management

### When Correlations Spike

During market stress:
- Correlations increase (everything sells together)
- Effective gross higher than nominal
- Diversification benefit decreases

**Action:**
- Reduce gross during high correlation regimes
- Focus on truly uncorrelated positions
- Increase cash buffer

### Correlation Monitoring

| Metric | Normal | Warning | Action |
|--------|--------|---------|--------|
| Avg pairwise correlation | <0.4 | 0.4-0.6 | Monitor |
| Top 5 positions correlation | <0.5 | 0.5-0.7 | Reduce |
| TA concentration effect | <1.3x | 1.3-1.5x | Trim |

---

## True vs False Diversifiers

### True Diversifiers

| Position Type | Why Diversifying |
|---------------|------------------|
| Different TA | Uncorrelated news flow |
| Different phase | Different risk profile |
| Different geography | Regulatory independence |
| Platform vs product | Different value drivers |

### False Diversifiers

| Perceived Diversification | Reality |
|---------------------------|---------|
| "5 AD names" | Single TA bet |
| "Mix of Phase 2 and 3" | Still correlated on sentiment |
| "Long and short same TA" | May be same bet if highly correlated |
| "Different companies, same target" | Essentially single bet |

---

## Correlation Checklist

```
CORRELATION ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━

FOR NEW POSITION:
□ What existing positions share same target?
□ What existing positions in same TA?
□ What's the correlation estimate?
□ Is this diversifying, redundant, or hedging?
□ What's the effective exposure after adding?

FOR PORTFOLIO:
□ Top 5 positions correlation matrix
□ TA-level correlation clusters identified
□ Effective gross vs nominal gross
□ True diversification vs false diversification
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
