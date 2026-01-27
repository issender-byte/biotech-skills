# Sentiment Indicators

Framework for assessing market sentiment to inform position timing and sizing.

---

## Overview

Sentiment analysis answers: **What does the market think, and how crowded is that view?**

Two types:
1. **Sellside sentiment** — analyst ratings, price targets, estimate revisions
2. **Buyside sentiment** — positioning, fund flows, conference activity

---

## Sellside Sentiment

### Rating Distribution Analysis

| Rating Mix | Interpretation | Signal |
|------------|----------------|--------|
| All Buys, no Sells | Peak bullishness, no incremental buyers | Contrarian bearish |
| Mostly Buys, few Holds | Bullish consensus | Neutral to cautious |
| Mixed ratings | Debate exists | Opportunity for differentiation |
| Mostly Holds/Sells | Bearish consensus | Contrarian bullish if fundamentals support |
| All Sells | Peak bearishness | Strong contrarian signal |

### Price Target Analysis

| PT vs Current | Interpretation |
|---------------|----------------|
| PTs well above (>30%) | Street has upside conviction |
| PTs clustered near current | Expectations baked in |
| PTs below current | Street skeptical |
| Wide PT range | High uncertainty, debate |
| Narrow PT range | Consensus (beware) |

### Estimate Revision Trends

| Trend | Signal |
|-------|--------|
| Revisions rising | Fundamental momentum |
| Revisions falling | Fundamental deterioration |
| Large upward revision | Positive surprise potential |
| Earnings whisper above consensus | Buy-side expectations higher |

### Sellside Tone Indicators

| Tone | Description | Signal |
|------|-------------|--------|
| **Euphoric** | "Best-in-class," "transformational" | Peak bullishness |
| **Promotional** | Cherry-picked data, ignore risks | Concerning |
| **Balanced** | Fair assessment of bull/bear | Healthy |
| **Cautious** | Acknowledges upside but hedged | Potentially contrarian |
| **Skeptical** | Downside focused | Bearish or contrarian |

---

## Buyside Sentiment

### Conference Activity

| Signal | Interpretation |
|--------|----------------|
| Management meeting slots full | High interest |
| Sparse attendance | Low interest (opportunity?) |
| Buy-side panels bullish | Crowded long |
| Expert network calls rising | Due diligence activity |

### Fund Flow Signals

| Flow Pattern | Signal |
|--------------|--------|
| Inflows to biotech funds | Sector tailwind |
| Outflows from biotech | Sector headwind |
| New fund launches | Peak interest (often late) |
| Fund liquidations | Potential bottom |

---

## Contrarian Indicators

### Peak Bullishness Signals

Watch for these at potential tops:
- "No one is bearish on this name"
- All analysts at Buy
- Price targets clustered high
- Crowded long positioning
- Mainstream media coverage
- Company doing secondary offering

### Peak Bearishness Signals

Watch for these at potential bottoms:
- "Everyone hates this name"
- Analyst downgrades cascading
- Price targets slashed
- High short interest
- No conference attendance
- Insider buying

---

## Sentiment Cycle

```
┌─────────────────────────────────────────────────────────────┐
│                    SENTIMENT CYCLE                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  PEAK OPTIMISM ← ─ ─ ─ ─ ─ → EUPHORIA (sell signal)        │
│        ↑                           │                        │
│   OPTIMISM                    DENIAL                        │
│        ↑                           ↓                        │
│   HOPE ← ─ ─ ─ ─ ─ ─ ─ ─ ─ → FEAR                          │
│        ↑                           ↓                        │
│   RELIEF                      PANIC                         │
│        ↑                           ↓                        │
│  PEAK PESSIMISM ← ─ ─ ─ ─ → CAPITULATION (buy signal)      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Sentiment Scoring Framework

### Rating Distribution (1-5)

| Score | Condition |
|-------|-----------|
| 5 | Strong contrarian setup (all bearish, you're bullish) |
| 4 | Healthy skepticism, room for upgrades |
| 3 | Mixed consensus |
| 2 | Crowded bullish, limited upgrade potential |
| 1 | Peak euphoria (all bullish) |

### PT Positioning (1-5)

| Score | Condition |
|-------|-----------|
| 5 | PTs significantly below your fair value |
| 4 | PTs below fair value with room to rise |
| 3 | PTs near your fair value |
| 2 | PTs above current but below fair value |
| 1 | PTs above your fair value |

### Sentiment Momentum (1-5)

| Score | Condition |
|-------|-----------|
| 5 | Improving from deep pessimism |
| 4 | Early upgrades beginning |
| 3 | Stable sentiment |
| 2 | Late-stage bullishness |
| 1 | Peak or deteriorating |

### Composite Score

**Sentiment Score = (Rating + PT + Momentum) / 3**

| Score | Interpretation | Position Adjustment |
|-------|----------------|---------------------|
| 4-5 | Favorable setup | Can size higher |
| 3-4 | Neutral | Standard sizing |
| 2-3 | Cautious | Reduce size |
| 1-2 | Unfavorable | Minimum size or avoid |

---

## Sentiment Checklist

```
SENTIMENT ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━

SELLSIDE:
□ Rating mix: ____ Buy / ____ Hold / ____ Sell
□ Average PT: $___ vs current $___ (___% upside)
□ PT range: $___ to $___ (wide/narrow?)
□ Recent changes: Upgrades or downgrades?
□ Estimate revisions: Rising/Falling/Flat

BUYSIDE:
□ Conference interest: High/Medium/Low
□ Expert network activity: Rising/Falling
□ Fund positioning: See positioning-analysis.md

CONTRARIAN SIGNALS:
□ Is everyone on one side? [ ] Yes [ ] No
□ Peak euphoria signs? [ ] Yes [ ] No
□ Peak pessimism signs? [ ] Yes [ ] No

COMPOSITE SENTIMENT SCORE: ___/5
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Integration with Position Sizing

| Your View | Sentiment | Action |
|-----------|-----------|--------|
| Bullish | Bearish consensus | Favorable - can size up |
| Bullish | Bullish consensus | Cautious - reduce size |
| Bearish | Bullish consensus | Favorable for short |
| Bearish | Bearish consensus | Cautious - crowded short |

**Key principle:** Edge is in the GAP between your view and consensus. If everyone agrees with you, the opportunity is priced in.
