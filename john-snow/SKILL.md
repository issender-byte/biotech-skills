---
name: john-snow
description: "Estimate peak sales given a target product profile (TPP) and competitive set. Named for John Snow - we map the epidemiology to find the market. Use when translating clinical efficacy/safety into commercial potential. Requires TPP assumptions (efficacy, safety, dosing, convenience) and competitive landscape. Does NOT assess clinical PoS or valuation - use reverend-bayes and graham skills for those. Triggers: peak sales, market size, competitive positioning, launch trajectory, pricing, market share, commercial potential."
---

# John Snow: Commercial Peak Sales Assessment

*"First, map the population. Then, find the opportunity."*

**Scope:** Given a TPP, what's the revenue opportunity?

**Required inputs:**
- TPP (efficacy, safety, dosing, convenience)
- Competitive set (approved and pipeline)
- Market size data

**Out of scope:** Clinical PoS → use `reverend-bayes` skill. Valuation → use `graham` skill.

## Output

```
Peak Sales: $[X-Y]B (US) / $[A-B]B (WW)
Key Assumptions: [Market size, share, pricing]
Sensitivity: [What drives to top/bottom of range]
```

## Framework Overview

```
1. MARKET SIZING → TAM/SAM/SOM
2. COMPETITIVE POSITIONING → Share assumptions by segment
3. PRICING & ACCESS → Net price realization
4. LAUNCH TRAJECTORY → Ramp assumptions
5. PEAK SALES → Triangulate across methods
```

## Step 1: Market Sizing

### TAM/SAM/SOM Framework

| Level | Definition | How to Calculate |
|-------|------------|------------------|
| **TAM** | Total addressable market | All patients with condition × price |
| **SAM** | Serviceable addressable market | Patients eligible for this drug class × price |
| **SOM** | Serviceable obtainable market | Realistic capture × price |

### Epidemiology Sources

- Published literature (prevalence, incidence)
- Claims data (diagnosed/treated patients)
- Company guidance (often optimistic)
- KOL interviews (practical adoption)

### Patient Flow

```
Total Prevalence
    ↓ (% diagnosed)
Diagnosed Patients
    ↓ (% treated with any therapy)
Treated Patients
    ↓ (% eligible for drug class)
Class-Eligible Patients
    ↓ (% share for your drug)
Your Patients
    × Price
= Revenue
```

## Step 2: Competitive Positioning

### TPP Comparison Matrix

| Attribute | Your Drug | Comp 1 | Comp 2 | SOC | Weight |
|-----------|-----------|--------|--------|-----|--------|
| Efficacy (primary) | | | | | 30% |
| Efficacy (durability) | | | | | 15% |
| Safety | | | | | 20% |
| Dosing convenience | | | | | 15% |
| Route of admin | | | | | 10% |
| Monitoring burden | | | | | 10% |
| **Weighted Score** | | | | | 100% |

### Share Assumptions by Positioning

| Positioning | Typical Share | Conditions |
|-------------|---------------|------------|
| Best-in-class (clear) | 40-60% of new starts | Differentiated on efficacy + safety |
| Best-in-class (modest) | 25-40% | Differentiated on one dimension |
| Me-too / undifferentiated | 10-25% | Third+ to market, no clear advantage |
| Niche / specific population | 5-15% of total, but higher in niche | Subset of patients benefits |

### The "Third-to-Market" Problem

From CGON/ALMS exchanges:
- **Undifferentiated third-to-market has minimal opportunity**
- "Nobody cared that CYTK was a little bit better"
- Must identify specific dimension of differentiation

### Launch Overhang Analysis

From CGON exchange - if first-mover underwhelms, entire space de-rates:

| Space | First-Mover | Launch | Space Impact |
|-------|-------------|--------|--------------|
| GA | Izervay/Syfovre | Underwhelmed | All GA de-rated |
| AD (amyloid) | Leqembi | Slow | Next-gen lost hype |
| Muscarinics | Cobenfy | Below expectations | Space de-rated |
| TYK2 | Sotyktu | Slow | Competitors lost interest |

**Question:** Is your space at risk of first-mover overhang?

## Step 3: Pricing & Access

### Pricing Methods

