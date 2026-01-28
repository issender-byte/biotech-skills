# Positioning Analysis

Framework for assessing ownership, short interest, and crowding to inform position sizing.

---

## Overview

Positioning analysis answers: **Who owns this stock, and how crowded is the trade?**

Key components:
1. **Institutional ownership** — Who holds it, quality of holders
2. **Short interest** — How many betting against
3. **Crowding assessment** — Is the trade too popular?
4. **Flow analysis** — Who's buying/selling recently

---

## Institutional Ownership Analysis

### Owner Type Classification

| Owner Type | What It Tells You |
|------------|-------------------|
| **Dedicated biotech funds** | Core holders; less likely to sell |
| **Crossover funds** | Validation; but late-stage indicator |
| **Generalist HFs** | Tourists; quick to exit on disappointment |
| **Long-only funds** | Patient capital; support on pullbacks |
| **Index funds** | Mechanical; not informative |
| **VC/PE overhang** | Supply risk; watch for distributions |

### Specialist Fund Tiers (Biotech)

**Tier 1 (Highest quality signal):**
- RA Capital, Avoro, Perceptive, Baker Brothers, OrbiMed, Frazier, Vivo

**Tier 2 (Strong signal):**
- Redmile, Rock Springs, Boxer, Cormorant, RTW, EcoR1, Casdin

**Tier 3 (Good signal):**
- Janus, T. Rowe, Wellington biotech sleeve, Fidelity biotech

### Ownership Quality Score

| Factor | Positive | Negative |
|--------|----------|----------|
| Tier 1 fund ownership | +2 per fund | — |
| Tier 2 fund ownership | +1 per fund | — |
| Multiple specialists | +2 | — |
| Single large holder dominance | — | -2 (concentration risk) |
| Heavy generalist HF | — | -1 (flight risk) |
| VC >20% still holding | — | -1 (overhang) |

---

## Short Interest Analysis

### Short Interest Levels

| Short Interest | Interpretation | Risk/Opportunity |
|----------------|----------------|------------------|
| <5% of float | Normal; limited squeeze potential | Neutral |
| 5-10% | Elevated; some skepticism | Monitor |
| 10-15% | High; meaningful debate exists | Squeeze potential on positive |
| 15-20% | Very high; significant bearish bet | High squeeze risk |
| >20% | Extreme; crowded short | Binary setup |

### Float Concentration Amplifies Squeeze Risk

**Pattern (from IBRX):** When insiders own large blocks, TRUE float is much smaller than stated float. Calculate SI as % of true float, not stated float.

| Scenario | Stated Float | Insider Ownership | True Float | Stated SI | True SI |
|----------|-------------|-------------------|------------|-----------|--------|
| IBRX | 330M shares | 67% (PSS) | 109M shares | 35% | ~106% |
| Normal | 100M shares | 15% | 85M shares | 15% | 18% |

**Rule:** When insider/strategic ownership >40%, recalculate SI as % of tradeable shares. SI >50% of true float = extreme squeeze risk.

**Warning signs:**
- Founder CEO with majority control
- Strategic investor with lock-up expired
- Family office/billionaire with illiquid position
- Cross-holdings between related companies

### Days to Cover

Days to Cover = Short Interest / Average Daily Volume

| Days to Cover | Interpretation |
|---------------|----------------|
| <3 days | Easy to cover; low squeeze risk |
| 3-5 days | Moderate; normal |
| 5-10 days | Elevated; potential squeeze |
| >10 days | Very elevated; high squeeze risk |

### Cost to Borrow

| Borrow Rate | Signal |
|-------------|--------|
| <1% | Easy to short; no crowding |
| 1-5% | Moderate interest |
| 5-20% | Hard to borrow; crowded |
| >20% | Very hard to borrow; extreme crowding |

---

## Crowding Assessment

### Signs of Crowded Long

- Multiple large HFs holding >3% each
- Top 5 holders own >50% of float
- HF ownership >40% of float
- High short-term turnover
- Conference panels all bullish
- Stock runs on no news

### Signs of Crowded Short

- SI >15% of float
- Days to cover >5
- Borrow rate elevated
- Multiple bearish research notes
- Social media negativity

### Crowding Risk Matrix

| Your Position | Long Crowded | Short Crowded | Neither |
|---------------|--------------|---------------|---------|
| **Long** | ⚠️ Reduce size | ✅ Squeeze potential | ✅ Normal |
| **Short** | ✅ Unwind potential | ⚠️ Reduce size | ✅ Normal |

---

## 13-F Analysis

### How to Use 13-F Data

Source: SEC EDGAR (https://www.sec.gov/edgar/search/)

**What to look for:**
1. New positions by quality funds (bullish)
2. Position increases by existing holders (conviction)
3. New exits by quality funds (bearish)
4. Position decreases (reduced conviction)

### 13-F Scoring

| Activity | Score |
|----------|-------|
| New Tier 1 fund position | +3 |
| Tier 1 fund increase >25% | +2 |
| New Tier 2 fund position | +2 |
| Tier 1 fund exit | -3 |
| Tier 1 fund decrease >50% | -2 |
| Multiple funds decreasing | -2 |

### Timing Considerations

- 13-F filed 45 days after quarter end (stale data)
- Position may have changed since filing
- Use as directional signal, not precise timing

---

## Flow Analysis

### Institutional Flow Signals

| Flow Type | How to Detect | Meaning |
|-----------|---------------|---------|
| HF accumulation | 13F increases | Smart money entering |
| HF distribution | 13F decreases | Smart money exiting |
| Index addition | Announced | Forced buying coming |
| Index deletion | Announced | Forced selling coming |

### Secondary Offering Impact

| Secondary Type | Impact |
|----------------|--------|
| Follow-on at market | Modest dilution, signals confidence |
| Discounted offering | Bearish signal |
| ATM in place | Overhang (potential selling) |
| VC distribution | Supply pressure |

---

## Position Adjustments for Crowding

| Situation | Adjustment |
|-----------|------------|
| Very crowded long, you're long | Reduce 25-50% |
| Crowded long, positive catalyst coming | Still reduce pre-event |
| Crowded short, you're short | Reduce 25-50% |
| Crowded short, negative catalyst coming | Still reduce pre-event |
| Quality ownership, not crowded | Can size higher |

---

## Positioning Checklist

```
POSITIONING ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━

OWNERSHIP QUALITY:
□ Tier 1 specialist funds: ____
□ Tier 2 specialist funds: ____
□ Top 5 holder concentration: ____%
□ VC overhang: [ ] Yes [ ] No

SHORT INTEREST:
□ SI % of float: ____%
□ Days to cover: ___ days
□ Cost to borrow: ____%
□ SI trend: [ ] Rising [ ] Flat [ ] Falling

CROWDING:
□ Crowded long? [ ] Yes [ ] No
□ Crowded short? [ ] Yes [ ] No
□ Recent 13-F changes: Bullish/Bearish/Mixed

COMPOSITE POSITIONING SCORE: ___/5
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Quick Reference: Positioning Scorecard

| Factor | Bullish | Neutral | Bearish |
|--------|---------|---------|---------|
| Specialist ownership | Multiple Tier 1 | Some Tier 2-3 | None |
| Short interest | <5% | 5-15% | >15% |
| 13-F trend | Accumulation | Mixed | Distribution |
| HF concentration | Diversified | Moderate | Crowded |
| VC overhang | None | <10% | >20% |

**Composite:**
- 4-5 Bullish → Strong positioning tailwind
- 2-3 Bullish → Modest support
- Mixed → Neutral
- 2-3 Bearish → Positioning headwind
- 4-5 Bearish → Significant risk, reduce size
