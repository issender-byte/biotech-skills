# Street Expects Integration

How to combine trader intelligence (buyside sentiment, expected moves, street scenarios) with fundamental analyst views to generate actionable trade recommendations.

---

## Source

**Primary:** OCUL SOL-1 analysis (December 2025) - Adrian (trader) + ZH (fundamental analyst) collaboration

---

## Why This Matters

Fundamental analysis tells you **what should happen**.
Street expects tell you **what's priced in**.

The edge comes from the gap between the two.

---

## Framework: Information Sources

### Trader Intelligence (What Market Expects)

| Source | What It Tells You |
|--------|-------------------|
| Options market | Implied move, skew |
| Sellside notes | Consensus view, PT distribution |
| Hedge fund positioning | Who owns it, concentration |
| Short interest | Skepticism level |
| Flow data | Who's buying/selling |
| Channel checks | Expert network chatter |

### Fundamental Analysis (What Should Happen)

| Source | What It Tells You |
|--------|-------------------|
| PoS assessment | Probability of clinical success |
| Peak sales model | Revenue potential |
| Valuation | Fair value vs current |
| Competitive dynamics | Market positioning |
| Timeline | When value will be realized |

---

## Framework: Combining Views

### Step 1: Document Street Expectations

Before any catalyst, document:
- Consensus PoS
- Expected stock move on success/failure
- Key debates in street research
- Options-implied move

### Step 2: Document Your View

From skills framework:
- Your PoS (reverend-bayes)
- Your peak sales (john-snow)
- Your fair value (graham)
- Your positioning read (keynes)

### Step 3: Calculate Edge

```
Edge = Your View - Street Consensus

If Edge > 0 and significant → Opportunity exists
If Edge ≈ 0 → No edge, wait or pass
If Edge < 0 → You're the consensus, dangerous
```

### Step 4: Size Based on Edge

| Edge Magnitude | Position Size |
|----------------|---------------|
| <10% delta | Tracking position |
| 10-20% delta | Standard position |
| >20% delta | Larger position if conviction high |

---

## Framework: Catalyst Scenarios

### Pre-Catalyst Scenario Matrix

| Outcome | Your PoS | Street PoS | Stock Move (Your Est) | Street Move | Edge |
|---------|----------|------------|----------------------|-------------|------|
| Strong success | 30% | 30% | +50% | +40% | +10% |
| Modest success | 20% | 25% | +20% | +15% | +5% |
| Miss | 40% | 40% | -40% | -35% | -5% |
| Failure | 10% | 5% | -60% | -70% | +10% |

### Weighted Expected Value

```
Weighted EV = Σ (Probability × Stock Move)

Your weighted EV vs Street weighted EV = Net Edge
```

---

## Framework: Trader-Analyst Collaboration

### Division of Labor

| Trader Provides | Analyst Provides |
|-----------------|------------------|
| Current positioning | PoS estimate |
| Options pricing | Peak sales estimate |
| Flow observations | Competitive analysis |
| Street scenarios | Valuation |
| Execution advice | Catalyst timeline |

### Communication Protocol

**Before catalyst:**
1. Analyst: Delivers 5PTer with PoS and scenarios
2. Trader: Maps to street expects and options pricing
3. Joint: Agree on position and sizing

**After catalyst:**
1. Trader: Executes per plan (or flags deviation)
2. Analyst: Updates thesis based on data
3. Joint: Debrief and document learnings

---

## Checklist: Catalyst Trade Setup

```
CATALYST TRADE SETUP
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

FUNDAMENTAL VIEW:
□ PoS: _____%
□ Key debates: ______________
□ Your differentiated view: ______________
□ Fair value on success: $______
□ Fair value on failure: $______

STREET EXPECTS:
□ Consensus PoS: _____%
□ Options implied move: ±_____%
□ Street "bogey": ______________
□ Short interest: _____%

EDGE CALCULATION:
□ Your PoS vs street: _____% delta
□ Your success scenario vs street: _____% delta
□ Your failure scenario vs street: _____% delta
□ Weighted EV delta: _____% 

POSITION:
□ Direction: [Long/Short/Flat]
□ Size: _____ bps
□ Entry: $_______
□ Stop on failure: $_______
□ Target on success: $_______
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Case Study: OCUL SOL-1

### Context
Phase 3 data readout expected for SOL-1 in retinal disease

### Street Expects (Adrian/Trader)
- Consensus PoS: ~65%
- Options implied move: ±35%
- Key bogey: Must show superiority to Eylea on durability
- Street focused on: Q12 vs Q8 dosing benefit

### Fundamental View (ZH/Analyst)
- Analyst PoS: 70%
- Key insight: Baseline characteristics show milder population than MARINA → higher bar
- Differentiated view: Durability is achievable, but magnitude may disappoint

### Integration
- PoS edge: +5% (small)
- Magnitude edge: -10% (street too optimistic on magnitude)
- Net: Small long, but don't chase

### Outcome
Integrated view helped avoid oversized position going into catalyst.

---

## Key Principles

1. **Street expects = current price** - You need to know what's priced in before taking a view
2. **Your view ≠ edge** - Edge is the gap between your view and consensus
3. **Catalyst trades are event-driven** - Different calculus than fundamental positions
4. **Trader + analyst > either alone** - Combining perspectives captures more information
5. **Document before, debrief after** - Learn from every catalyst
