---
name: simons
description: "Portfolio construction and risk management - sizing positions relative to each other, managing correlations, gross/net exposure, and TA concentration. Named for Jim Simons - systematic risk management at scale. Use after individual stock analysis (reverend-bayes → john-snow → graham → keynes) to determine how a position fits within the broader portfolio. Triggers: portfolio sizing, correlation, gross exposure, net exposure, concentration, pair trades, risk budget, TA exposure, hedging, position limits."
---

# Simons: Portfolio & Risk Management

*"The best way to minimize risk is to think."*

**Scope:** How does this position fit within the portfolio? Size relative to correlations, exposures, and risk budget.

**Required inputs:**
- Position recommendation (from `keynes`)
- Current portfolio (all positions, sizes, directions)
- Risk parameters (gross/net limits, concentration limits)

**Out of scope:** Single-stock analysis → use `reverend-bayes`, `john-snow`, `graham`, `keynes`.

## Why This Skill Exists

Individual stock analysis tells you:
- APGE is 30% undervalued (Graham)
- Buy 125 bps (Keynes)

But portfolio context matters:
- Already long 200 bps in AD names → adding APGE increases TA concentration
- Short a TYK2 name → partially hedged to I&I, or doubling down?
- At 180% gross → do we have room for new positions?
- Correlation to existing longs → diversification or redundancy?

**Simons integrates individual decisions into portfolio construction.**

## Framework Overview

```
1. CURRENT PORTFOLIO STATE → What do we own?
2. EXPOSURE ANALYSIS → Gross, net, factor exposures
3. CORRELATION MAPPING → How does new position relate?
4. CONCENTRATION CHECK → TA, market cap, phase, catalyst
5. RISK BUDGETING → How much risk can we allocate?
6. FINAL SIZING → Adjust for portfolio context
```

## Step 1: Current Portfolio State

### Portfolio Snapshot

```
═══════════════════════════════════════════════════════════════
PORTFOLIO SNAPSHOT
Date: [Date]
═══════════════════════════════════════════════════════════════

EXPOSURE SUMMARY:
│ Metric          │ Current │ Target │ Limit  │ Status    │
│ Gross Exposure  │ [X]%    │ [Y]%   │ [Z]%   │ [OK/High] │
│ Net Exposure    │ [X]%    │ [Y]%   │ ±[Z]%  │ [OK/High] │
│ Long Exposure   │ [X]%    │        │        │           │
│ Short Exposure  │ [X]%    │        │        │           │

POSITION COUNT:
│ Longs  │ [X] positions │ Avg size: [Y] bps │
│ Shorts │ [X] positions │ Avg size: [Y] bps │
│ Total  │ [X] positions │                   │

TOP POSITIONS:
│ Ticker │ Direction │ Size (bps) │ TA        │ Thesis        │
│        │           │            │           │               │
│        │           │            │           │               │
│        │           │            │           │               │
═══════════════════════════════════════════════════════════════
```

### Exposure Definitions

| Metric | Calculation | Typical Range |
|--------|-------------|---------------|
| Gross Exposure | |Longs| + |Shorts| | 150-250% |
| Net Exposure | Longs - Shorts | 20-80% net long |
| Beta-Adjusted Net | Σ(Position × Beta) | Varies |

## Step 2: Exposure Analysis

### Factor Exposures

Track exposure to key factors that drive biotech returns:

| Factor | Description | How to Measure |
|--------|-------------|----------------|
| **TA Exposure** | AD, oncology, CNS, CV, etc. | Σ positions by TA |
| **Phase Exposure** | Ph1, Ph2, Ph3, commercial | Σ positions by phase |
| **Catalyst Density** | Near-term binary events | # positions with catalyst <3mo |
| **Market Cap** | Small, mid, large | Σ positions by cap bucket |
| **Quality** | Cash runway, management | Subjective overlay |

### TA Concentration

