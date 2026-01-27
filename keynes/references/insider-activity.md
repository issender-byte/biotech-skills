# Insider Activity Analysis

Framework for interpreting insider transactions to inform position timing.

---

## Overview

Insider trading (legal, disclosed) is one of the most reliable signals in equity investing. Insiders know more about their company than any outside investor.

**Key insight:** Not all insider transactions are equal. Filter for high-information trades.

---

## Form 4 Basics

### What Gets Filed

| Form | Trigger | Timing |
|------|---------|--------|
| **Form 4** | Any change in beneficial ownership | Within 2 business days |
| **Form 3** | Initial statement (new insider) | Within 10 days |
| **Form 5** | Annual summary of unreported | Within 45 days of FY end |

### Who is an "Insider"

| Insider Type | Definition | Signal Quality |
|--------------|------------|----------------|
| **Officer** | CEO, CFO, COO, CMO, CSO | Highest |
| **Director** | Board member | High |
| **10% Owner** | >10% beneficial owner | Medium (may be VC/fund) |

### Transaction Codes

| Code | Meaning | Signal Value |
|------|---------|--------------|
| **P** | Open market purchase | **Highest** — discretionary buy |
| **S** | Open market sale | Medium — many reasons |
| **M** | Option exercise | Low — often paired with sale |
| **A** | Grant/award | None — compensation |
| **G** | Gift | None |
| **F** | Tax withholding | None — automatic |
| **J** | Other (10b5-1) | Low — programmatic |

---

## High-Information vs Low-Information Trades

### High-Information (Pay Attention)

| Trade Type | Why It Matters |
|------------|----------------|
| **Open market purchase (P)** | Discretionary; insider betting own money |
| **Cluster buying** | Multiple insiders buying = coordinated conviction |
| **C-suite buying** | CEO/CFO have most information |
| **Buying into weakness** | Contrarian signal |
| **First purchase in years** | Change in conviction |
| **Large relative to comp** | Meaningful to insider |

### Low-Information (Mostly Ignore)

| Trade Type | Why It's Low Signal |
|------------|---------------------|
| **10b5-1 sales** | Programmatic; set months ago |
| **Option exercise + sale** | Liquidity, tax planning |
| **VC distributions** | Expected after lockup |
| **Small director purchases** | May be board requirement |
| **Tax withholding (F)** | Automatic, no discretion |

---

## Interpreting Different Insiders

### By Role

| Role | Information Quality | Notes |
|------|---------------------|-------|
| **CEO** | Highest | Knows everything |
| **CFO** | Very high | Financial visibility |
| **CMO/CSO** | High for clinical | Pipeline insight |
| **COO** | High for commercial | Execution insight |
| **Director** | Medium | Board-level only |
| **10% Owner (fund)** | Medium | May be rebalancing |

### By Transaction Type

| Insider | Buying | Selling |
|---------|--------|---------|
| C-suite | Very bullish | Context-dependent |
| Director | Bullish | Less concerning |
| VC/Fund | Unusual (bullish) | Expected (low signal) |

---

## Red Flags

### Concerning Selling Patterns

| Pattern | Concern Level |
|---------|---------------|
| CEO selling >25% holdings | High |
| Multiple executives same window | High |
| Selling accelerated vs. history | Medium-High |
| Selling into weakness | High |
| Selling before known catalyst | Very High |
| New 10b5-1 filed recently | Medium (often precedes selling) |
| 10b5-1 modification/termination | High |

### Context Matters

| Selling Context | Interpretation |
|-----------------|----------------|
| After big run | Less concerning (taking profit) |
| Into strength | Less concerning |
| Into weakness | More concerning |
| Before data readout | Very concerning (CMO/CSO) |
| Diversification/tax | Neutral if consistent pattern |

---

## Bullish Signals

### Strong Buy Signals

| Signal | Strength |
|--------|----------|
| Cluster buying (3+ insiders) | Very strong |
| C-suite buying | Strong |
| Buying after significant decline | Strong |
| First purchase in years | Strong |
| Large purchase relative to comp | Strong |
| Board member buying own shares | Moderate |

### The Cluster Effect

Cluster buying = Multiple insiders buying within 30-60 days

| # of Insiders Buying | Signal |
|---------------------|--------|
| 1 | Interesting |
| 2 | Notable |
| 3+ | Strong bullish signal |

---

## Insider Activity Scoring

### Scoring Framework (-3 to +3)

| Activity | Score |
|----------|-------|
| Cluster buying (3+ insiders) | +3 |
| C-suite buying | +2 |
| Single insider buying | +1 |
| No activity | 0 |
| 10b5-1 sales (programmatic) | 0 |
| Single discretionary selling | -1 |
| Multiple insider selling | -2 |
| C-suite selling into weakness | -3 |

### Position Adjustment

| Score | Adjustment |
|-------|------------|
| +2 to +3 | Increase conviction 10-20% |
| +1 | Slight positive |
| 0 | No adjustment |
| -1 | Monitor closely |
| -2 to -3 | Reduce size or exit |

---

## Data Sources

| Source | Coverage | Timeliness |
|--------|----------|------------|
| SEC EDGAR | Complete | 2 business days |
| OpenInsider | Aggregated | Same day |
| InsiderScore | Analyzed | Same day |
| Bloomberg | Integrated | Real-time |

---

## Insider Activity Checklist

```
INSIDER ACTIVITY ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━

RECENT ACTIVITY (90 days):
□ Purchases: ___ transactions, $___ total
□ Sales: ___ transactions, $___ total
□ Net: [ ] Buying [ ] Selling [ ] Mixed [ ] None

KEY TRANSACTIONS:
□ C-suite buying? [ ] Yes [ ] No
□ Cluster buying? [ ] Yes [ ] No
□ Concerning sales? [ ] Yes [ ] No

CONTEXT:
□ Stock performance: Up/Down ___% in period
□ Upcoming catalysts: _______________
□ Historical pattern: Consistent/Changed

INSIDER SCORE: ___/+3 to -3
POSITION ADJUSTMENT: _______________
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Historical Return Spread (Verdad Research)

Based on insider activity signal (Sept 2013–Oct 2025):

| Quintile | Signal | Annualized Return |
|----------|--------|-------------------|
| Q1 | Most bearish | 0% |
| Q2 | Bearish | +7% |
| Q3 | Neutral | +9% |
| Q4 | Bullish | +15% |
| Q5 | Most bullish | +7% |

**Key insight:** Q4 (bullish) shows best returns. Q5 (extreme buying) shows lower returns, possibly due to over-optimism or small samples.

**Practical application:** Use as confirming signal, not primary driver. Best combined with specialist ownership and short interest.

---

## Quick Reference

### Bullish Signals
- C-suite open market purchase
- Cluster buying (3+ insiders)
- Buying after significant decline
- First purchase in years
- Large purchase relative to compensation

### Bearish Signals
- C-suite discretionary selling outside 10b5-1
- Multiple executives selling same period
- Selling into weakness
- CMO/CSO selling before data readout
- 10b5-1 plan modification/termination

### Ignore
- 10b5-1 scheduled sales
- Option exercise + immediate sale
- VC post-lockup distribution
- Tax withholding (F code)
- Small director purchases (board policy)
