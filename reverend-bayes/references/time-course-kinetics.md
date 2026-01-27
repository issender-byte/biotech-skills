# Time-Course & Kinetics Analysis

How to interpret efficacy curves, assess consistency of drug effect over time, and avoid common pitfalls in evaluating trial data.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Efficacy curve shows inconsistent separation | Yes - red flag assessment |
| Drug = placebo at intermediate timepoints | Yes - noise vs signal evaluation |
| Evaluating "late separation" claims | Yes - statistical artifact risk |
| Comparing kinetics to known positive control | Yes - benchmark methodology |
| Error bars are wide/overlapping | Yes - confidence interval discipline |
| High dose performs no better than low/placebo | Yes - dose-response coherence |

---

## Framework 1: Consistent Separation > End-of-Study Separation

### The RP Pattern

> "The kinetics are super odd to me, we know IL-1β biomarkers drop fast but if we look at the curves at many time points the high dose is no different than placebo. At week 8, all the arms are basically the same on HiSCR75. Compare this with Bimzelx where its consistently separated from placebo across most timepoints."

### What Good Kinetics Look Like

```
REAL DRUG EFFECT:
        Efficacy
           |     Drug ----→
           |    /
           |   /    ← Separation maintained
           |  /
           | / Placebo ----→
           |____________________ Time
              W2   W4   W8   W12   W16
```

### What Suspicious Kinetics Look Like

```
POSSIBLE NOISE/ARTIFACT:
        Efficacy
           |              Drug
           |             /
           |    ←-→←-→  /  ← Inconsistent, overlapping
           |      \/   /
           |      /\  /     Placebo
           |____________________ Time
              W2   W4   W8   W12   W16
              ↑
              Drug = Placebo at intermediate timepoints
```

### Pattern Classification Table

| Pattern | What It Suggests | Red Flag Level |
|---------|------------------|----------------|
| Drug separates early and maintains | Real drug effect | Low |
| Drug separates progressively and maintains | Real drug effect | Low |
| Drug = placebo at multiple timepoints, separates late | **Statistical fluctuation possible** | High |
| High dose = placebo at Week 8, separates at Week 16 | **Very concerning** | Very High |
| Dose-response inverted at intermediate timepoints | **Incoherent kinetics** | Very High |
| Drug worse than placebo at any timepoint | **Biological implausibility** | Very High |

### Application Rules

1. **Early separation that fades** = possible tolerance/tachyphylaxis
2. **Late-only separation** = possible noise, especially if CI overlapping earlier
3. **Consistent separation throughout** = strongest evidence of real effect
4. **Drug = placebo at any timepoint after expected onset** = red flag

---

## Framework 2: Positive Control Benchmarking

### The Method

Use a known successful drug in the same indication as the benchmark for "what good kinetics look like."

### Example: IL-17 in HS (Bimzelx as Positive Control)

| Timepoint | Bimzelx - Placebo Delta | Consistent? |
|-----------|-------------------------|-------------|
| Week 4 | ~15% | Yes |
| Week 8 | ~20% | Yes |
| Week 12 | ~25% | Yes |
| Week 16 | ~25% | Yes |

**Interpretation:** Bimzelx shows consistent, growing separation from placebo at every timepoint. This is what a real drug effect looks like.

### Comparison: IL-1 in HS (MAS825/Luti Concerns per RP)

| Timepoint | Drug - Placebo Delta | Consistent? |
|-----------|----------------------|-------------|
| Week 4 | ~10% | Yes |
| Week 8 | ~0% | **NO - collapsed** |
| Week 12 | ~5% | Recovering? |
| Week 16 | ~10% | Final? |

**Interpretation:** Inconsistent separation. Week 8 collapse is concerning - drug briefly performed no better than placebo.

### When to Apply Positive Control Benchmarking

