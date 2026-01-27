# Pulmonary Arterial Hypertension (PAH) Trial Assessment

Framework for evaluating PAH clinical trials, with focus on 6MWD endpoints, PVR-6MWD correlations, and subgroup analysis skepticism.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| PAH trial with 6MWD endpoint | Yes |
| Claims of biomarker enrichment improving effect size | Yes |
| Subgroup analysis from failed Phase 2 | Yes |
| Novel PAH mechanism with systemic vs local effects | Yes |
| Comparing inhaled vs systemic TKIs in PAH | Yes |

---

## Framework 1: PVR-to-6MWD Regression Sanity Check

### The Question
Does the claimed 6MWD benefit make sense given the observed PVR reduction?

### FDA Published Regression
From FDA review of Tracleer (pooled data from 12 RCTs, 9 approved PAH drugs):

```
Slope: -0.055 m per dyne·sec/cm⁵
Interpretation: Every 1 dyne·sec/cm⁵ PVR reduction → 0.055m 6MWD improvement
```

### Using the Regression

| Your Trial's PVR Delta | Predicted 6MWD | If Claimed 6MWD >> Predicted |
|------------------------|----------------|------------------------------|
| 50 dynes·sec/cm⁵ | ~2.7m | Overstated |
| 100 dynes·sec/cm⁵ | ~5.5m | Overstated if claiming >15m |
| 166 dynes·sec/cm⁵ | ~9m | Overstated if claiming >20m |
| 200 dynes·sec/cm⁵ | ~11m | Overstated if claiming >25m |

### GOSS Example
> "If we plug in GOSS's class 3 spread of ~166 dynes·sec/cm⁵, that would point to ~7-9m delta on 6MWD which is not clinically meaningful."

GOSS claimed 34m in subgroup but PVR regression predicts only ~9m. **5x overstated.**

### Source
FDA Tracleer review: https://www.accessdata.fda.gov/drugsatfda_docs/nda/2017/209279Orig1s000MedR.pdf

---

## Framework 2: Cardiac Output as Efficacy Constraint

### The Question
Does the mechanism allow for meaningful cardiac output (CO) improvement?

### Why CO Matters
Imatinib's 6MWD benefit was largely driven by CO improvement. Newer PAH drugs with minimal systemic exposure (e.g., inhaled TKIs) may not achieve meaningful CO benefit, limiting 6MWD improvement potential.

### CO-6MWD Correlation
From historical imatinib trials and GOSS Ph2:

| Baseline CO | Expected 6MWD Delta | Notes |
|-------------|---------------------|-------|
| <4.0 L/min | 20-25m potential | Sicker patients, room to improve |
| 4.0-4.5 L/min | 15-20m potential | Moderate |
| 4.5-5.0 L/min | 10-15m potential | Less sick, less room |
| >5.0 L/min | <10m potential | Near-normal CO, limited upside |

### GOSS Example
> "We know that imatinib works mostly by improving CO. If they end up with 4.5 in ph3, the predicted 6MWT is ~15m."

GOSS Ph2 baseline CO was ~5. Ph3 enriched for FC III patients (74% vs 48%) but this may not change baseline CO enough to improve effect size.

---

## Framework 3: Subgroup Analysis Skepticism from Failed Ph2

### The Question
When a Phase 2 fails in all-comers but shows effect in a subgroup, how reliable is the subgroup?

### Red Flags for Subgroup-Driven Powering

| Red Flag | Why It's Concerning |
|----------|---------------------|
| Post-hoc analysis | Not pre-specified; high multiple testing risk |
| Small n in subgroup | High variance; effect may be noise |
| Effect driven by placebo worsening | Placebo can vary by chance; not drug effect |
| Complementary subgroup shows "harm" | Sign of noise; treatment shouldn't hurt patients |
| OLE doesn't replicate subgroup effect | If switch-over patients show smaller effect, subgroup was noise |
| Active arm performance similar across subgroups | Delta driven by placebo, not drug |

### The GOSS Pattern

**All-Comers Result:** Failed Phase 2b
**Subgroup Claim:** FC III or REVEAL Lite 2 ≥5 showed 37m 6MWD improvement

**Why It's Suspect:**

1. **Effect driven by placebo worsening:**
> "The 6MWD improvement of 37m in the pts with elevated risk was in part driven by pbo pts showing worsening of 6MWD (-11m)."

2. **Complementary subgroup shows "harm":**
> "This subgroup analysis suggests that pbo treated low risk pts can actually see 35m 6MWD benefit vs the treatment (suggesting the tx is actually doing harm)."

3. **Active arm PVR similar across subgroups:**
> "If we isolate the active arms in the GOSS trial, the active arm performance on PVR is minimal between the positive subgroup and the all-comers population."

4. **OLE doesn't replicate:**
> "Their own Ph2b OLE data does not support their effect size assumption of 30m because the high risk pbo pts switched to active drug treatment during the OLE phase only saw an improvement of 21m in an open-label setting with 2X of follow-up time."

### OLE Reality Check Formula

```
Subgroup Claimed Effect: X meters
OLE Switch-Over Effect: Y meters (with 2× follow-up)
Adjusted OLE Effect: Y - (~4m for extra follow-up) = Z meters
Open-Label Inflation: Assume 30-50% inflation
True Effect Estimate: Z × 0.6-0.7 = True meters

If True << Subgroup Claimed → Subgroup was noise
```

---

## Framework 4: Competitor Read-Through

### The Question
Did a similar mechanism fail despite similar biomarker effect?

### AVTE-GOSS Comparison

