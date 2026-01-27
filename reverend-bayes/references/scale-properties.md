# Clinical Scale Properties Framework

How to interpret clinical scales correctly. Non-linear scales, floor/ceiling effects, and cross-trial comparison pitfalls.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Interpreting point changes on any clinical scale | Yes |
| Comparing deltas across trials with different baselines | Yes |
| Assessing if effect size is clinically meaningful | Yes |
| Evaluating power calculations that use point changes | Yes |
| Any scale where "2 points" might mean different things | Yes |

---

## Framework 1: Linear vs Non-Linear Scales

### The Problem (from AG on ACAD)

**NPIC (Neuropsychiatric Inventory - Caregiver) is a non-linear scale, which makes point changes hard to interpret.**

Not all clinical scales are created equal:

| Scale Type | Property | Interpretation |
|------------|----------|----------------|
| **Linear** | 1 point = same clinical meaning at all severities | Point delta = clinical delta |
| **Non-linear** | 1 point = different meaning at different severities | Point delta ≠ clinical delta |

### Common Scale Types

| Scale | Type | Range | Notes |
|-------|------|-------|-------|
| **NPIC/NPI** | Non-linear | 0-144 | Frequency × Severity product; floor/ceiling effects |
| **SAPS-H+D** | Non-linear | 0-45 | Hallucinations + Delusions subscales |
| **PANSS** | Non-linear | 30-210 | Positive, negative, general subscales |
| **ADAS-Cog** | Non-linear | 0-70 | Item difficulties vary |
| **HAM-D** | Non-linear | 0-52 | More sensitive at moderate severity |
| **6MWD** | Linear | 0-800m+ | Continuous measure, meters |
| **FVC (% predicted)** | Linear | 0-120%+ | Continuous measure, percentage |
| **ACR20/50/70** | Binary | Yes/No | Responder threshold |

### Why Non-Linear Matters

**Example: 5-point change on NPI**

| Baseline | 5-point change | Clinical meaning |
|----------|---------------|------------------|
| NPI = 80 (severe) | 80 → 75 | Modest improvement, still severe |
| NPI = 25 (mild) | 25 → 20 | Meaningful improvement, approaching normal |
| NPI = 8 (minimal) | 8 → 3 | Near floor, may be measurement noise |

**The same point delta has different clinical significance depending on where you start.**

---

## Framework 2: Floor and Ceiling Effects

### Definitions

| Effect | Definition | Problem |
|--------|------------|---------|
| **Floor effect** | Scale can't go lower, even if patient improves | Underestimates improvement in mild patients |
| **Ceiling effect** | Scale can't go higher, even if patient worsens | Underestimates worsening in severe patients |

### Impact on RW Trial Interpretation

