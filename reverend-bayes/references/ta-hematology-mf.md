# Therapeutic Area Reference: Hematology — Myelofibrosis (MF)

Clinical benchmarks and analytical frameworks for evaluating MF trials.

---

## EPIDEMIOLOGY

### US Prevalence
| Metric | Value | Source |
|--------|-------|--------|
| MF prevalence | ~16,000-18,500 | Registry estimates |
| Annual incidence | ~3,000 | SEER |
| Median age at diagnosis | ~65 years | Registry |
| Median survival (untreated) | 3.5-5.5 years | DIPSS-dependent |

### Risk Stratification (DIPSS)
| Risk Category | % of Patients | Median Survival |
|---------------|---------------|-----------------|
| Low | ~10% | >10 years |
| Intermediate-1 | ~30% | ~7 years |
| Intermediate-2 | ~35% | ~4 years |
| High | ~25% | ~2 years |

---

## CLINICAL ENDPOINTS & BENCHMARKS

### Total Symptom Score (TSS) / MF-SAF

**Components (7 domains, 10 points each = 70 points max):**
1. Fatigue
2. Night sweats
3. Itching (pruritus)
4. Abdominal discomfort
5. Pain under ribs (left side)
6. Early satiety
7. Bone/muscle pain

**Key insight:** Only 3/7 domains are spleen-related (4-6). Systemic symptoms (1-3, 7) driven by proinflammatory cytokines, not spleen size.

### Scale Versions
| Version | Max Score | Trials Using |
|---------|-----------|--------------|
| MF-SAF TSS (full) | 70 points | MANIFEST-2, TRANSFORM-1 |
| TSS ex-Fatigue | 60 points | KPTI Ph3, Jakafi approval |

**Rescaling formula:** 60pt result × (70/60) = 70pt equivalent

### Responder Definitions
| Endpoint | Definition | Notes |
|----------|------------|-------|
| TSS50 | ≥50% reduction from baseline | Binary, loses granularity |
| TSS CFB | Mean/median change from baseline | Continuous, more power |
| SVR35 | ≥35% spleen volume reduction | MRI-based |

### Historical Benchmarks - Rux Monotherapy

| Trial | Baseline TSS | TSS CFB | % CFB |
|-------|--------------|---------|-------|
| COMFORT-I | ~18 | ~-9 | -50% |
| COMFORT-II | ~18 | ~-8.5 | -47% |
| MANIFEST-2 (rux arm) | ~25 | ~-11 | -44% |
| TRANSFORM-1 (rux arm) | ~28 | ~-13 | -46% |

**Critical insight:** Rux % CFB is remarkably consistent at -45-50% regardless of baseline. Absolute CFB varies with baseline severity.

### Combination Trial Benchmarks

| Trial | Drug + Rux | N | TSS50 | TSS CFB | SVR35 |
|-------|------------|---|-------|---------|-------|
| MANIFEST-2 | Pelabresib | ~215 | 52% | -13.5 (-57%) | 66% |
| MANIFEST-2 | Rux mono | ~215 | 46% | -11.3 (-51%) | 35% |
| TRANSFORM-1 | Navitoclax | ~125 | 55% | -14.2 | 63% |
| TRANSFORM-1 | Rux mono | ~125 | 48% | -12.5 | 32% |

**Key finding:** Strong SVR benefit (~30% delta) does NOT translate to proportional TSS benefit (~6% TSS50 delta).

---

## ANALYTICAL FRAMEWORKS

### Framework 1: % CFB Normalization

**Problem:** Absolute CFB is confounded by baseline severity.

**Solution:** Convert to % CFB for valid comparison.

**Example (CNST MANIFEST-2):**
- Pela+rux: -13.5 pts / 25 baseline = -54% CFB
- Rux mono: -11.3 pts / 25 baseline = -45% CFB
- Delta: -9% (not the -2.2 pt absolute)
- Normalized to typical baseline 22.5: 9% × 22.5 = **2.0 pts real effect**

### Framework 2: Dropout-Adjusted ITT Analysis

**Problem:** High dropout rates can inflate PP efficacy.

**Method:**
1. Count completers vs dropouts
2. Assume 0 improvement for dropouts (worst case)
3. Recalculate ITT effect

**Example (KPTI Ph1):**
- Treated: 14 patients
- TSS data reported: 9 patients (36% missing)
- CNST Ph1b: 80/82 patients (2% missing)

| Analysis | KPTI TSS CFB | Interpretation |
|----------|--------------|----------------|
| PP (n=9) | -68% | Best case |
| ITT (assume 0 for 5) | -44% | Worst case |
| Midpoint | -56% | Realistic |

**Conclusion:** KPTI's -68% PP shrinks to ~-56% ITT, similar to CNST's -57%.

### Framework 3: Endpoint Component Removal Impact

**Question:** Does removing fatigue from TSS meaningfully change the result?

**CNST Sensitivity Analysis (from CT.gov):**

| Endpoint | Pela+Rux | Rux Mono | Delta |
|----------|----------|----------|-------|
| TSS50 (full) | 52% | 46% | +6% |
| TSS50 (ex-fatigue) | 56% | 48% | +8% |

**Key insight:** Removing fatigue only adds ~2% to the spread. Both arms improve because both cause fatigue.

### Framework 4: Dose Reduction Impact on Efficacy

**Problem:** High dose reductions of backbone therapy undermine combination efficacy.

**KPTI Ph1 Data:**
- 4-5 of 9 patients dose-reduced rux to 5mg (minimum approved dose)
- Patients started at 15-20mg
- ~50% of patients on suboptimal backbone

