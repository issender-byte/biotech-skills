# PK/PD Exposure-Response Analysis Framework

How to analyze when efficacy differences are driven by pharmacokinetics (exposure), not pharmacodynamics (biology). Critical for understanding cross-indication differences and predicting trial outcomes.

---

## When to Use This Framework

| Situation | Use E-R Analysis |
|-----------|-----------------|
| Same drug looks different across indications | Yes - check if exposure differs |
| Same drug looks different across trials | Yes - check design differences (dose caps, titration) |
| Heavier/lighter patient populations | Yes - mg/kg dosing with caps creates exposure differences |
| Concomitant medications differ between trials | Yes - DDIs affect exposure |
| Competitor comparison where potency differs | Yes - need potency-adjusted exposure |
| Drug "doesn't work" in harder indication | Maybe - could be exposure ceiling |

---

## The Raj Dose-Cap Insight

### Core Problem

**If there's a maximum daily dose cap, heavier patients can't achieve the mg/kg exposure that lighter patients get.**

### Example: Fintepla in LGS vs Dravet

| Parameter | Dravet | LGS | Implication |
|-----------|--------|-----|-------------|
| Max daily dose | 26mg | 26mg | Same cap |
| Mean patient weight | ~32kg | ~42kg | LGS heavier |
| Max titration dose | 0.7 mg/kg | 0.7 mg/kg | Same target |
| Achievable exposure at mean weight | 0.81 mg/kg | 0.62 mg/kg | LGS lower |
| Weight at which cap binds | 37kg | 37kg | ~50% of LGS pts |

**Calculation:**
- Max daily dose = 26mg
- Target dose = 0.7 mg/kg
- Weight at which cap binds = 26 / 0.7 = 37.1 kg
- In LGS, ~50% of patients weigh >37.5kg → they can't reach target mg/kg

### E-R Curve Interpretation

```
Efficacy
    ^
    |           ___________
    |          /
    |         /
    |        /
    |       /
    |      /    ← Dravet achieves exposures here
    |     /
    |    /  ← LGS stuck here due to dose cap
    |   /
    |__/________________________> Exposure (Cmax or AUC)
```

**The drug isn't less effective in LGS - patients just aren't getting enough exposure.**

---

## The Mike Challenge: "Wouldn't mg/kg Dosing Equalize Exposure?"

### The Answer: Not If There's a Dose Cap

| Scenario | Patient Weight | Target (mg/kg) | Actual Dose | Exposure |
|----------|---------------|----------------|-------------|----------|
| Under cap | 30kg | 0.7 | 21mg | Full |
| At cap | 37kg | 0.7 | 26mg (cap) | Full |
| Over cap | 50kg | 0.7 | 26mg (cap) | 52% of target |
| Far over cap | 100kg | 0.7 | 26mg (cap) | 37% of target |

### What to Look For in Trial Designs

1. **Is there a dose cap?** (regulatory, safety, or formulation-driven)
2. **What's the weight distribution in the trial population?**
3. **What % of patients hit the cap?**
4. **Does the E-R curve plateau before the cap, or is efficacy still increasing?**

---

## Concomitant Medication Effects

### The Problem

Background medications can:
1. **Reduce exposure** via CYP induction (lower plasma levels)
2. **Increase exposure** via CYP inhibition (higher plasma levels, toxicity risk)
3. **Reduce efficacy** via pharmacodynamic competition (same receptor/pathway)

### Fintepla Example

| Background ASM | Effect on Fintepla Efficacy |
|----------------|----------------------------|
| Clobazam | Efficacy looks weaker |
| Valproate | Efficacy looks weaker |
| Fewer prior ASMs failed | Larger effect size |

### Cross-Trial Design Differences

| Trial | Concomitant ASM Cap | Implication |
|-------|---------------------|-------------|
| LBPH Phase 1/2 | Capped at 4 | Cleaner population |
| DRUG | Mean/median > 4 | Harder population, reduced efficacy |

**If your trial allows more concomitant meds than the comp, your efficacy may look worse even if the drug is equivalent or better.**

---

## Potency-Adjusted Exposure Comparison

### When Comparing Drugs with Different Potencies

Don't compare mg doses - compare **potency-adjusted exposure**.

### Framework

```
Potency-adjusted exposure = (Dose / EC50) × Fraction at target

If Drug A has EC50 of 10 nM and Drug B has EC50 of 50 nM:
- Drug A at 10mg ≈ Drug B at 50mg (potency-adjusted equivalent)
```

### Example from Exchange

| Drug | Potency-Adjusted Exposure | Observed Efficacy |
|------|---------------------------|-------------------|
| LBPH | 1x | Baseline |
| DRUG | 5x | ~10% better in LGS |

**Interpretation:** DRUG is achieving 5x the potency-adjusted exposure and seeing ~10% better efficacy in a harder-to-treat population. This suggests:
1. E-R relationship is real (more exposure → more efficacy)
2. DRUG could look better in Phase 3 if exposure advantage maintained
3. LBPH may have room to improve if they can increase exposure

