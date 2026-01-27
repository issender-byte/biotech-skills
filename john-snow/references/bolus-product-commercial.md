# Bolus Product Commercial Analysis

Framework for analyzing fixed-course therapies (gene therapies, surgical adjuncts) where revenue is one-time per patient rather than recurring.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Gene therapy launch | Yes |
| Fixed-course therapy | Yes |
| Surgical adjunct products | Yes |
| CAR-T or cell therapy | Yes |
| Chronic maintenance therapy | No - use standard models |

---

## Framework 1: Claims Data TAM Waterfall

### The Problem
Company guidance inflates TAM. Claims data reveals truth.

### Methodology
Build a waterfall from broad to narrow:

```
ICD-10 Code (broad diagnosis)
    ↓ Filter: Age/demographics per label
    ↓ Filter: Procedure codes (actually getting treatment)
    ↓ Filter: Multi-year procedures (recurring need)
    ↓ Filter: Already seeking treatment (current demand)
    = Addressable Market
```

### PGEN Example (RRP - Recurrent Respiratory Papillomatosis)

| Filter | Patients | Logic |
|--------|----------|-------|
| ICD10 D14.1 (larynx neoplasm) | 24,466 | Broad universe |
| Adults only | 23,776 | Label restriction |
| + Surgery 2025 | 3,437 | Actually getting debulked |
| + Surgery 2024 AND 2025 | **697** | **Ceiling** (recurring burden) |
| On Avastin 2025 | **398** | **Floor** (already seeking Rx) |

**Key insight:** 697 ceiling / 398 floor brackets the opportunity. Company guidance often inflates.

### Capture Rate Adjustment
- IQVIA captures ~59% of specialty scripts
- Adjust claims data accordingly
- PGEN: 697 ÷ 0.59 = ~1,180 true ceiling

---

## Framework 2: Ceiling/Floor Bracketing

### The Question
What are the bounds on market opportunity?

### Methodology
| Bound | Definition | How to Find |
|-------|------------|-------------|
| **Ceiling** | Maximum addressable patients | Multi-year procedure overlap |
| **Floor** | Minimum interested patients | Currently on alternative Rx |

### Interpretation
- Bull case: Approach ceiling
- Base case: Between floor and ceiling
- Bear case: At or below floor

### PGEN Example
- Ceiling: 697 patients (recurring surgical burden)
- Floor: 398 patients (on Avastin)
- At $460K/course: $183M (floor) to $321M (ceiling) one-time
- **Not a franchise** - depleting TAM

---

## Framework 3: PSF-First Tracking

### The Question
For bolus products, how do we track commercial trajectory?

### Methodology
**PSFs (Patient Start Forms) are the leading indicator. Revenue is lagging confirmation.**

```
PSF Submitted → Insurance Verification → PA Approval → Dosing → Revenue Recognition
     |                                                              |
     +-------------- 8-12 week lag typical -------------------------+
```

### Tracking Template

| Date | PSFs Cumulative | Implied PSFs/Week | Trend |
|------|-----------------|-------------------|-------|
| Launch | 0 | — | — |
| Week 4 | X | X/4 | Baseline |
| Week 8 | Y | (Y-X)/4 | Accelerating/Decelerating |

### Scenario Modeling
| Scenario | PSF Trajectory | Logic |
|----------|----------------|-------|
| Bull | +2/week every 10 weeks | KOL adoption spreads |
| Base | Flat at launch rate | Initial enthusiasm, no expansion |
| Bear | Decline 50% | Funnel breakdown |

### PGEN Example
| Timepoint | PSFs | Implied Rate |
|-----------|------|--------------|
| 11/13/25 (EPS PR) | >100 | ~10/week |
| 1/12/26 (JPM PR) | >200 | ~12/week |

Flat to slight acceleration - but conversion to dosing is the real test.

---

## Framework 4: KOL Dosing Validation

### The Question
Are KOLs actually dosing patients, or just submitting PSFs?

### Why This Matters
PSFs ≠ treated patients. The funnel can break at multiple points:
- Insurance denial
- Patient hesitation
- KOL skepticism after initial PSF
- PA requirements too onerous

### Methodology
Interview KOLs directly. Ask:
1. How many patients have you submitted PSFs for?
2. How many have you actually dosed?
3. Why the gap (if any)?
4. What's your dosing rate going forward?

### PGEN KOL Validation (Devastating)

| KOL | Institution | Volume | Dosed | Key Quote |
|-----|-------------|--------|-------|-----------|
| Best | Hopkins | 35-40 PSFs | **0** | "If you care about efficacy, you don't understand medicine" |
| Rosen | UCSF | ~10 PSFs | **0** | "Very hard to assess placebo response" |
| Gao | UChicago | ~3 PSFs | **0** | "Avastin allows many pts to have no re-growth" |
| Merati | UW | 5-10 PSFs | **0** | "Avastin works amazingly well" |
| Cohen | Duke | 0 | **0** | "Not truly randomized...not sure it proved efficacy" |

**5 KOLs, combined ~340 RRP patients treated, ZERO dosed with Papzimeos.**

---

## Framework 5: Off-Label Competition Analysis

### The Question
How effective is the existing off-label standard-of-care?

### Why This Matters
If off-label therapy already "works amazingly well" (per KOL quote), the unmet need is much narrower than company claims.

### Assessment Template

| Factor | Favorable to New Drug | Favorable to Off-Label |
|--------|----------------------|------------------------|
| Efficacy | Superior data | "Good enough" |
| Safety | Safer profile | Known, tolerable |
| Cost | — | Much cheaper |
| Convenience | One-time | Chronic but familiar |
| KOL comfort | Novel, exciting | Established |

