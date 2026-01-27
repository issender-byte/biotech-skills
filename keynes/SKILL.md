---
name: keynes
description: "Position management incorporating market sentiment, sellside expectations, insider activity, technical levels, and catalyst timing. Named for John Maynard Keynes - the market can stay irrational longer than you can stay solvent. Use after graham establishes fair value to determine WHEN and HOW MUCH to act. Triggers: position sizing, entry timing, sellside consensus, insider buying/selling, short interest, crowding, catalyst positioning, technical levels."
---

# Keynes: Position Management

*"The market can stay irrational longer than you can stay solvent."*

**Scope:** Given fair value (from graham), when and how much should you act?

**Key insight:** Being right on value is not enough. You need:
- The market to eventually agree (catalyst path)
- To survive until it does (position sizing, risk management)
- To not get run over by flows (sentiment, positioning)

**Required inputs:**
- Fair value estimate (from `graham` skill)
- Current price and implied PoS
- Market data (sentiment, positioning, technicals)

## The Graham-Keynes Distinction

| Graham | Keynes |
|--------|--------|
| What is it worth? | What does the market think? |
| Intrinsic value | Market price discovery |
| Fundamental analysis | Sentiment analysis |
| "Price is what you pay" | "Beauty contest" dynamics |
| Long-term correct | Short-term survivable |

**Both matter.** Graham without Keynes = right but broke. Keynes without Graham = trading noise.

## Framework Overview

```
1. SENTIMENT CHECK → What does the market think?
2. POSITIONING CHECK → Who owns it? How crowded?
3. EXPECTATIONS CHECK → What's priced in?
4. TECHNICAL CHECK → Key levels, momentum
5. CATALYST TIMING → When will market re-rate?
6. POSITION DECISION → Size and timing
```

## Step 1: Sentiment Check

### Sellside Sentiment

| Metric | Bullish Signal | Bearish Signal |
|--------|---------------|----------------|
| Rating distribution | Few Buys (room to upgrade) | All Buys (nowhere to go) |
| PT vs. current | PTs well above (catching up) | PTs at/below (capped) |
| Estimate revisions | Raising numbers | Cutting numbers |
| Tone of notes | Cautious/skeptical | Euphoric/promotional |
| Initiation activity | Bears starting coverage | Bulls capitulating |

### Buyside Sentiment

| Metric | How to Assess |
|--------|---------------|
| HF ownership | 13F filings, ownership concentration |
| Mutual fund ownership | Quarterly filings |
| Conference attendance | IR feedback, meeting density |
| Expert network activity | Call volume, topic interest |

### Contrarian Signals

**Peak bullishness indicators:**
- "No one is bearish on this"
- All analysts at Buy
- Price targets clustered high
- Crowded long positioning

**Peak bearishness indicators:**
- "Everyone hates this name"
- Analyst downgrades cascading
- Price targets slashed
- High short interest

## Step 2: Positioning Check

### Ownership Analysis

| Owner Type | What It Tells You |
|------------|-------------------|
| Concentrated HF ownership | Crowded; vulnerable to unwinds |
| Crossover funds | Validation; but late-stage |
| Dedicated biotech funds | Core holders; less likely to sell |
| Generalist funds | Tourists; quick to exit |
| Index inclusion | Forced buying; technical support |

### Short Interest

| Short Interest Level | Interpretation |
|---------------------|----------------|
| <5% of float | Normal; limited squeeze potential |
| 5-10% | Elevated; some skepticism |
| 10-20% | High; potential squeeze on good news |
| >20% | Extreme; crowded short, binary setup |

### Insider Activity

| Signal | Interpretation | Reliability |
|--------|---------------|-------------|
| Cluster buying by multiple insiders | Strongly bullish | High |
| CEO/CFO buying | Bullish | High |
| Director buying | Moderately bullish | Medium |
| 10b5-1 selling | Neutral (programmatic) | Low signal |
| Large discretionary selling | Concerning | Medium-High |
| VC distribution | Neutral (expected) | Low signal |
| Selling into strength | Less concerning | Context-dependent |
| Selling into weakness | More concerning | Context-dependent |