**Implication:** If half the patients are effectively on seli monotherapy vs rux monotherapy, combination can't show benefit over mono.

**Generalized rule:** If >30% of patients dose-reduce backbone to subtherapeutic levels, the combination thesis is compromised.

### Framework 5: SD Reasonableness Check

**Red flag:** SD approximately equal to mean CFB

**KPTI Ph1 Data:**
- CFB: -18.5 pts
- Baseline: 27 pts (so -68%)
- SD: 14 pts
- n: 9

**Problem:** For SD ≈ mean to occur in n=9, data would need to be implausibly uniform or bimodal.

**Expectation:** In MF trials, SD is typically 40-60% of baseline, not 50% of CFB.

### Framework 6: Biomarker Ceiling Effect

**Question:** Does more spleen reduction = more symptom improvement?

**Jakafi Data:**
| SVR Category | TSS Improvement |
|--------------|-----------------|
| 10% SVR | ~-40% TSS |
| 35% SVR | ~-45% TSS |
| 50% SVR | ~-48% TSS |

**Key insight:** Diminishing returns beyond ~10% SVR. A drug that achieves 65% SVR35 vs 35% SVR35 will NOT show proportional TSS benefit.

**Implication for combination trials:** Strong SVR delta (pela/navitoclax both showed ~30% SVR35 advantage) translates to modest TSS delta (~6% TSS50) because TSS benefit plateaus.

---

## CASE STUDY: KPTI Selinexor + Rux Ph3

### Bull Case Summary

| Argument | Supporting Evidence | Strength |
|----------|---------------------|----------|
| Ph1 data look BIC | SVR35, TSS50, CFB similar/better than CNST | Medium |
| CNST Ph1→Ph3 translated | MANIFEST-2 Ph3 generally held Ph1b efficacy | Strong |
| TSS CFB > TSS50 | Continuous endpoint captures more signal | Strong |
| Removing fatigue smart | Reduces noise from drug class effect | Medium |
| MMRM + ex-fatigue → lower SD | Powered at SD=12; CNST ex-fatigue SD=10 | Medium |
| Dexamethasone unblinds | 64% nausea → most get dex → may help symptoms | Weak |

### Bear Case Summary

| Argument | Supporting Evidence | Strength |
|----------|---------------------|----------|
| High dropout rate | 36% missing vs CNST 2% | Strong |
| Small n (Ph1b n=14) | vs CNST n=81 multicenter | Strong |
| ITT-adjusted effect similar to CNST | Assuming 0s for dropouts | Strong |
| Absolute CFB ignores baseline | % CFB analysis shows only ~2pt delta | Strong |
| Removing fatigue didn't help CNST much | Sensitivity analysis: +2% spread only | Strong |
| SD math suspicious | SD=14 vs CFB=-18.5 implausible | Medium |
| 50% rux dose reduction | Effectively mono vs mono | Strong |
| SVR ceiling effect | >10% SVR doesn't add TSS | Medium |

### Expected Effect Size Calculation

**Step 1:** Baseline-adjusted CNST effect
- CNST raw: -2 pt absolute delta
- Baseline-adjusted: -1.5 pt delta

**Step 2:** Add ex-fatigue benefit
- CNST sensitivity: +3.6% spread on % CFB
- Off baseline 22.5: +0.8 pt

**Step 3:** Expected KPTI effect
- 1.5 + 0.8 = **~2.3 pt delta**

**Step 4:** Power calculation
- Assumed SD: 12
- Effect: 2.3 pt
- Power: ~40-50%

**Conclusion:** Trial is a coin flip, not the "lock" bulls suggest.

---

## KEY DEBATES

### Debate 1: Is KPTI Ph1 Data Trustworthy?

| Position | Argument |
|----------|----------|
| **BULL** | Data look BIC on SVR35, TSS50, CFB |
| **BEAR** | 36% missing data; ITT-adjusted looks like CNST |
| **Resolution** | Need to track fate of each dropout |

### Debate 2: Does Removing Fatigue Change the Outcome?

| Position | Argument |
|----------|----------|
| **BULL** | CNST almost won; removing noise tips it over |
| **BEAR** | CNST sensitivity analysis showed only +2% improvement |
| **Resolution** | Math suggests ~1 pt extra, not transformative |

### Debate 3: Can Seli Combo Beat Rux When Half Are on Suboptimal Rux?

| Position | Argument |
|----------|----------|
| **BULL** | Dose intensity >95% for seli; dex helps symptoms |
| **BEAR** | 50% on 5mg rux = seli mono vs rux mono |
| **Resolution** | This is the key risk; can't show combo benefit if half aren't on combo |

---

## PATTERN SUMMARY FOR REVEREND-BAYES

| Pattern | Application |
|---------|-------------|
| % CFB normalization | Always convert absolute CFB to % before cross-trial comparison |
| Dropout-adjusted ITT | Stress-test by assuming 0 for all missing |
| Sensitivity analysis mining | Check CT.gov for buried alternative definitions |
| Backbone dose reduction | >30% subtherapeutic = combination thesis compromised |
| Biomarker ceiling effect | Beyond threshold, more biomarker ≠ more clinical |
| SD reasonableness | SD ≈ mean CFB is suspicious |
| Endpoint gaming detection | Check if competitor's sensitivity analysis validates |

---

*Source: KPTI MF bull/bear analysis, January 2026*
*Case studies: KPTI (selinexor), CNST (pelabresib), ABBV/Navitoclax*