| Method | Approach | Best For |
|--------|----------|----------|
| **Cost-plus** | Manufacturing + margin | Generics |
| **Competitive parity** | Match class pricing | Me-too |
| **Value-based** | Efficacy premium over SOC | Differentiated |
| **ICER threshold** | $/QALY calculation | HTA markets |

### Net Price vs. List Price

**Critical from ALMS exchange:**

> "Sotyktu sales were flat y/y despite volume growth of 50-60% which suggests to me they are having net price and access issues."

| Factor | Impact on Net Price |
|--------|---------------------|
| Rebates to PBMs | -20-40% |
| Patient assistance | -5-15% |
| 340B | -15-25% (for eligible) |
| Government pricing | -15-25% |

**Always model NET price, not list price.**

### Price/Volume Decomposition

Before extrapolating revenue trends:
```
Revenue = Price × Volume

If Price ↓ but Volume ↑:
- Revenue may be flat
- But demand is growing
- Forward revenue may accelerate if price stabilizes

If Price ↑ but Volume ↓:
- Revenue may look stable
- But demand is declining
- Forward revenue may decelerate
```

## Step 4: Launch Trajectory

### Typical Launch Curves

| Launch Type | Year 1 | Year 2 | Year 3 | Peak Year |
|-------------|--------|--------|--------|-----------|
| **Strong** | 15-25% of peak | 40-60% | 70-85% | Year 4-5 |
| **Moderate** | 10-15% | 25-40% | 50-65% | Year 5-7 |
| **Slow** | 5-10% | 15-25% | 30-45% | Year 7-10 |

### Launch Success Factors

| Factor | Positive | Negative |
|--------|----------|----------|
| Unmet need | High | Low/crowded |
| Physician familiarity | Known MOA | Novel/education needed |
| Payer access | Broad formulary | Prior auth, step edits |
| Patient identification | Easy diagnosis | Requires biomarker |
| Administration | Oral/self-admin | Infusion/office visit |
| Competition timing | First-mover | Late entrant |

### Real-World Launch Comps

Always benchmark to actual launches in similar settings:
- Same therapeutic area
- Similar competitive dynamics
- Similar access environment

## Step 5: Peak Sales Estimation

### Method 1: Bottom-Up (Patient-Based)

```
Eligible patients × Share × Net price × Compliance = Revenue

Example:
- 500K eligible patients
- 15% share = 75K patients
- $50K net price
- 80% compliance adjustment
= $3B peak
```

### Method 2: Analog-Based

```
Find comparable drug launches:
- Similar indication
- Similar positioning
- Similar competitive environment

Adjust for:
- Market growth since analog launch
- Pricing environment changes
- Your TPP vs. analog TPP
```

### Method 3: Top-Down (Market Share)

```
Total market size × Your share = Revenue

Example:
- $20B market (current)
- Growing 5%/year → $25B at your peak
- 15% share
= $3.75B peak
```

### Triangulation

**Use multiple methods and triangulate:**

| Method | Peak Estimate | Confidence |
|--------|---------------|------------|
| Bottom-up | $X | Medium |
| Analog-based | $Y | High |
| Top-down | $Z | Low |
| **Triangulated** | $[weighted avg] | |

## Deliverable: Peak Sales Assessment

```
═══════════════════════════════════════════════════════════════
COMMERCIAL PEAK SALES ASSESSMENT
Drug: [Name] | Indication: [Indication]
TPP: [Efficacy X%, Safety Y, Dosing Z]
═══════════════════════════════════════════════════════════════

PEAK SALES ESTIMATE: $[X-Y]B (US) / $[A-B]B (WW)
Peak Year: [Year X post-launch]

MARKET SIZING:
│ TAM │ $[X]B │ [All patients × price] │
│ SAM │ $[Y]B │ [Eligible × price] │
│ SOM │ $[Z]B │ [Realistic capture] │

COMPETITIVE POSITIONING:
│ Attribute │ Your Drug │ Best Comp │ Delta │
│ Efficacy │ │ │ │
│ Safety │ │ │ │
│ Convenience │ │ │ │
│ OVERALL │ [Better/Parity/Worse] │

SHARE ASSUMPTIONS:
- New patient share: [X%]
- Switch share: [Y%]
- Peak share of market: [Z%]
- Rationale: [Why this share?]

PRICING:
- List price: $[X]
- Net price: $[Y] ([Z]% discount)
- Price trend: [Stable/Declining/Improving]

LAUNCH TRAJECTORY:
- Year 1: $[X] ([Y]% of peak)
- Year 3: $[X] ([Y]% of peak)
- Peak year: [X]

SENSITIVITY:
- To top of range: [Higher share because...]
- To bottom of range: [Lower share because...]

KEY RISKS:
1. [Risk 1]
2. [Risk 2]

>>> INPUT FROM: reverend-bayes (PoS estimate)
>>> HAND OFF TO: graham (for fair value)
═══════════════════════════════════════════════════════════════
```