### APGE Example

> "Director Fairmount Funds Management Llc sold 1,750,000 shares at $76.30"

**Assessment:** VC distribution after big run (+200% from lows). Less concerning than discretionary insider selling, but worth noting as supply overhang. Watch for more distributions.

## Step 3: Expectations Check

### What's Priced In?

| Method | Calculation |
|--------|-------------|
| Implied PoS | (EV - Cash) / NPV at 100% PoS |
| Implied peak sales | Back-solve from EV to peak |
| Implied probability | Compare to your estimate |

### Expectations vs. Reality Framework

| Your View vs. Consensus | Position Implication |
|------------------------|---------------------|
| You higher, stock cheap | Buy - market will catch up |
| You higher, stock fair | Hold - need catalyst to re-rate |
| You in line, stock fair | No edge - pass |
| You lower, stock rich | Sell/short - market will correct |

### Sellside Model Check

| What to Look For | Why It Matters |
|------------------|----------------|
| Peak sales assumptions | Are they using your TPP? |
| PoS assumptions | Explicit or implicit? |
| Timeline to launch | Conservative or aggressive? |
| Competition assumptions | Who do they include? |
| Pricing assumptions | Net vs. list? |

## Step 4: Technical Check

### Key Levels

| Level | How to Identify |
|-------|-----------------|
| Support | Prior lows, high volume areas, round numbers |
| Resistance | Prior highs, offering prices, analyst PTs |
| Moving averages | 50-day, 200-day as trend indicators |
| VWAP | Institutional average cost |

### Volume Analysis

| Pattern | Interpretation |
|---------|---------------|
| High volume up | Conviction buying |
| High volume down | Conviction selling |
| Low volume drift up | Weak rally; vulnerable |
| Low volume drift down | Lack of sellers; may stabilize |
| Volume spike at level | Significant support/resistance |

### For Biotech Specifically

| Technical Factor | Biotech Context |
|------------------|-----------------|
| Cash per share | Hard floor (usually) |
| 52-week range | Sentiment anchors |
| Post-data price | Market's verdict on news |
| Offering price | Recent capital raise = supply |

## Step 5: Catalyst Timing

### Catalyst Calendar Framework

| Catalyst Type | Typical Setup | Typical Fade |
|---------------|--------------|--------------|
| Data readout | Run into event | Sell on news (even good) |
| FDA decision | Premium into PDUFA | Binary outcome |
| Conference presentation | Modest anticipation | Depends on content |
| Earnings | Low volatility | Unless guidance change |

### When to Position

| Strategy | When to Use |
|----------|-------------|
| **Pre-catalyst** | High conviction, want full exposure to event |
| **Post-catalyst** | Let dust settle, buy on confirmation |
| **Scale in** | Moderate conviction, average into position |
| **Scale out** | Take profits into strength, reduce event risk |

### Event Risk Management

| Position Size | Catalyst Risk Tolerance |
|---------------|------------------------|
| >150 bps | Only if very high conviction on catalyst |
| 100-150 bps | Comfortable with binary outcome |
| 50-100 bps | Want exposure but limiting event risk |
| <50 bps | Tracking position; waiting for better entry |

## Step 6: Position Decision

### Sizing Framework

| Conviction Level | Graham Discount | Keynes Signals | Position Size |
|-----------------|-----------------|----------------|---------------|
| Very High | >50% undervalued | Sentiment supportive | 150-200 bps |
| High | 30-50% undervalued | Sentiment neutral | 100-150 bps |
| Moderate | 15-30% undervalued | Sentiment neutral | 50-100 bps |
| Low | <15% undervalued | Any | 0-50 bps |
| Negative | Overvalued | Sentiment negative | Short candidate |

### Adjustments for Keynes Factors