| Metric | AVTE High Dose | GOSS All-Comers |
|--------|----------------|-----------------|
| Mechanism | Inhaled TKI (PDGFR) | Inhaled TKI (PDGFR, c-KIT, CSF1R) |
| PVR spread vs pbo | ~55 dynes·sec/cm⁵ | ~66 dynes·sec/cm⁵ |
| 6MWD benefit | Minimal | Minimal |
| mPAP change (active) | -1.6 mmHg | Similar |
| CO benefit | Minimal | Minimal |
| Outcome | **Discontinued** | Running Ph3 in subgroup |

### Key Insight
> "The fact AVTE discontinued their program completely despite showing similar PVR reduction in the active arm to GOSS all-comers implies to me they likely didn't see any signals of efficacy in any subgroup."

---

## Framework 5: Power Calculation for Stats Sig vs Street Bar

### The Question
What's the probability of hitting statistical significance vs the clinically meaningful threshold?

### Two Bars in PAH

| Bar | Definition |
|-----|------------|
| Statistical significance | p < 0.05 on primary endpoint |
| Street bar / commercial bar | Effect size that supports peak sales thesis |

### GOSS Example

| Scenario | Effect Size | Power for Stats Sig | Power for ≥20m |
|----------|-------------|---------------------|----------------|
| Bull case | 20-25m | 80-90% | 50-75% |
| Base case | 16-17m | 50-75% | 30-40% |
| Bear case | 11-13m | 20-40% | <20% |

**Key Insight:** Stats sig but miss street bar = stock DOWN

---

## Framework 6: Historical Placebo Performance in PAH

### Placebo Performance by Functional Class

| FC | Expected Placebo 6MWD Change | Notes |
|----|------------------------------|-------|
| FC II | +5m to -5m | More stable |
| FC III | -10m to -15m | Sicker, decline expected |
| FC IV | -15m to -25m | Rapid decline |

---

## PAH Historical Benchmarks

### Approved PAH Drugs - Pivotal Trial Results

| Drug | Trial | 6MWD Delta vs Pbo | PVR Delta | Approval |
|------|-------|-------------------|-----------|----------|
| Tyvaso (inhaled) | TRIUMPH | +19m | Modest | Yes |
| Sotatercept | STELLAR | +40m | -235 dynes | Yes |
| Imatinib | IMPRES | +32m | -379 dynes | No (safety) |
| Selexipag | GRIPHON | +12m (at 26 wks) | — | Yes (TTE) |

### What Constitutes Clinically Meaningful

| Effect Size | Interpretation | Commercial Implication |
|-------------|----------------|------------------------|
| <10m | Not clinically meaningful | No approval or minimal market |
| 10-15m | Borderline | Approval possible, limited uptake |
| 15-20m | Clinically meaningful | Standard approval path |
| >20m | Strongly meaningful | Premium positioning possible |

---

## Integrated Checklist: PAH Trial Assessment

```
PAH TRIAL ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

BIOMARKER SANITY CHECK:
□ PVR reduction: _____ dynes
□ Expected 6MWD (PVR × 0.055): _____ meters
□ Claimed/powered 6MWD: _____ meters
□ Gap ratio: _____x (>2x = red flag)

SUBGROUP ANALYSIS (if applicable):
□ Was subgroup pre-specified? [ ] Yes [ ] No
□ Effect driver: [ ] Active improvement [ ] Placebo worsening
□ Complementary population: [ ] Neutral [ ] Harmed
□ OLE consistent with subgroup? [ ] Yes [ ] No

COMPETITOR READ-THROUGH:
□ Similar mechanism discontinued? [ ] Yes [ ] No
□ If yes, what was their biomarker effect? _____
□ Enrichment strategy credible? [ ] Yes [ ] No

POWER ANALYSIS:
□ Power for stats sig: _____%
□ Power for street bar: _____%
□ Gap: _____% (>20% gap = "win but lose" risk)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Case Study: GOSS Seralutinib Ph3

### Company Profile
- Ticker: GOSS
- Market Cap: ~$877M
- Net Cash: -$23M (negative)
- EV: ~$900M

### Trial Setup
- Drug: Seralutinib (inhaled TKI, PDGFR/c-KIT/CSF1R)
- Population: Enriched for FC III or REVEAL Lite 2 ≥5
- Primary Endpoint: 6MWD at 24 weeks
- Powering Assumption: 30m effect size from subgroup

### Bear Thesis Summary

**1. Flawed Powering Assumptions**
- Post-hoc subgroup from failed Ph2b
- Effect driven by placebo worsening, not active improvement
- OLE switch-over data shows only 21m (vs 34m claimed)

**2. Mechanistic Concerns**
- Inhaled delivery = low systemic exposure
- Minimal CO benefit expected
- PVR → 6MWD regression predicts only ~9m

**3. Competitive Read-Through**
- AVTE discontinued with similar PVR effect
- Overlapping mechanism suggests limitation

### PoS Estimates

| Analyst | PoS for Stats Sig | PoS for ≥20m |
|---------|-------------------|--------------|
| Leo | 50-75% | 30-55% |
| RP | 25-40% | <25% |
| Alex | 40% | — |

### Position Recommendation
> "GOSS – Discuss 25bps short inline and add to 50bps if stock gets to $4 before the Ph3 PAH data in February."

---

## Key Principles for PAH Trials

1. **PVR → 6MWD regression is your sanity check** - use FDA published slopes
2. **Baseline CO constrains effect size** - drugs without systemic exposure have limited 6MWD potential
3. **Subgroup from failed Ph2 is high risk** - especially if effect driven by placebo worsening
4. **OLE switch-over is reality check** - if OLE effect << subgroup claim, subgroup was noise
5. **Competitor discontinuation is bearish** - especially with overlapping mechanism
6. **Stats sig ≠ commercial success** - model both thresholds
