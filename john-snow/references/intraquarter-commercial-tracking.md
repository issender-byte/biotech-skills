# Intraquarter Commercial Tracking

Framework for using real-time prescription data to inform commercial thesis, calibrate peak sales estimates, and identify variant perception opportunities.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Tracking launch trajectory intraquarter | Yes |
| Sellside projecting miss based on script data | Yes - validate their methodology |
| Calibrating peak sales slope assumptions | Yes |
| Rare disease / specialty pharmacy launch | Yes - capture rates are key |
| Earnings preview with commercial uncertainty | Yes |

---

## Framework 1: Script Data Sources & Limitations

### Data Source Hierarchy

| Source | Description | Capture | Utility |
|--------|-------------|---------|---------|
| **Company PSFs/Active Patients** | Patient start forms, active patient count | 100% (ground truth) | Quarterly only - use to calibrate |
| **Symphony Health** | Claims-based, extrapolated | 10-30% typical | Weekly - directional signal |
| **IQVIA** | Retail pharmacy focused | Variable | Often blocked for specialty |
| **Bloomberg Terminal** | Aggregates Symphony | Same as Symphony | Convenient access |

### Critical Limitation: Specialty Pharmacy Blocking

For rare disease / specialty pharmacy products:
- IQVIA often **blocked** - scripts don't show up
- Symphony shows **paid claims** with extrapolation factor
- Company-reported data (PSFs, active patients) is ground truth
- Must calibrate Symphony to company data quarterly

**Key insight from SLNO:** "Management previously clarified that these are not actual scripts via the specialty distributor, which are blocked and don't show up on IQVIA. These are paid claims captured by Symphony."

---

## Framework 2: Capture Rate Analysis

### What is Capture Rate?

Capture rate = Symphony scripts / Total actual scripts

### Why Capture Rate Matters

For specialty products with 10-30% capture:
- Small changes in capture = large changes in implied revenue
- ±1-2pp capture flex = ±5-10% revenue swing
- Capture rate is the key variable, not raw script counts

### Capture Rate Benchmarks (Rare Disease)

| Product | Indication | Capture Rate | Trend |
|---------|------------|--------------|-------|
| DAWN (Sarepta) | DMD | 11-12% | Stable |
| CPRX (Catalyst) | Congenital myasthenia | 10-13% | Stable |
| BBIO (BioMarin) | Achondroplasia | 29-30% | Stable |
| SLNO (Soleno) | PWS | 18-24% | Wide, early launch |