---

## E-R Analysis Checklist

### Before Comparing Trials or Indications

1. **Dose and Exposure**
   - [ ] Is there a dose cap? What is it?
   - [ ] What's the weight distribution in each trial?
   - [ ] What % of patients hit the cap?
   - [ ] Are plasma concentrations reported (not just dose)?

2. **E-R Curve Shape**
   - [ ] Is E-R relationship monotonic (more = better) or does it plateau?
   - [ ] Where on the E-R curve are most patients?
   - [ ] Is there a clear exposure threshold for efficacy?

3. **Concomitant Medications**
   - [ ] What background meds are allowed?
   - [ ] Are there DDI concerns (CYP interactions)?
   - [ ] Does background therapy affect efficacy (PD competition)?

4. **Population Differences**
   - [ ] Are patients heavier/lighter?
   - [ ] Are patients more/less refractory?
   - [ ] Are baseline disease characteristics different?

---

## How E-R Analysis Changes PoS Assessment

### Scenario 1: Drug "Failed" in One Indication

**Before E-R analysis:** "Drug doesn't work in LGS, negative read-through"

**After E-R analysis:** "Drug didn't achieve adequate exposure in LGS due to dose cap + heavier patients. Not a biology failure - it's a PK problem. If exposure could be increased, drug might work."

**PoS impact:** Don't penalize for indication where exposure was suboptimal.

### Scenario 2: Competitor Looks Better

**Before E-R analysis:** "Competitor shows 60% efficacy vs our 50% - we're behind"

**After E-R analysis:** "Competitor achieved 3x higher potency-adjusted exposure. If we dose higher, we could match or exceed."

**PoS impact:** Less negative if exposure differential explains efficacy gap.

### Scenario 3: Your Trial Has Harder Population

**Before E-R analysis:** "Our trial has more concomitant ASMs - we'll look worse"

**After E-R analysis:** Quantify the expected efficacy hit from concomitant meds. Adjust expectations accordingly, but don't mark down the drug.

**PoS impact:** Adjust for trial design, not drug quality.

---

## Mike's Follow-Up Questions (Best Practices)

When someone presents E-R analysis, ask:

1. **"Can you show patient weight distribution?"**
   - Validate that weight difference is meaningful, not just assumed

2. **"Is the E-R curve from the same indication?"**
   - Dravet E-R may not apply to LGS if disease biology differs

3. **"What's the source of the concentration data?"**
   - Observed exposures vs modeled can differ significantly

4. **"How noisy is the E-R model?"**
   - Wide confidence intervals = less reliable
   - Observed quartile analysis often more robust than model

5. **"Can we share this with the company?"**
   - E-R insights can inform trial design (enroll lighter patients, reduce concomitant meds)

---

## Integration with Main PoS Framework

### Where E-R Analysis Fits

| Pillar | How E-R Analysis Informs |
|--------|-------------------------|
| 1. Trial Design | Dose cap implications, titration scheme |
| 2. Population | Weight distribution, concomitant med burden |
| 3. Comparator | N/A for placebo-controlled |
| 4. Efficacy Signal | Exposure-adjusted efficacy, not raw response rates |
| 5. Competitive | Potency-adjusted exposure comparison |
| 6. Execution | N/A |

### When to Anchor on E-R vs. Observed Efficacy

| Situation | Use |
|-----------|-----|
| E-R relationship well-characterized, exposure suboptimal | E-R-adjusted efficacy |
| E-R relationship unclear or noisy | Observed efficacy with caveats |
| Exposure optimal, efficacy still low | Observed efficacy (drug may not work) |

---

## Template: E-R Cross-Indication Analysis

```
═══════════════════════════════════════════════════════════════
EXPOSURE-RESPONSE ANALYSIS
Drug: [Name]
Indication A: [e.g., Dravet] | Indication B: [e.g., LGS]
═══════════════════════════════════════════════════════════════

DOSE AND EXPOSURE COMPARISON:
| Parameter | Indication A | Indication B |
|-----------|--------------|--------------|
| Max daily dose | | |
| Mean patient weight | | |
| % patients at cap | | |
| Mean exposure achieved | | |

E-R CURVE ASSESSMENT:
- Shape: [Monotonic / Plateau / Threshold]
- Optimal exposure range: [X-Y ng/mL or mg/kg]
- Indication A exposure: [Within / Below / Above optimal]
- Indication B exposure: [Within / Below / Above optimal]

CONCOMITANT MEDICATION ANALYSIS:
| Trial | Background meds allowed | Known DDIs | PD competition |
|-------|------------------------|------------|----------------|
| | | | |

EXPOSURE-ADJUSTED EFFICACY:
- Indication A observed: [X%]
- Indication B observed: [Y%]
- If Indication B achieved Indication A exposure: [estimated Z%]

IMPLICATIONS:
- Is efficacy difference explained by exposure? [Yes / Partially / No]
- Can exposure be increased? [Yes - how / No - why]
- PoS adjustment: [+/- X%]
═══════════════════════════════════════════════════════════════
```