| Factor | Adjustment |
|--------|------------|
| Very crowded long | Reduce size 25-50% |
| High short interest (squeeze potential) | Can increase size if long |
| Insider buying cluster | Increase conviction |
| Heavy insider selling | Reduce size or wait |
| Near technical support | Better risk/reward |
| Near technical resistance | Trim or wait for breakout |
| Catalyst imminent | Size for event risk tolerance |
| Sentiment at extreme | Contrarian opportunity |

### Entry Tactics

| Scenario | Tactic |
|----------|--------|
| Strong conviction, fair price | Buy full position |
| Strong conviction, elevated price | Scale in on pullbacks |
| Moderate conviction | Starter position, add on confirmation |
| Good story but crowded | Wait for unwind/pullback |
| Post-selloff washout | Contrarian entry if thesis intact |

### Exit Tactics

| Scenario | Tactic |
|----------|--------|
| Approaching fair value | Begin trimming |
| Catalyst delivered, thesis played out | Exit majority |
| Sentiment euphoric, crowded | Trim into strength |
| Thesis broken | Exit immediately |
| Better opportunity elsewhere | Reallocate |

## Output: Position Management Overlay

```
═══════════════════════════════════════════════════════════════
KEYNES: POSITION MANAGEMENT OVERLAY
Company: [Name] | Ticker: [Symbol]
Graham Fair Value: $[X] | Current: $[Y] | Discount: [Z%]
═══════════════════════════════════════════════════════════════

SENTIMENT CHECK:
│ Sellside │ [X] Buys / [Y] Holds / [Z] Sells │ [Bullish/Neutral/Bearish] │
│ Avg PT │ $[X] vs current $[Y] │ [Above/At/Below] │
│ Estimate trend │ [Rising/Flat/Falling] │ │
│ Tone │ [Cautious/Neutral/Euphoric] │ │

POSITIONING CHECK:
│ HF ownership │ [X]% of float │ [Crowded/Normal/Light] │
│ Short interest │ [X]% of float │ [High/Normal/Low] │
│ Recent insider │ [Buying/Selling/Neutral] │ [Signal strength] │
│ VC overhang │ [Yes/No] │ │

EXPECTATIONS CHECK:
│ Implied PoS │ [X]% │ vs your [Y]% │
│ Consensus peak │ $[X]B │ vs your $[Y]B │
│ Delta │ [You higher/lower by Z] │ │

TECHNICAL CHECK:
│ vs 52-wk range │ [X]% from low, [Y]% from high │
│ Key support │ $[X] │ │
│ Key resistance │ $[Y] │ │
│ Trend │ [Up/Down/Sideways] │ │

CATALYST TIMING:
│ Next catalyst │ [Event] │ [Date] │
│ Setup │ [Pre-event run/Post-event buy/etc] │ │
│ Event risk │ [High/Medium/Low] │ │

POSITION RECOMMENDATION:
│ Graham says │ [Buy/Hold/Sell] at [X] bps │
│ Keynes adjustment │ [+/-] [X] bps because [reason] │
│ FINAL RECOMMENDATION │ [X] bps │ │

Entry: $[X] | Add: $[Y] | Trim: $[Z] | Stop: $[W]
═══════════════════════════════════════════════════════════════
```

## Integration with Other Skills

```
reverend-bayes → PoS estimate
       ↓
john-snow → Peak sales estimate
       ↓
graham → Fair value, implied PoS gap
       ↓
keynes → Position size, timing, entry/exit
       ↓
FINAL RECOMMENDATION
```

**Graham tells you WHAT to do. Keynes tells you WHEN and HOW MUCH.**

## Reference Files

| File | Use When |
|------|----------|
| `references/catalyst-playbook.md` | Event-driven positioning |
| `references/m-and-a-playbook.md` | M&A scenarios, short covering rules |
| `references/sentiment-indicators.md` | Assessing sellside/buyside sentiment |
| `references/positioning-analysis.md` | Ownership, short interest, crowding |
| `references/insider-activity.md` | Interpreting Form 4 filings |
| `references/technical-basics.md` | Key levels, volume analysis |