**Key insight:** Wide capture rate (like SLNO's 6pp range) means high uncertainty. Scenarios should frame as "what capture rate to inline?" not "will they beat?"

### Calibration Methodology

1. Get company-reported PSFs/active patients (quarterly)
2. Compare to Symphony TRx over same period
3. Calculate implied capture rate
4. Track stability over time
5. Apply capture rate to intraquarter Symphony data

---

## Framework 3: Capture Rate Scenario Analysis

### The Question
Instead of "will they beat/miss?", ask "what capture rate is required to inline?"

### Methodology

| Scenario | Capture Rate | Implied Q Revenue | vs Consensus |
|----------|--------------|-------------------|--------------|
| Bear | 24% (Q3 rate) | $72M | -14% |
| Base | 23% (-1pp) | $77M | -8% |
| Bull | 22% (-2pp) | $81M | -4% |
| Inline | 21.5% (-2.5pp) | $84M | Inline |

### Key Questions
1. Is the required capture rate plausible?
2. Has capture been stable or volatile?
3. What drove prior capture changes?

### SLNO Q4 Example
- Q3 capture: ~24%
- Consensus: $84M
- Required for inline: ~21.5% (need -2.5pp improvement)
- Assessment: Capture has ranged 18-24%, so 21.5% is achievable but optimistic

---

## Framework 4: Script Slope to Peak Sales

### The Question
What does current script trajectory imply for peak sales?

### Methodology
Different slope assumptions lead to dramatically different peaks:

| Slope Period | Implied US Peak | Logic |
|--------------|-----------------|-------|
| May launch slope | $800M | Early enthusiasm continues |
| August slope | $575M | Recent deceleration persists |
| December slope | ~$450M | Conservative |

### Peak Sales Drivers

Peak Sales = New Starts × Persistence × Net Price

| Variable | What Drives It | How to Track |
|----------|---------------|--------------|
| New Starts | Script slope, market penetration | NRx weekly |
| Persistence | How long patients stay on | TRx/NRx ratio over time |
| Net Price | WAC minus rebates | Quarterly revenue ÷ scripts |

---

## Framework 5: Persistence Curve Analogs

### Why Persistence Matters
Persistence is often the largest driver of peak sales variance.

### Persistence Archetypes

| Archetype | Shape | Peak Timing | Example |
|-----------|-------|-------------|---------|
| Long tail | Gradual erosion | Year 4-5 | Effective chronic therapy |
| Early bolus, sustained | Front-loaded, stable base | Year 2-3 | Rare disease w/ pent-up |
| Early peak, rapid decay | Bolus then dropout | Year 1-2 | Low efficacy, tolerability |

### SLNO Persistence Scenarios

| Assumption | Analog | Implied US Peak |
|------------|--------|-----------------|
| Long tail (hybrid) | Imcivree + Daybue | $940M |
| Traditional 39-week | ACAD Skyclarys | $450M |
| Management guidance | "Less intense than Daybue" | $600-800M |

**Key insight:** "We have seen low efficacy rare disease products effectively peak 1 yr into launch despite being a theoretically chronic treatment despite lack of alternatives like Reata's Skyclarys."

### Persistence Warning Signs

| Signal | Interpretation | Peak Impact |
|--------|----------------|-------------|
| NRx growing faster than TRx | Patients churning | Bearish |
| Repeat Rx % increasing | Persistence improving | Bullish |
| Dose consolidation | Patients stabilizing | Neutral to bullish |
| Early bolus flattening fast | Pent-up exhausted | Bearish for slope |

---

## Framework 6: Sellside Script Tracker Critique

### Common Sellside Errors

| Error | Description | How to Exploit |
|-------|-------------|----------------|
| **Static capture assumption** | Assume capture = last quarter | Capture improves as launch matures |
| **Ignore dosing dynamics** | Script decline = revenue decline | Dose consolidation ≠ patient loss |
| **Mechanically project weekly** | Linear extrapolation | Miss dosing cycles (4-week fills) |
| **Ignore seasonality** | Holiday week = structural change | Christmas/New Year distorts |

### SLNO vs Sellside Example

**TD Cowen projection:** $72M [$63-81M] vs $84M consensus = -14% miss at midpoint

**Critique of sellside methodology:**
1. "Script only tracker is inherently punitive" - ignores dose/script increase
2. "Weak week aligned with 4 weeks prior" - monthly fill cadence, expect bounce
3. Holiday seasonality not structural
4. Capture can flex 1-2pp to close the gap

**Variant perception:** Sellside mechanically projecting miss, but assumptions may be flawed.

---

## Framework 7: Dosing Cycle Patterns

### The Question
Are weekly script fluctuations signal or noise?

### 4-Week Fill Cadence
Most chronic therapies have 28-30 day supply:
- Week 1 post-fill: Low refills
- Week 4: Refill wave
- Pattern repeats monthly

### Holiday Distortion
Christmas/New Year weeks typically show:
- Reduced patient starts (offices closed)
- Delayed refills
- NOT structural decline

### Validation Check
If weak week aligns with 4 weeks prior (also weak), likely cadence effect, not structural.

---

## Framework 8: Street Focus Analysis

### The Question
What metric is the street focused on? Beat/miss on wrong metric doesn't move stock.

### Metrics That Move Stock

| Launch Stage | Primary Focus | Secondary |
|--------------|---------------|-----------|
| Launch Q1-Q2 | New starts trajectory | Any revenue |
| Year 1 | Revenue vs consensus | New starts |
| Year 2+ | Persistence/durability | Peak sales revision |

### SLNO Key Question
> "What is the street focused on for SLNO – purely sales, new start trajectory, or persistence commentary?"

This determines what data point moves the stock, not just whether they beat/miss.

---

## Integrated Checklist: Intraquarter Commercial Analysis

```
INTRAQUARTER COMMERCIAL ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

DATA VALIDATION:
□ Symphony capture rate calibrated to company data? [ ] Yes [ ] No
□ Capture rate stability: [ ] Tight (±2pp) [ ] Moderate (±4pp) [ ] Wide (±6pp+)
□ Current capture rate: _____%
□ Capture rate required for inline: _____%

SCRIPT TRAJECTORY:
□ Weekly TRx trend: [ ] Accelerating [ ] Flat [ ] Declining
□ Weekly NRx trend: [ ] Accelerating [ ] Flat [ ] Declining
□ TRx/NRx ratio trend: [ ] Improving [ ] Stable [ ] Deteriorating
□ Dosing cycle accounted for? [ ] Yes [ ] No

SELLSIDE CRITIQUE:
□ Sellside methodology reviewed? [ ] Yes [ ] No
□ Errors identified: _____________________
□ Variant perception opportunity? [ ] Yes [ ] No

PEAK SALES IMPLICATIONS:
□ Persistence analog named: _____________________
□ Slope scenario: [ ] Bull ($___M) [ ] Base ($___M) [ ] Bear ($___M)
□ Street focus: [ ] Sales [ ] New starts [ ] Persistence [ ] Other

CONCLUSION:
□ Beat/miss likely: [ ] Beat [ ] Inline [ ] Miss
□ Stock reaction expected: _____________________
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Case Study: SLNO Vykat XR (Q4 2025)

### Background
- **Drug:** Vykat XR (diazoxide choline) for Prader-Willi Syndrome
- **Launch:** Mid-April 2025
- **Data source:** Symphony via Bloomberg
- **Capture rate:** 18-24% (wide, early launch)
- **Consensus Q4:** $84M
- **FY consensus:** $183M

### Script Data (Week ending 12/19/25)

| Metric | Value | Context |
|--------|-------|---------|
| Weekly TRx | 30 | Down from 47 two weeks prior |
| Weekly NRx | 17 | Solid new starts |
| YTD TRx | 1,134 | Since mid-April launch |
| YTD NRx | 590 | Unique patients |
| Q4 TRx projection | 595 | +22% QoQ vs Q3 |

### Sellside View (TD Cowen)
- Projecting $72M [$63-81M] vs $84M consensus
- Based on script regression with 1.02 TRx/week slope
- Acknowledging capture likely under-represents actual scripts

### Internal Analysis

**Key debates:**

1. **Capture rate flex:**
   - 24% (Q3) → 23% = inline at $81M scenario
   - 24% → 22% = inline at $77M scenario
   - Both reasonable given historical flex

2. **Dosing cycle:**
   - Weak week aligns with 4 weeks prior (monthly fill pattern)
   - Expect bounce next week if pattern holds
   - Holiday (Christmas) adds noise

3. **Peak sales implications:**
   - May slope: $800M US peak
   - August slope: $575M US peak
   - Persistence: $450M (Skyclarys) to $940M (Imcivree hybrid)

### Decision Framework

| Signal | Bullish | Bearish |
|--------|---------|---------|
| Scripts bounce next week | ✅ | |
| Scripts stay flat | | ⚠️ |
| Repeat Rx % increasing | ✅ | |
| NRx decelerating | | ⚠️ |
| Capture tightening | ✅ | |

---

## Key Principles

1. **Capture rate is the key variable** for low-capture products - not script counts
2. **Scenario frame as "capture to inline"** - what do you need to believe?
3. **Understand dosing dynamics** - script decline ≠ patient/revenue decline
4. **Name your persistence analog** - this drives peak sales more than anything
5. **Sellside can be mechanically wrong** - exploit their static assumptions
6. **Connect intraquarter to peak** - script slope informs long-term trajectory
7. **Ask what street is focused on** - beat/miss on the wrong metric doesn't move stock
