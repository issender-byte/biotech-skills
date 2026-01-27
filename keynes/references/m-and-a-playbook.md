# M&A Playbook

How to analyze, position for, and trade around biotech M&A situations.

---

## Source

**Primary:** RVMD/Merck analysis (January 2026)

---

## Framework: M&A Short Cover Rule

### The Rule

**When M&A rumors emerge on a SHORT position, cover immediately unless you have a differentiated view on deal break.**

### Decision Matrix

| Your Position | M&A News | Your Thesis | Action |
|---------------|----------|-------------|--------|
| Short | Rumor/confirmed | Valuation | Cover immediately |
| Short | Rumor/confirmed | Clinical failure | Reassess - acquirer may accept risk |
| Short | Rumor/confirmed | Commercial failure | Cover - acquirer may have different view |
| Short | Rumor + upcoming positive catalyst | Any | Cover - two ways to lose |

### Why This Rule Exists

1. **Takeout premium invalidates valuation shorts** - If your thesis was "overvalued at $X," a premium makes that irrelevant
2. **Deal spread creates floor** - Stock now trades to deal price minus break risk
3. **Asymmetric risk** - Downside from deal break is less than upside from deal completion
4. **You're fighting informed capital** - Acquirer did more diligence than you

### Exception: When NOT to Cover

Only stay short if you have:
1. Specific, differentiated view on deal break (regulatory, financing, diligence issue)
2. Deal spread is wide enough to compensate for break risk
3. Your timeline allows waiting for deal resolution

---

## Framework: Deal Status Assessment

### Deal Phases

| Phase | Description | Spread Behavior |
|-------|-------------|-----------------|
| Rumor | Unconfirmed reports | Wide, volatile |
| Confirmed | Definitive agreement signed | Tighter spread |
| Regulatory review | HSR, CFIUS, etc. | Steady, may widen on concerns |
| Shareholder vote | If required | Usually tight |
| Closing | Deal completes | Zero spread |

### Break Price Estimation

| Situation | Break Price Estimate |
|-----------|---------------------|
| Premium deal, no fundamental catalyst | Pre-rumor price |
| Premium deal, positive catalyst since | Pre-rumor + catalyst value |
| Strategic merger | Pre-rumor - 10-20% |
| Hostile deal rejected | Often above pre-rumor |

---

## Framework: M&A Valuation Back-Solve

### From RVMD Analysis

> "$23bn market cap prices in ~$4bn peak sales in PDAC w/ takeout premium (6x)"

### Takeout Valuation Check

```
Implied Peak Sales = Takeout EV / Revenue Multiple

For RVMD:
$23bn takeout / 6x multiple = ~$4bn implied peak sales
```

### Is This Reasonable?

| Check | Method |
|-------|--------|
| Peak sales vs TAM | Is implied peak achievable? |
| Multiple vs comps | Is 6x in line with similar deals? |
| Premium vs historical | Is premium reasonable (30-50% typical)? |

### RVMD Example

- PDAC TAM: ~70k US incident × $200k/yr = $14bn US
- Global: >$20bn TAM
- $4bn peak at 6x = reasonable given TAM

---

## Checklist: M&A Situation Analysis

```
M&A SITUATION ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

DEAL BASICS:
□ Deal price: $_____
□ Current price: $_____
□ Spread: _____% (annualized: _____%)
□ Expected close: _____ months

BREAK RISK:
□ Regulatory path: _____________
□ Financing: _____________
□ Strategic dynamics: _____________
□ Estimated P(Close): _____%
□ Break price estimate: $_____

VALUATION CHECK:
□ Implied peak sales: $_____B
□ Multiple: _____x
□ Premium to pre-deal: _____%
□ Is valuation reasonable? [ ] Yes [ ] No

POSITION ACTION:
□ If LONG: Hold for spread? [ ] Yes [ ] No
□ If SHORT: Cover per M&A rule? [ ] Yes [ ] No
□ If FLAT: Arb opportunity? [ ] Yes [ ] No

UPCOMING CATALYSTS:
□ Catalyst during deal period? [ ] Yes [ ] No
□ If yes, how does deal change catalyst risk/reward?
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Position Sizing for M&A Arb

### Spread Arb Sizing

| Spread | Max Position | Rationale |
|--------|--------------|-----------|
| <5% annualized | Small or skip | Not worth the risk |
| 5-10% annualized | Standard | Normal arb |
| 10-20% annualized | Larger if confident | Higher return compensates |
| >20% annualized | Careful | Market sees something |

### Risk Adjustment

```
Adjusted Size = Base Size × P(Close) / Expected Holding Period

If P(Close) = 80% and holding period = 6 months:
Adjusted Size = Base × 0.8 / 0.5 = 1.6x base (capped at limits)
```

---

## Integration with Other Skills

| Skill | How M&A Informs It |
|-------|-------------------|
| **graham** | M&A floor in valuation, premium expectations |
| **keynes** | M&A short cover rule, spread dynamics |
| **simons** | M&A positions have different risk profile |

---

## Case Study: RVMD/Merck

**Situation:**
- Short position on RVMD
- M&A rumors with Merck
- $23bn market cap post-rumor
- Upcoming pivotal 2L PDAC data (high PoS)

**Analysis:**
- Takeout implies $4bn peak sales at 6x multiple
- $4bn peak is reasonable for PDAC ($20bn+ TAM)
- Upcoming catalyst has high PoS to be positive
- Two ways to lose: deal closes OR positive data

**Action:**
- Cover short per M&A short cover rule
- No differentiated view on deal break
- Can't hold short into positive catalyst
- Move to neutral