```
TA EXPOSURE ANALYSIS:
│ Therapeutic Area │ Long (bps) │ Short (bps) │ Net (bps) │ % of Gross │
│ Atopic Dermatitis│            │             │           │            │
│ Oncology         │            │             │           │            │
│ CNS              │            │             │           │            │
│ Cardio/Metabolic │            │             │           │            │
│ Rare Disease     │            │             │           │            │
│ Other I&I        │            │             │           │            │
│ TOTAL            │            │             │           │            │

CONCENTRATION FLAGS:
- Single TA >30% of gross: [Flag if true]
- Single position >5% of gross: [Flag if true]
- Top 5 positions >50% of gross: [Flag if true]
```

### Phase Exposure

| Phase | Typical Characteristics | Risk Profile |
|-------|------------------------|--------------|
| Preclinical | High upside, high failure | Very high vol |
| Phase 1 | Safety/PK, dose finding | High vol |
| Phase 2 | PoC, efficacy signal | High vol, binary |
| Phase 3 | Pivotal, registration | Medium-high vol |
| Commercial | Revenue, execution | Lower vol |

```
PHASE EXPOSURE:
│ Phase      │ Long (bps) │ Short (bps) │ Net (bps) │
│ Preclinical│            │             │           │
│ Phase 1    │            │             │           │
│ Phase 2    │            │             │           │
│ Phase 3    │            │             │           │
│ Commercial │            │             │           │
```

## Step 3: Correlation Mapping

### Why Correlations Matter

Two positions can be:
- **Diversifying**: Different drivers, low correlation → both can work
- **Redundant**: Same drivers, high correlation → doubling down on same bet
- **Hedged**: Opposite exposures → one offsets the other

### Correlation Clusters in Biotech

| Cluster Type | Example | Correlation Driver |
|--------------|---------|-------------------|
| Same target | Two IL-13 antibodies | Mechanism validation |
| Same TA | Multiple AD names | TA sentiment, M&A |
| Same phase | Multiple Phase 3 names | Risk-on/off flows |
| Same market cap | Small cap biotechs | Factor flows |
| Competitor set | APGE vs Dupixent exposure | Zero-sum dynamics |

### Correlation Assessment

For a new position, assess correlation to existing book:

```
CORRELATION TO EXISTING POSITIONS:
│ Existing Position │ Correlation │ Driver                    │
│ [Ticker]          │ High/Med/Low│ Same TA / Same target / etc│
│ [Ticker]          │ High/Med/Low│                           │
│ [Ticker]          │ High/Med/Low│                           │

NET EFFECT:
- Adding [X] increases effective AD exposure by [Y] bps
- Correlated to [Z] existing positions
- Diversification benefit: [High/Medium/Low/None]
```

### Pair Trade Dynamics

When long and short in same TA:

| Scenario | Long Position | Short Position | Net Exposure |
|----------|--------------|----------------|--------------|
| TA rallies | Gains | Loses | Partially hedged |
| TA sells off | Loses | Gains | Partially hedged |
| Long wins, short loses | Gains | Gains | Best case |
| Long loses, short wins | Loses | Loses | Worst case |

**Key question:** Is this a *spread* (betting on relative performance) or *directional* (net long/short the TA)?

## Step 4: Concentration Check

### Position-Level Limits

| Limit Type | Typical Range | Rationale |
|------------|---------------|-----------|
| Max single position | 300-500 bps | Idiosyncratic risk |
| Max TA concentration | 25-35% of gross | TA-level drawdown |
| Max catalyst overlap | 3-5 positions/month | Event clustering |
| Min position size | 25-50 bps | Meaningful impact |

### Concentration Flags

```
CONCENTRATION CHECKLIST:
[ ] No single position >5% of NAV
[ ] No single TA >30% of gross
[ ] No more than 3 binary catalysts same week
[ ] Top 10 positions <60% of gross
[ ] Largest long < 2x average position
[ ] Largest short < 1.5x average position
```

### APGE Example

If adding 125 bps APGE to a portfolio that already has:
- 150 bps long in another AD name (e.g., CRVS)
- 75 bps short in Dupixent-exposed name