---

## Common E-R Red Flags

| Red Flag | What It Means |
|----------|---------------|
| Dose cap binding in >30% of patients | Significant efficacy ceiling |
| E-R curve still rising at max exposure | Leaving efficacy on the table |
| Wide E-R confidence intervals | Uncertain relationship |
| Modeled E-R differs from observed quartiles | Model may be wrong |
| High concomitant med burden vs comp | Efficacy may look artificially worse |
| No plasma concentration data reported | Can't do proper E-R analysis |
| **E-R plateau/regression at high doses** | Higher dose may not help (see below) |

---

## E-R Plateau Skepticism (from ACAD)

### The "Just Dose Higher" Thesis Problem

**If prior E-R data shows efficacy regression at highest concentrations, the "dose higher" thesis is suspect.**

### Pattern Recognition

| E-R Shape | Implication |
|-----------|-------------|
| Still rising at max tested dose | Higher dose may help |
| Plateau (flat) at high doses | Higher dose unlikely to add efficacy |
| **Regression (decline) at high doses** | **Red flag - higher dose may hurt** |

### ACAD Example (Pimavanserin in PDP)

```
E-R Curve Shape:
    ^
    |      ●
    |     / \
    |    /   ● (highest conc regresses)
    |   /     
    |  ●       
    | /        
    ●__________> Exposure
```

> "The highest concentration had some regression. This could be due to small n or could be reaching plateau in efficacy."

**Rule:** When evaluating "2nd gen dosed higher" thesis, check if 1st gen showed plateau/regression at high exposure. If yes, higher exposure from 2nd gen may not translate to better efficacy.

### Questions to Ask

1. What did the E-R curve look like in prior studies?
2. Did the highest tested dose/exposure show continued benefit?
3. Is there a biological reason for plateau (receptor saturation, toxicity)?
4. How much of the efficacy gain comes from exposure vs. other factors?

---

## 2nd Gen vs 1st Gen Molecule Comparison (from ACAD)

### Framework for Evaluating "Improved" Molecules

When company claims 2nd gen is "better" than 1st gen, evaluate systematically:

| Dimension | How to Assess | ACAD Example |
|-----------|---------------|--------------|
| **PK/Exposure** | Cmax, Cavg at comparable doses | 2nd gen 60mg ≈ 1.6x 1st gen 34mg Cavg |
| **CNS Penetration** | CSF exposure ratio | 2nd gen 5x higher CSF exposure |
| **Potency** | In vitro IC50/EC50 | 2nd gen more potent (in vitro) |
| **Safety enabling** | Can you dose higher safely? | 2nd gen no QT issue, can dose 2x |
| **Total exposure gain** | Combine all factors | ~1.6x plasma, potentially ~8x CNS |

### The Key Question

**Does the improvement actually matter for efficacy?**

| Improvement Type | When It Matters |
|------------------|-----------------|
| Higher exposure possible | E-R curve still rising (not plateau) |
| Better CNS penetration | CNS is the relevant compartment |
| Higher potency | If prior generation was underdosed |
| Longer half-life | If trough matters for efficacy |

### 2nd Gen Skepticism Checklist

```
□ Did 1st gen show dose-response in target indication? If no → red flag
□ Did 1st gen show E-R plateau/regression? If yes → more exposure may not help
□ Is 2nd gen improvement in the relevant compartment? (CNS vs plasma)
□ Is there preclinical proof that 2nd gen is more efficacious? (Head-to-head, not just PK)
□ Has the company shown the improvement matters for the endpoint?
```

### Application (ACAD)

| Factor | Assessment |
|--------|------------|
| 1st gen E-R in ADP | Limited data, PDP showed plateau |
| 1st gen efficacy in ADP | Weak (parallel failed, RW marginal) |
| 2nd gen improvement | ~1.6x plasma, ~5x CNS exposure |
| Does it matter? | **Uncertain** - if already at plateau, more exposure may not help |

**WS Conclusion:** 30% PoS reflects skepticism that improved exposure will overcome weak underlying efficacy.

---

## Key Takeaways

1. **"Same drug, different efficacy" may be exposure, not biology**
2. **Dose caps + heavy patients = exposure ceiling**
3. **Concomitant meds can reduce efficacy (PD) or exposure (PK)**
4. **Compare potency-adjusted exposure, not raw doses**
5. **E-R analysis can rescue a "failed" indication or explain a "success"**
6. **Always ask for weight distribution and plasma concentrations**
7. **E-R plateau/regression = skepticism of "dose higher" thesis**
8. **2nd gen improvements only matter if 1st gen was underexposed on the rising part of E-R curve**