| Situation | Use Positive Control? |
|-----------|----------------------|
| Same MOA, same indication | Yes - most informative |
| Same indication, different MOA | Yes - establishes "achievable" kinetics |
| Same MOA, different indication | Maybe - mechanism kinetics may apply |
| Novel target, novel indication | Limited - no benchmark exists |

---

## Framework 3: Error Bar Discipline

### The RP Observation

> "Error bars are super wide for ABBV pasted on Leo's pictures above"

### What Wide Error Bars Mean

| CI Characteristic | Implication |
|-------------------|-------------|
| **Wide CIs** | High variability in response; low confidence in point estimate |
| **Overlapping CIs (drug vs placebo)** | Separation may not be real; could be noise |
| **Asymmetric CIs** | Possible skewness; outliers may be driving effect |
| **CIs crossing zero** | Effect could be null or even negative |

### Visual Rules

```
CONFIDENT SEPARATION:              UNCERTAIN SEPARATION:
                                   
  Drug ─●─     ← Narrow CI           Drug ─────●─────  ← Wide CI
                                                    \ overlaps
  Pbo  ─○─     ← No overlap          Pbo  ─────○─────  
                                   
```

### The Checklist

Before concluding "drug beats placebo":

- [ ] Are error bars (95% CI) shown, not just point estimates?
- [ ] Do the CIs NOT overlap at the primary timepoint?
- [ ] Are the CIs reasonably narrow (N is adequate)?
- [ ] Is the separation statistically significant (p-value provided)?
- [ ] Does separation persist at multiple timepoints, not just endpoint?

---

## Framework 4: Dose-Response Coherence

### Expected Pattern

Higher dose → Greater effect (up to plateau or safety limit)

```
COHERENT DOSE-RESPONSE:
        Efficacy
           |     High Dose ----→
           |    /
           |   / Med Dose ----→
           |  /
           | / Low Dose ----→
           |/ Placebo ----→
           |____________________ Time
```

### Red Flags

| Pattern | What It Suggests | Concern |
|---------|------------------|---------|
| High dose = Low dose | Plateau reached; may be dosing too high | Medium |
| High dose < Med dose | **Inverse dose-response** | High |
| High dose = Placebo | **No drug effect at therapeutic dose** | Very High |
| High dose < Placebo | **Drug may be harmful** | Very High |

### Example: Lutikizumab Inverse Dose-Response in HS

| Dose | Regimen | Pbo-adj HiSCR50 | Pbo-adj HiSCR75 |
|------|---------|-----------------|-----------------|
| 300mg | EW (high) | 14% | 21% |
| 300mg | EOW (middle) | 24% | 28% |

**Issue:** Higher frequency dosing (EW) performed WORSE than lower frequency (EOW). Possible explanations:
1. Immunogenicity at higher exposure
2. Receptor saturation/downregulation
3. Statistical noise (CI overlap?)
4. ADA development

**Analytical Response:** Inverse dose-response requires explanation. "More drug = worse outcome" is biologically suspicious.

---

## Framework 5: Biomarker-Efficacy Kinetics Alignment

### The Expectation

If MOA is understood, biomarker kinetics should predict clinical kinetics.

### Example: IL-1β Inhibition

**Expected:**
- IL-1β pathway inhibition → rapid biomarker response (CRP, IL-6 down within days)
- Clinical response should follow biomarker timing (unless tissue penetration/compartment issues)

**RP's Observation:**
> "We know IL-1β biomarkers drop fast but if we look at the curves at many time points the high dose is no different than placebo."

**The Disconnect:**
| Parameter | Expected | Observed |
|-----------|----------|----------|
| Biomarker response | Fast (days-weeks) | Fast (confirmed) |
| Clinical response | Should follow biomarker | Inconsistent/delayed |

**Implication:** If biomarkers respond but clinical doesn't, either:
1. Wrong target (biomarker engagement ≠ clinical mechanism)
2. Wrong dose (but biomarker says dose is adequate)
3. Wrong patient population
4. Indication not driven by this pathway

---