**Assessment:**
- Total AD long exposure: 150 + 125 = 275 bps
- AD short exposure: 75 bps
- Net AD: 200 bps long
- AD as % of gross (assuming 200% gross): 175 bps / 4000 bps = 4.4%

→ Acceptable concentration, but now meaningful AD bet

## Step 5: Risk Budgeting

### Risk Budget Framework

Allocate risk based on:
1. **Conviction** - Higher conviction → more risk budget
2. **Edge** - Larger edge vs consensus → more budget
3. **Correlation** - Lower correlation to book → more budget
4. **Liquidity** - More liquid → can size larger

### Expected Contribution to Portfolio Vol

```
Position Risk Contribution ≈ Position Size × Position Vol × Correlation to Portfolio

Example:
- APGE size: 125 bps
- APGE vol: 60% annualized
- Correlation to portfolio: 0.4
- Risk contribution: 125 × 0.60 × 0.4 = 30 bps of portfolio vol
```

### Risk-Adjusted Sizing

| Conviction/Edge | Vol Profile | Suggested Size |
|-----------------|-------------|----------------|
| Very high edge, low vol | Low risk per unit | Size up (150-200 bps) |
| Very high edge, high vol | High risk per unit | Moderate (100-150 bps) |
| Moderate edge, low vol | Moderate risk | Standard (75-125 bps) |
| Moderate edge, high vol | High risk | Smaller (50-100 bps) |
| Low edge, any vol | Limited upside | Minimal (25-50 bps) |

### Kelly Criterion (Simplified)

```
Optimal Size = Edge / Odds

Where:
- Edge = Your PoS - Implied PoS
- Odds = Upside / Downside

Example (APGE):
- Your PoS: 70%
- Implied PoS: 35%
- Edge: 35%
- Upside: +60% to fair value
- Downside: -30% to floor
- Odds: 2:1
- Kelly: 35% / 2 = 17.5% of bankroll

In practice, use fractional Kelly (25-50%) for biotechs:
- Full Kelly: 17.5%
- Half Kelly: 8.75%
- Quarter Kelly: 4.4%

→ For a fund, quarter Kelly ≈ 100-150 bps position
```

## Step 6: Final Sizing

### Adjustment Waterfall

```
START: Keynes recommendation (125 bps)
│
├─ Gross exposure check
│  └─ At limit? → Reduce or fund from elsewhere
│
├─ TA concentration check
│  └─ Would exceed 30%? → Reduce
│
├─ Correlation check
│  └─ High correlation to existing? → Reduce 20-30%
│
├─ Catalyst clustering check
│  └─ Multiple events same window? → Reduce
│
├─ Liquidity check
│  └─ >10% ADV daily? → Reduce to fit liquidity
│
└─ FINAL SIZE: [Adjusted bps]
```

### Documentation

```
SIZING DECISION:
│ Input                    │ Adjustment │ Running Size │
│ Keynes base recommendation│ -          │ 125 bps      │
│ Gross exposure headroom   │ OK         │ 125 bps      │
│ TA concentration          │ -15 bps    │ 110 bps      │
│ Correlation to book       │ -10 bps    │ 100 bps      │
│ Catalyst clustering       │ OK         │ 100 bps      │
│ Liquidity constraint      │ OK         │ 100 bps      │
│ FINAL SIZE                │            │ 100 bps      │
```

## Output: Portfolio Integration Assessment

