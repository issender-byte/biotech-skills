---
name: graham
description: "Translate clinical PoS and commercial peak sales into fair value and investment recommendation. Named for Benjamin Graham - we seek margin of safety. Use when determining if a stock is cheap or expensive, assessing risk/reward asymmetry, or validating short theses. Requires PoS (from reverend-bayes) and peak sales (from john-snow) as inputs. Triggers: valuation, fair value, rNPV, implied PoS, risk/reward, position sizing, short thesis, catalyst asymmetry."
---

# Graham: Biotech Valuation

*"Price is what you pay. Value is what you get."*

**Scope:** Given PoS and peak sales, what's fair value and risk/reward?

**Required inputs:**
- PoS estimate (from `reverend-bayes` skill)
- Peak sales estimate (from `john-snow` skill)
- Current stock price and market cap

**Out of scope:** Clinical PoS assessment → use `reverend-bayes`. Peak sales estimation → use `john-snow`.

## Output

```
Fair Value: $[X-Y] per share
Current Price: $[Z] → [Over/Under]valued by [N]%
Implied PoS at current: [X%] vs. your estimate [Y%]
Recommendation: [Buy/Hold/Sell/Short] with [position size]
```

## Framework Overview

```
1. rNPV CALCULATION → Probability-weighted value
2. SCENARIO ANALYSIS → Range of outcomes
3. IMPLIED PoS → What's market pricing?
4. VALUATION FLOOR → Downside protection
5. CATALYST ASYMMETRY → Risk/reward on events
6. RECOMMENDATION → Position sizing
```

## Step 1: rNPV Calculation

**→ See `references/rnpv-methodology.md` for detailed formulas and examples**

### Quick Framework

```
rNPV = Σ (Peak Sales × Margin × Multiple × PoS × Discount Factor) - Costs
```

| Shortcut | Formula | Use |
|----------|---------|-----|
| Peak multiple | Peak × 4x × PoS | Quick estimate |
| Royalty value | Peak × Royalty% × 10x × PoS | Partner economics |

### Multi-Asset Template

| Asset | Indication | PoS | Peak Sales | Prob-Adj NPV |
|-------|------------|-----|------------|--------------|
| Lead | [A] | X% | $YB | $Z |
| Second | [B] | X% | $YB | $Z |
| **Total Pipeline** | | | | **$Sum** |

+ Cash − Debt − Dev Costs = **Fair Value**

## Step 2: Scenario Analysis

### Three-Scenario Model

| Scenario | PoS | Peak Sales | NPV/Share |
|----------|-----|------------|-----------|
| **Bull** | High end | High end | $X |
| **Base** | Center | Center | $Y |
| **Bear** | Low end | Low end | $Z |
| **Weighted** | | | $Avg |

### Probability Weighting

```
Weighted Value = P(Bull) × Bull + P(Base) × Base + P(Bear) × Bear

Example:
- Bull: 20% × $50 = $10
- Base: 50% × $30 = $15
- Bear: 30% × $10 = $3
- Weighted: $28
```

## Step 3: Implied PoS Analysis

### Back-Solving for Implied PoS

**What PoS is the market pricing in?**

```
Current EV = NPV at 100% PoS × Implied PoS
Implied PoS = Current EV / NPV at 100%

Example:
- Current EV: $2B
- NPV at 100% PoS: $5B
- Implied PoS: 40%
```

### Interpretation

| Your PoS vs. Implied | Interpretation | Action |
|---------------------|----------------|--------|
| Your PoS >> Implied | Market too pessimistic | Buy |
| Your PoS = Implied (±10%) | Fairly valued | Hold |
| Your PoS << Implied | Market too optimistic | Sell/Short |

## Step 4: Valuation Floor Analysis

### Sources of Downside Protection

| Floor Type | Calculation | When It Matters |
|------------|-------------|-----------------|
| **Cash** | Net cash per share | Binary events |
| **Other pipeline** | rNPV of non-lead assets | Lead failure |
| **Platform value** | Technology/capability worth | If drug fails, platform remains |
| **Acquisition floor** | Strategic premium | M&A interest |
| **Royalty/milestone** | Contracted payments | Partner deals |

### The Mike Question (from ALMS)

> "At $1.2bn cap and $850mm EV, and an MOA that is almost certain to hit stats, the skew seems up to me."

**Calculate:**
```
Current EV: $850M
Cash: $350M
Implied pipeline value: $500M

If trial hits: Stock to $X (upside Y%)
If trial misses: Stock to ~cash (downside Z%)

Is the expected value positive even on a "stat sig but underwhelming" outcome?
```