## Framework 6: Integration with "Underdosed" Thesis Assessment

### The RP Biomarker Validation Pattern

> "MAS825 SC performed as expected with IL-6 down about 50%... suggesting to me dosing may not be an issue"

### Decision Framework

| Evidence | "Underdosed" Thesis | "Mechanism Doesn't Work" Thesis |
|----------|---------------------|--------------------------------|
| Biomarker doesn't move | ✓ Supports | ✗ |
| Biomarker moves as expected | ✗ Refutes | ✓ Supports |
| Kinetics inconsistent despite biomarker hit | ✗ | ✓ Strong support |

### Application

When someone claims "the drug was underdosed" to explain underwhelming efficacy:

1. **Check biomarker data** - Did the expected PD biomarker move?
2. **Check dose-response** - Did higher doses show more biomarker effect?
3. **If biomarker moved as expected** - "Underdosed" thesis is refuted
4. **If biomarker didn't move** - "Underdosed" thesis may be valid; check PK

---

## Case Studies

### Case 1: AVTX/MAS825/Luti in HS (from RP Analysis)

**Observations:**
- MAS825: IL-6 down 50% (biomarker hit) but clinical underwhelming
- Luti: High dose = placebo at Week 8 on HiSCR75
- Luti: Inverse dose-response (EW < EOW)
- MEDI8968: CRP, fibrinogen down in COPD but clinical failure

**Analytical Conclusions:**
1. "Underdosed" thesis doesn't hold - biomarkers moved
2. Kinetics are incoherent - inconsistent separation, inverse dose-response
3. Positive control (Bimzelx) shows what good kinetics look like
4. IL-1 mechanism may not translate to clinical efficacy in HS

### Case 2: [Template for Future Cases]

**Observations:**
- Drug X: [Biomarker response]
- Drug X: [Kinetics pattern at intermediate timepoints]
- Drug X: [Dose-response relationship]
- Positive control: [What does success look like?]

**Analytical Conclusions:**
1. "Underdosed" thesis: [Valid/Refuted/Uncertain]
2. Kinetics assessment: [Coherent/Incoherent/Suspicious]
3. Positive control comparison: [Matches/Doesn't match/No benchmark]
4. Mechanism validity: [Supported/Questioned/Refuted]

---

## Integration Checklist

When evaluating ANY efficacy data, ask:

**Time-Course:**
- [ ] Does separation emerge early and maintain?
- [ ] Is drug ever = placebo after expected onset?
- [ ] Are there intermediate timepoint collapses?

**Error Bars:**
- [ ] Are CIs shown?
- [ ] Do CIs overlap at key timepoints?
- [ ] Is N adequate for narrow CIs?

**Dose-Response:**
- [ ] Does higher dose → better effect?
- [ ] Is there inverse dose-response?
- [ ] Does high dose = placebo at any timepoint?

**Biomarker Alignment:**
- [ ] Did expected biomarkers move?
- [ ] Do clinical kinetics match biomarker kinetics?
- [ ] If biomarker hit but clinical miss, why?

**Positive Control:**
- [ ] What do good kinetics look like in this indication?
- [ ] Does this drug match the positive control pattern?
- [ ] If kinetics differ, is there a biological explanation?

---

## Key Takeaways

1. **Consistent separation > end-of-study separation** - Drug = placebo at intermediate timepoints is a red flag
2. **Use positive controls** - Bimzelx in HS shows what good kinetics look like; benchmark against winners
3. **Look at error bars** - Wide/overlapping CIs mean the "separation" may be noise
4. **Check dose-response coherence** - Inverse dose-response is biologically suspicious
5. **Align biomarker and clinical kinetics** - If biomarker hits but clinical misses, the "underdosed" thesis fails
6. **Integration is key** - Time-course analysis connects to biomarker validation, dose-response, and mechanism assessment

---

## Source Attribution

Framework developed from RP feedback on AVTX/IL-1 analysis (January 2025).