```
═══════════════════════════════════════════════════════════════
SIMONS: PORTFOLIO INTEGRATION ASSESSMENT
New Position: [Ticker] | Direction: [Long/Short] | Proposed: [X] bps
═══════════════════════════════════════════════════════════════

CURRENT PORTFOLIO STATE:
│ Gross: [X]% │ Net: [Y]% │ Positions: [Z] │
│ Headroom to gross limit: [X]% │

EXPOSURE IMPACT:
│ Factor          │ Before    │ After     │ Change    │
│ AD Exposure     │ [X] bps   │ [Y] bps   │ +[Z] bps  │
│ Phase 2 Exposure│ [X] bps   │ [Y] bps   │ +[Z] bps  │
│ Net Exposure    │ [X]%      │ [Y]%      │ +[Z]%     │

CORRELATION ANALYSIS:
│ Related Position │ Correlation │ Net Effect              │
│ [Ticker]         │ [H/M/L]     │ [Increases/hedges] [TA] │
│ [Ticker]         │ [H/M/L]     │                         │

Effective new exposure (correlation-adjusted): [X] bps

CONCENTRATION CHECK:
[ ] Single position limit: [OK/FLAG]
[ ] TA concentration: [OK/FLAG]
[ ] Catalyst clustering: [OK/FLAG]
[ ] Top positions: [OK/FLAG]

RISK BUDGET:
│ Position vol (ann.)  │ [X]%     │
│ Correlation to book  │ [X]      │
│ Risk contribution    │ [X] bps  │
│ Kelly optimal        │ [X] bps  │
│ Risk budget available│ [X] bps  │

SIZING WATERFALL:
│ Step                      │ Adjustment │ Size    │
│ Keynes recommendation     │ -          │ [X] bps │
│ [Adjustment 1]            │ [±X]       │ [Y] bps │
│ [Adjustment 2]            │ [±X]       │ [Y] bps │
│ FINAL RECOMMENDED SIZE    │            │ [Z] bps │

IMPLEMENTATION:
│ Entry price │ $[X]     │ Stop: $[Y] │
│ Days to build │ [X] days │ % ADV: [Y]% │
│ Funding source │ [New capital / Trim existing] │

>>> INPUT FROM: keynes (base position recommendation)
>>> OUTPUT: Final position size, implementation plan
═══════════════════════════════════════════════════════════════
```

## Special Situations

### Adding to Winners

| Consideration | Guidance |
|---------------|----------|
| Position already large | Higher bar to add |
| Thesis still intact | Required to add |
| Correlation increasing | May be doubling down |
| Approaching max size | Trim instead of add |

### Cutting Losers

| Consideration | Guidance |
|---------------|----------|
| Thesis broken | Cut immediately |
| Thesis intact, price down | May add, not cut |
| Stop hit | Follow rules |
| Correlation changed | Reassess fit |

### Pair Trades

```
PAIR TRADE ANALYSIS:
Long: [Ticker A] | Size: [X] bps
Short: [Ticker B] | Size: [Y] bps
Net TA exposure: [Z] bps

Spread thesis: [Why A outperforms B]
Correlation between A and B: [X]
Expected spread vol: [Y]%
Spread target: [Z]%
```

### Catalyst Hedging

When multiple positions have correlated catalysts:

| Strategy | When to Use |
|----------|-------------|
| Reduce all sizes | High correlation, can't pick winner |
| Offset with short | Hedge TA while keeping best idea |
| Stagger entries | Reduce event clustering |
| Accept concentration | Very high conviction |

## Integration with Other Skills

```
reverend-bayes → PoS estimate
       ↓
john-snow → Peak sales estimate
       ↓
graham → Fair value, intrinsic value
       ↓
keynes → Timing, standalone position size
       ↓
simons → Portfolio-adjusted final size
       ↓
TRADE EXECUTION
```

**The full stack:**
1. **Bayes**: Should this drug work? (70% PoS)
2. **Snow**: What's the market? ($5B peak)
3. **Graham**: What's it worth? ($112/share, 35% cheap)
4. **Keynes**: When to buy? (Now, 125 bps base)
5. **Simons**: How much given portfolio? (100 bps after adjustments)

## Reference Files

| File | Content |
|------|---------|
| `references/exposure-limits.md` | Gross/net targets by strategy |
| `references/correlation-clusters.md` | Common biotech correlations |
| `references/position-sizing.md` | Kelly, risk parity, heuristics |

**Planned (not yet created):**
- `references/pair-trade-construction.md` - Spread construction, hedging
- `references/catalyst-calendar.md` - Event clustering management