## Step 5: Catalyst Asymmetry

### Event Risk/Reward

| Scenario | Probability | Stock Move | EV Impact |
|----------|-------------|------------|-----------|
| Beat expectations | X% | +Y% | +$Z |
| Meet expectations | X% | +/-Y% | +/-$Z |
| Miss expectations | X% | -Y% | -$Z |
| **Weighted EV** | | | **$Sum** |

### Short Thesis Validation

**From ALMS exchange - before shorting, verify:**

1. **Methodology check:** Are projections using right metric ($ vs. volume)?
2. **Valuation floor:** What's implied pipeline value? Any downside protection?
3. **Catalyst asymmetry:** Is weighted EV actually negative?
4. **Mechanism comparability:** Are comps truly comparable?

### When Short Doesn't Work

**Even if you're right about fundamentals:**
- If weighted EV > 0, short has negative expected value
- "Stat sig but underwhelming" may still move stock up
- M&A risk creates unlimited upside for short
- Cash floor limits downside capture

## Step 6: Recommendation Framework

### Position Sizing

| Conviction | Your PoS vs. Implied | Position Size |
|------------|---------------------|---------------|
| High | >20% higher | 100-200 bps |
| Medium | 10-20% higher | 50-100 bps |
| Low | <10% higher | 25-50 bps |
| Neutral | Within 10% | 0 bps |
| Negative | Your PoS lower | Short or avoid |

### Recommendation Categories

| Category | Criteria | Action |
|----------|----------|--------|
| **Strong Buy** | >30% undervalued, high conviction | Max position |
| **Buy** | 15-30% undervalued | Add to position |
| **Hold** | Within ±15% of fair value | Maintain |
| **Sell** | >15% overvalued | Trim/exit |
| **Short** | >30% overvalued + negative catalyst asymmetry | Short position |

### Entry/Exit Triggers

```
BUY if: Stock falls to $X (implies Y% PoS, below your Z%)
SELL if: Stock rises to $X (implies Y% PoS, above your Z%)
COVER SHORT if: [Specific catalyst or price level]
```

## Deliverable: Valuation Assessment

```
═══════════════════════════════════════════════════════════════
BIOTECH VALUATION ASSESSMENT
Company: [Name] | Ticker: [Symbol]
Current Price: $[X] | Market Cap: $[Y] | EV: $[Z]
═══════════════════════════════════════════════════════════════

INPUTS (from other skills):
- PoS (clinical-trial-pos): [X-Y%]
- Peak Sales (commercial-peak-sales): $[X-Y]B

rNPV CALCULATION:
│ Asset │ PoS │ Peak Sales │ NPV │ Prob-Adj │
│ Lead │ │ │ │ │
│ Other │ │ │ │ │
│ Cash │ - │ - │ $X │ $X │
│ TOTAL │ │ │ │ $Sum │

Fair Value: $[X] per share

SCENARIO ANALYSIS:
│ Scenario │ PoS │ Peak │ Value │ Prob │ Weighted │
│ Bull │ │ │ │ │ │
│ Base │ │ │ │ │ │
│ Bear │ │ │ │ │ │
│ WEIGHTED │ │ │ │ │ $Sum │

IMPLIED PoS ANALYSIS:
- Current price implies: [X%] PoS
- Your estimate: [Y%] PoS
- Delta: [Z] points → [Over/Under]valued

VALUATION FLOOR:
- Cash: $[X] per share
- Other pipeline: $[Y] per share
- Acquisition floor: $[Z] per share
- Max downside: [X%] to floor

CATALYST ASYMMETRY:
│ Outcome │ Probability │ Move │ EV │
│ Beat │ │ │ │
│ Meet │ │ │ │
│ Miss │ │ │ │
│ WEIGHTED EV │ │ │ $[X] │

RECOMMENDATION: [Buy/Hold/Sell/Short]
Position Size: [X bps]
Entry: $[X] | Exit: $[Y] | Stop: $[Z]

KEY RISKS:
1. [Risk 1]
2. [Risk 2]

>>> INPUT FROM: reverend-bayes (PoS)
>>> INPUT FROM: john-snow (peak sales)
═══════════════════════════════════════════════════════════════
```

## Reference Files

| File | Use When |
|------|----------|
| `references/rnpv-methodology.md` | Detailed NPV calculations |
| `references/short-thesis-validation.md` | Validating short positions |

**Planned (not yet created):**
- `references/comparable-transactions.md` - M&A comp frameworks
- `references/economic-share.md` - LOE/exclusivity framework