### PGEN vs Avastin

| Factor | PGEN | Avastin |
|--------|------|---------|
| Efficacy | "Gene therapy" | "Works amazingly well" |
| Safety | Unknown long-term | Known |
| Cost | $460K | $5-10K |
| Convenience | One-time (if works) | Chronic |
| KOL comfort | Untested | 10+ years experience |

---

## Framework 6: Re-Dosing Skepticism

### The Question
For gene therapies, can patients be re-dosed?

### Default: Skepticism
For viral vector products:
- Neutralizing antibodies to capsid proteins develop
- May clear vector on re-dose
- Require specific re-dosing data, not assumptions

### Assessment
| Evidence | Confidence |
|----------|------------|
| Re-dosing study positive | High |
| Mechanism suggests possible | Moderate |
| No data, assumes works | Low - skepticism warranted |

---

## Framework 7: TAM Depletion Dynamics

### Bolus Products Deplete Their TAM

Unlike chronic therapies that replenish via incidence, bolus products deplete via treatment:

```
Year 1: Treat prevalent pool (large bolus)
Year 2: Treat new diagnoses only + untreated prevalent (smaller)
Year 3: Primarily incident cases (much smaller)
Year 4+: Steady-state incident (maintenance level)
```

### Peak Sales Timing

| Product Type | Peak Year | Shape |
|--------------|-----------|-------|
| Chronic therapy | Year 4-7 | Gradual climb, plateau |
| Bolus product | Year 1-2 | Spike, then decline |

**Implication:** Bolus products have "peak sales" in the traditional sense, but then sales decline as prevalent pool is treated.

---

## Framework 8: Trial Design Red Flags

### Mandatory Pre-Treatment Intervention
If trial requires surgery/procedure BEFORE dosing:
- Cannot separate drug effect from intervention effect
- Example: PGEN required debulking before dose 1

### Single-Center Generalizability
Elite academic centers (NIH, MGH) have:
- Best surgeons
- Most intensive follow-up
- Highly selected patients
- Results may not replicate in community

### Subjective Endpoints
"Clinically indicated" surgery is subjective:
- Physician judgment varies
- Expectation bias affects threshold
- Placebo groups may be watched more closely

---

## Integrated Checklist: Bolus Product Assessment

```
BOLUS PRODUCT COMMERCIAL ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TAM ANALYSIS:
□ Claims data waterfall completed? [ ] Yes [ ] No
□ Ceiling (max addressable): _____ patients
□ Floor (current demand): _____ patients
□ Capture rate adjustment applied? [ ] Yes [ ] No
□ One-time revenue at ceiling: $_____

PSF TRACKING:
□ Current PSF count: _____
□ PSFs per week: _____
□ Trajectory: [ ] Accelerating [ ] Flat [ ] Declining
□ PSF-to-dose conversion rate: _____%

KOL VALIDATION:
□ # of KOLs contacted: _____
□ # who have dosed patients: _____
□ KOL concentration risk? [ ] Yes [ ] No
□ Top KOL % of PSFs: _____%

OFF-LABEL COMPETITION:
□ Effective off-label exists? [ ] Yes [ ] No
□ Cost differential: $_____
□ KOL preference: [ ] New drug [ ] Off-label [ ] Mixed

TRIAL DESIGN:
□ Mandatory intervention confound? [ ] Yes [ ] No
□ Single-center generalizability risk? [ ] Yes [ ] No
□ Subjective endpoint? [ ] Yes [ ] No

RE-DOSING (if applicable):
□ Re-dosing data exists? [ ] Yes [ ] No
□ Mechanism supports re-dosing? [ ] Yes [ ] No [ ] Unknown

OVERALL:
□ Peak sales estimate: $_____
□ Time to peak: _____ years
□ TAM depletion rate: _____% per year
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Case Study: PGEN Papzimeos

**Setup:** Short 50bps above $4.00

**TAM Analysis:**
- Claims waterfall: 24K → 23K → 3.4K → 697 ceiling / 398 floor
- At $460K: $183M-$321M one-time opportunity
- Not a franchise - TAM depletes

**PSF Tracking:**
- >100 PSFs by 11/13/25
- >200 PSFs by 1/12/26
- ~12/week rate, flat to slight acceleration
- BUT: Zero doses by top KOLs

**KOL Validation (Devastating):**
- 5 KOLs interviewed
- Combined ~340 RRP patients treated
- **Zero patients dosed with Papzimeos**
- Best (Hopkins) = 35-40% of PSFs, zero doses

**Off-Label Competition:**
- Avastin "works amazingly well" per KOLs
- $5-10K vs $460K
- Established comfort

**Trial Confounds:**
- Mandatory surgery before dosing
- Cannot separate drug from intervention effect
- Single-center (NIH) generalizability questions

**Recommendation:** Short. PSFs are vanity metric; KOL dosing is the real signal, and it's zero.

---

## Key Principles

1. **Use claims data waterfall, not company guidance** - ICD10 → procedure codes → multi-year overlap
2. **Bracket with ceiling and floor** - max eligible vs min already seeking treatment
3. **Track PSFs, not revenue** - for bolus products, PSFs are leading indicator
4. **Validate KOL dosing, not just PSFs** - funnel is broken if KOLs haven't dosed
5. **Understand the off-label incumbent** - if Avastin "works amazingly well," unmet need is narrower
6. **Assume re-dosing doesn't work** - for viral vectors, NAbs are real
7. **Expect PA alignment with trial criteria** - expensive therapies face stringent access
8. **Model TAM depletion** - bolus products don't build franchises