---

## Clinical-Commercial Bidirectional Handoff

**Key Insight:** Clinical and commercial analysis are NOT independent sequential steps. They inform each other bidirectionally.

### The Handoff Loop

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   CLINICAL (reverend-bayes)          COMMERCIAL (john-snow)    │
│                                                                 │
│   "What's the probability           "What's the value          │
│    of hitting X bar?"         ←→     conditional on X bar?"    │
│                                                                 │
│         PoS by scenario              Peak sales by scenario    │
│              ↓                              ↓                   │
│                    VALUATION (graham)                          │
│                    EV = Σ (PoS × Value)                        │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Commercial → Clinical: The Clinical Bar

Commercial's job is to tell clinical what efficacy thresholds distinguish commercial scenarios:

```
CLINICAL BAR DEFINITION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

For [Drug] in [Indication]:

| Commercial Scenario | Peak Sales | Required Efficacy Bar |
|---------------------|------------|----------------------|
| Best-in-class | $[X]bn | [Endpoint] ≥[Y]% delta + [differentiation] |
| Me-better | $[X]bn | [Endpoint] [Y-Z]% delta |
| Me-too | $[X]bn | [Endpoint] [Y-Z]% delta, no differentiation |
| Also-ran | $[X]bn | [Endpoint] <[Y]% delta or safety issue |

Secondary differentiation factors:
- Dosing convenience: [What matters?]
- Safety profile: [What matters?]
- Subpopulation labels: [What matters?]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Example (AVTX in HS):**

| Scenario | Peak Sales | HiSCR75 Delta Required |
|----------|------------|------------------------|
| BIC | $2.0bn | ≥25% + faster onset or better safety |
| Me-better | $1.5bn | 20-25%, Q4W convenience |
| Me-too | $750mn | 15-20%, no differentiation vs Luti |
| Also-ran | $250mn | <15% or safety signals |

### Clinical → Commercial: Mechanism Implications

Clinical's job is to tell commercial what the mechanism debate means for competitive positioning:

```
MECHANISM-TO-COMMERCIAL TRANSLATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Mechanism finding: [What the science shows]
Commercial implication: [What it means for scenarios]

Example:
- Finding: IL-1α blockade alone showed signal (bermekimab 60% vs 10%)
- Implication: If IL-1α contributes materially, AVTX (IL-1β only) 
  may be capped at me-too even with good data
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Integration Checkpoint

Before completing analysis, verify:

```
□ Commercial defined clinical bars for each scenario
□ Clinical provided PoS for each bar
□ Mechanism debates mapped to commercial outcomes
□ Uncertainties identified with "what resolves it"
□ Both sides stated a view (even if tentative)
```

---

## Reference Files

| File | Use When |
|------|----------|
| `references/launch-analogs.md` | Finding comparable launches |
| `references/pricing-access.md` | Pricing methodology, payer dynamics |
| `references/bolus-product-commercial.md` | Gene therapy, CAR-T, fixed-course products |
| `references/intraquarter-commercial-tracking.md` | Script tracking, capture rates, persistence |
| `references/product-transition-commercial.md` | SKU discontinuation, forced adoption, device bundling |
| `references/cell-therapy-commercial.md` | **CAR-T, site-of-care dynamics, supply utilization** |
| `references/ta-hidradenitis-suppurativa.md` | HS competitive landscape, IL-1/IL-17 dynamics |