In randomized withdrawal designs:
- OL period: Patients improve, may approach **floor** (can't measure further improvement)
- DB period: Placebo patients worsen, but drug patients near floor **can't show delta**

> "Since the magnitude [of OL improvement] is so big, there may not have been much juice left to squeeze out." — MM

### Ceiling Effect in Withdrawal

| Scenario | Expected Delta | Actual Delta | Why |
|----------|---------------|--------------|-----|
| Severe → Moderate (OL) | Large | Large | Room to improve |
| Moderate → Mild (OL) | Moderate | Moderate | Still room |
| Mild → Near-normal (OL) | Small | Small | Approaching floor |
| Near-normal (DB maintenance) | Small | **Very small** | Floor binding |

**Application:** When DB delta looks "small," check if patients are near floor. Small delta near floor ≠ weak drug.

---

## Framework 3: NPIC Specific Properties

### Scale Construction

```
NPIC = Σ (Frequency × Severity × Caregiver Distress) across 12 domains

Domains: Delusions, Hallucinations, Agitation, Depression, 
         Anxiety, Euphoria, Apathy, Disinhibition, 
         Irritability, Aberrant Motor, Sleep, Appetite

Each domain:
- Frequency: 0-4
- Severity: 0-3 (if present)
- Domain score: 0-12
- Total NPIC: 0-144
```

### Non-Linearity Sources

1. **Multiplication** — Frequency × Severity creates non-linear relationship
2. **Multiple domains** — Improvement in one domain may not offset worsening in another
3. **Threshold effects** — Going from "daily" to "weekly" symptoms is clinically meaningful but same 1-point change as "weekly" to "few times"

### Cross-Trial Comparison Challenges

| Problem | Example |
|---------|---------|
| Different baseline severity | Trial A: NPIC=60, Trial B: NPIC=40 |
| Different domain composition | Trial A: Hallucinations-driven, Trial B: Agitation-driven |
| Different populations | DRP vs ADP have different symptom profiles |

**Rule:** Never compare raw point deltas across trials with different baseline characteristics.

---

## Framework 4: SAPS-H+D (Hallucinations + Delusions Subscale)

### Scale Construction

```
SAPS-H+D = Hallucinations subscale + Delusions subscale

Hallucinations: 7 items, 0-5 each → 0-35
Delusions: 13 items, 0-5 each → 0-65
Combined H+D: 0-100 (though typical range much narrower)
```

### ADP-204 (ACAD) Context

- **Primary endpoint:** SAPS-H+D (not NPIC)
- **Also measuring:** NPIC (secondary, enables read-through)
- **Powered for:** 0.4 effect size (Cohen's d)

### Converting Effect Size to Point Delta

| Input | Formula |
|-------|---------|
| Cohen's d | 0.4 |
| SD assumption | Unknown (need from prior data) |
| Expected delta | d × SD |

**If SD = 10:** Expected delta = 0.4 × 10 = 4 points
**If SD = 15:** Expected delta = 0.4 × 15 = 6 points

**Critical:** Power for 0.4 effect size depends entirely on SD assumption. Always ask: "What SD are they assuming?"

---

## Framework 5: Percent Change from Baseline Issues

### The Problem

Many scales use "% CFB" (percent change from baseline) to normalize across different baseline severities.

| Metric | Advantage | Disadvantage |
|--------|-----------|--------------|
| Absolute delta | Simple, interpretable | Biased by baseline |
| % CFB | Normalizes for baseline | Amplifies noise at low baseline |

### Example: % CFB Trap

| Patient | Baseline | Week 12 | Absolute Δ | % CFB |
|---------|----------|---------|------------|-------|
| A | 50 | 40 | -10 | -20% |
| B | 10 | 5 | -5 | -50% |

Patient B looks "better" on % CFB but has smaller absolute improvement.

**Application:** When trials use % CFB, check baseline distribution. Low-baseline patients can distort mean % CFB.

---

## Framework 6: Implications for Power Analysis

### Effect Size Requires SD

Power calculations using "effect size" (Cohen's d, Hedges' g) require an SD assumption:

```
Detectable delta = effect size × SD
Required N = f(effect size, α, power)
```

**If you don't know the SD, you can't interpret the effect size.**

### SD Sources (in order of preference)

1. **Same scale, same indication, same population** — Best
2. **Same scale, similar indication** — Good
3. **Same scale, different indication** — Caution
4. **Historical averages for the scale** — Last resort

### ACAD Example

AG noted ADP-204 is powered for 0.4 effect size on SAPS-H+D.

To interpret:
1. What SD is ACAD assuming? (Check protocol or prior trials)
2. Is that SD realistic for ADP population?
3. What point delta does 0.4 × SD produce?
4. Is that point delta clinically meaningful on SAPS-H+D?

---

## Integration Checklist: Scale Interpretation

```
SCALE ASSESSMENT CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SCALE PROPERTIES:
□ Scale name: _____
□ Type: [ ] Linear  [ ] Non-linear
□ Range: _____ to _____
□ Typical trial baseline: _____
□ Floor effect threshold: _____
□ Ceiling effect threshold: _____

TRIAL CONTEXT:
□ Baseline severity in this trial: _____
□ Near floor? [ ] Yes  [ ] No
□ Near ceiling? [ ] Yes  [ ] No
□ % CFB or absolute delta? _____

EFFECT SIZE TRANSLATION:
□ Effect size stated: _____
□ SD assumption: _____ (source: _____)
□ Expected point delta: effect size × SD = _____
□ Is that delta clinically meaningful? [ ] Yes  [ ] No

CROSS-TRIAL COMPARISON:
□ Are baselines comparable? [ ] Yes  [ ] No  [ ] Adjust
□ Are populations comparable? [ ] Yes  [ ] No
□ Is endpoint identical? [ ] Yes  [ ] No (specify difference)
□ Adjustment needed: _____
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Common Mistakes

| Mistake | Correction |
|---------|------------|
| Comparing point deltas across different baselines | Normalize or use % CFB with caution |
| Assuming "2 points" means the same thing everywhere | Check scale type and baseline position |
| Using effect size without knowing SD | Always identify SD assumption |
| Ignoring floor effects in RW trials | Small DB delta near floor may be expected |
| Treating all subscales equivalently | Different domains have different clinical weight |

---

## Key Principles

1. **Always know your scale type** — Linear vs non-linear changes interpretation
2. **Point deltas are baseline-dependent** — Same delta means different things at different severities
3. **Effect size ≠ point delta** — Need SD to translate
4. **Floor/ceiling effects compress observed deltas** — Especially in RW designs
5. **Cross-trial comparison requires baseline matching** — Or explicit adjustment

---

## Sources

- AG feedback on ACAD NPIC interpretation (Jan 2026)
- NPIC scale documentation
- SAPS scoring manual
- General psychometric principles
