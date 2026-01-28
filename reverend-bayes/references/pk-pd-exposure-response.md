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

## Exposure/IC50 Ratio Comparison (from AVTX/ZH)

### The Pattern

**When comparing drugs targeting the same pathway, normalize to Ctrough/IC50 (or AUC/IC50). Raw dose or IC50 alone is misleading.**

### Why This Matters

Different drugs have:
- Different potencies (IC50 values)
- Different PKs (half-life, clearance, volume of distribution)
- Different dosing regimens (frequency, route)

Two drugs at "equivalent" doses can have vastly different target coverage at trough.

### Framework

| Parameter | How to Use |
|-----------|------------|
| IC50 (in vitro) | Potency benchmark - lower = more potent |
| Ctrough (steady-state) | Lowest exposure between doses |
| **Ctrough/IC50 ratio** | **Target coverage at trough - higher = better coverage** |
| AUC/IC50 ratio | Total exposure-adjusted coverage |

### Calculation

```
Target Coverage = Ctrough (nM) / IC50 (nM)

If Ctrough = 100 nM and IC50 = 10 nM → Coverage = 10x
If Ctrough = 50 nM and IC50 = 50 nM → Coverage = 1x

General rule: Coverage >10x = likely saturating target
             Coverage 1-10x = partial coverage
             Coverage <1x = likely underdosed
```

### Example: IL-1 Inhibitors in HS (ZH Analysis)

| Drug | IL-1β IC50 (pM) | Half-life | Dosing | Efficacy |
|------|-----------------|-----------|--------|----------|
| Anakinra | ~nM | 4-6h | 100mg SC QD | Yes (n=10/arm) |
| Canakinumab | 0.2-1 nM | ~26 days | 150mg q4-8w | Y/N (case reports) |
| Lutikizumab | 21 pM | 10-14 days | 100-300mg q1-2w | Yes (n=40/arm) |
| MAS825 | 20-25 pM | 18-22 days | 300mg q2w→q4w | Marginal |
| LY2189102 | 2.8 pM | ~20 days | 150-600mg q2-4w | TBD |

**Gap in ZH's analysis:** Table shows IC50 and dosing but NOT Ctrough. Without Ctrough, can't calculate coverage ratio.

### Cross-Molecule Comparison Checklist

```
BEFORE CLAIMING DRUG A > DRUG B IN SAME PATHWAY:

□ Source IC50 from same assay system? (cell-based vs biochemical)
□ Report Ctrough (not just dose) for both?
□ Calculate Ctrough/IC50 for both?
□ If receptor blocker vs ligand neutralizer, different calculation required
□ Does dose-response data exist for the lead comparator?
□ Account for target form (free ligand vs receptor occupancy)
```

### Receptor Blocker vs Ligand Neutralizer Caveat

**IC50 is not directly comparable across these classes.**

| Drug Type | What IC50 Measures | Target |
|-----------|-------------------|--------|
| Ligand neutralizer (Ab) | Free ligand binding | Capture circulating ligand |
| Receptor blocker (small molecule or Ab) | Receptor occupancy | Block receptor activation |

For receptor blockers, need **receptor occupancy (RO)** calculation, not simple IC50 comparison:

```
RO (%) = [Drug] / ([Drug] + Kd) × 100

Where Kd = receptor binding constant (often ≠ IC50)
```

**Example (MEDI8968 vs Luti in HS):**
- MEDI8968 = IL-1R blocker (blocks ALL IL-1 signaling through IL-1R1)
- Lutikizumab = dual IL-1α/β neutralizer (captures free ligands)

Comparing IC50 values is apples-to-oranges. MEDI8968's IC50 measures receptor binding; Luti's IC50 measures ligand neutralization. Need RO calculation for MEDI8968.

### The Anakinra Paradox

Anakinra shows efficacy despite:
- Short half-life (4-6h) requiring daily dosing
- nM IC50 (weaker than pM antibodies)

Possible explanations:
1. **Small n** - n=10/arm may be noise
2. **Peak effect matters** - Some targets require high Cmax, not sustained Ctrough
3. **IL-1Ra mechanism** - Receptor antagonist vs neutralizing antibody (different kinetics)
4. **Rapid onset** - Anakinra effect in hours; long t½ Abs take weeks

**Lesson:** Trough/IC50 ratio isn't the only metric. Cmax, time-to-effect, and mechanism can matter.

### Integration with PoS Assessment

| Scenario | Ctrough/IC50 | PoS Adjustment |
|----------|--------------|----------------|
| Your drug >> competitor at known efficacy | Positive | Your floor is established |
| Your drug << competitor with marginal efficacy | Negative | May be underdosed |
| Your drug ≈ failed competitor | Negative | Same exposure, same outcome likely |
| Your drug >> failed competitor | Neutral | Underdosing may explain failure |

### Source: ZH AVTX Analysis (Jan 2025)

> "On an exposure to IC50 fold basis, MAS825 is underdosed (it is similar to 100 mg EW Luti, which didn't show efficacy in HS)."

**Critique:** Claim is directionally plausible but missing actual Ctrough data to prove it.

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

## QTc as Dose Ceiling (from AG on ACAD)

### The Pattern

**If 1st gen molecule had QTc prolongation limiting dose, and 2nd gen does not, the "dose higher" thesis gains validity.**

| Scenario | QTc Status | Dose Ceiling | Implication |
|----------|------------|--------------|-------------|
| 1st gen | QTc prolongation | Safety-limited | May not have reached optimal exposure |
| 2nd gen | No QTc | Tolerability-limited | Can explore higher doses |

### Application (ACAD/ADP-204)

> "The lack of QTc prolongation enables higher dosing." — AG

| Molecule | QTc | Max Tested | Dose Headroom |
|----------|-----|------------|---------------|
| Pimavanserin (1st gen) | Prolongation observed | 34mg | Limited by QTc |
| ADP-204 (2nd gen) | No signal | 60mg | Can dose 2x higher |

### Integration with E-R Analysis

QTc status changes interpretation of E-R curves:

| E-R Curve Shape (1st gen) | QTc Ceiling? | 2nd Gen Implication |
|---------------------------|--------------|---------------------|
| Still rising at max dose | Yes (QTc limited) | **Higher dose may help** — E-R not fully explored |
| Still rising at max dose | No (tolerability limited) | Higher dose still helpful |
| Plateau/regression at max | Yes (QTc limited) | **Uncertain** — was plateau from QTc or biology? |
| Plateau/regression at max | No | **Higher dose unlikely to help** — true biological plateau |

### Key Question

When evaluating 2nd gen "dose higher" thesis:

1. Did 1st gen have QTc (or other safety) ceiling?
2. If yes → E-R curve may be truncated, higher dose could unlock efficacy
3. If no → E-R plateau is likely biological, higher dose won't help

---

## Withdrawal Study Mining for Durability Floor (from APGE/RP)

### The Pattern

**When evaluating extended dosing intervals (Q3M, Q6M, annual), search for competitor withdrawal/discontinuation studies. The efficacy loss with complete drug withdrawal establishes the worst-case floor.**

### Why This Works

Withdrawal studies show what happens when drug concentration → zero. If efficacy loss is modest even with zero exposure, extended dosing intervals that maintain *some* trough should perform at least that well.

### Example: Ebglyss Withdrawal in Atopic Dermatitis

| Arm | EASI-75 Maintenance | Interpretation |
|-----|---------------------|----------------|
| Lebrikizumab Q2W | 70.8% | On-drug reference |
| Lebrikizumab Q4W | 71.2% | Extended interval ≈ Q2W |
| **Lebrikizumab Withdrawal** | **60.0%** | **Complete withdrawal floor** |

**Delta:** Only 10-11% efficacy loss with complete drug withdrawal.

**Implication for APGE Q6M:** If complete withdrawal loses only 10-11%, a Q6M regimen maintaining meaningful Ctrough should lose less than that. This bounds the downside.

### Application Framework

```
1. Find competitor withdrawal/discontinuation data
2. Calculate efficacy delta: [On-drug] - [Withdrawal] = [Max loss]
3. Compare your regimen's Ctrough to withdrawal (Ctrough ≈ 0)
4. If your Ctrough >> 0, efficacy loss should be < max loss
5. Use withdrawal efficacy as floor for your extended dosing
```

### When to Search for Withdrawal Data

| Situation | Search for Withdrawal Data? |
|-----------|----------------------------|
| Evaluating Q3M+ dosing intervals | Yes - establishes floor |
| Drug has long half-life (>2 weeks) | Yes - durability question |
| Competitor has approved extended dosing | Yes - may have withdrawal data |
| Drug targets pathway with sustained effects | Yes - may show durability even off-drug |

### Source: RP APGE Analysis (Jan 2025)

> "The proportions of lebrikizumab responders who maintained EASI 75 with no or minimal fluctuations were 70.8% (lebrikizumab Q2W), 71.2% (lebrikizumab Q4W), and 60.0% (lebrikizumab withdrawal). This suggests to me that if you completely withdrawal drug, you lose 10-11% efficacy but suggests there is quite a lot of durability of effect even when drug concentrations are close to zero."

---

## Biomarker Rebound Timing → Concentration Threshold (from APGE/RP)

### The Pattern

**Map when biomarkers rebound in PK studies to the drug concentration at that timepoint. This establishes the Minimum Effective Concentration (MEC). If your regimen's Ctrough > MEC, efficacy should be maintained.**

### Methodology

```
Step 1: Find MAD or long-term PK/PD study
Step 2: Identify when biomarker suppression is lost (rebound)
Step 3: Map timepoint to concentration curve
Step 4: Read concentration at rebound timepoint = MEC
Step 5: Compare your Ctrough to MEC
```

### Example: APGE (Zumilokibart) in Atopic Dermatitis

**MAD Study Data:**
- Dosing: 2 doses only (D1/D15 or D1/D29)
- Biomarkers: pSTAT6, TARC
- Observation: Near-complete suppression through Week 24
- Rebound: pSTAT6 and TARC start rebounding at ~Week 36
- Time since last dose at rebound: ~34 weeks

**Concentration Mapping:**
- Concentration at Week 36 (rebound point): ~10-15 µg/mL
- This is the MEC for IL-13 pathway suppression

**Application to Q6M Dosing:**
| Parameter | Value | vs MEC |
|-----------|-------|--------|
| APGE Q6M Ctrough | 24.8 µg/mL | **1.7-2.5x above MEC** |
| MEC (from MAD) | 10-15 µg/mL | Threshold |

**Conclusion:** APGE Q6M maintains Ctrough well above the concentration where biomarker rebound occurs → should maintain pathway suppression → should maintain efficacy.

### Visual Framework

```
Concentration
    ^
    |\                            MEC = concentration at rebound
    | \                           
    |  \      Q6M Ctrough         If Ctrough > MEC → efficacy maintained
    |   \    ════════════         If Ctrough < MEC → biomarker rebound risk
    |    \        
    |     \   ─ ─ ─ MEC ─ ─ ─     
    |      \  
    |       \______ Rebound occurs here
    |              
    |________________________________> Time (weeks)
              ↑
         Week 36 (rebound)
```

### Key Questions

1. **Is there MAD or long-duration PK/PD data available?**
   - Look for single/limited dose studies with long follow-up
   - Withdrawal studies also work

2. **Which biomarker is most relevant?**
   - Should be mechanistically linked to efficacy
   - pSTAT6/TARC for IL-13; VEGF for anti-VEGF; etc.

3. **Is the rebound clinically meaningful?**
   - Statistical rebound ≠ clinical loss
   - Check if rebound correlates with efficacy loss

4. **What's the confidence in concentration mapping?**
   - Sparse PK sampling = less precise
   - Population PK models can help

### Source: RP APGE Analysis (Jan 2025)

> "In MAD dosing, rebound on pSTAT6 and TARC occurred close to 36 weeks which is around 34 weeks after last dose. This corresponds to a concentration of around 10-15 ug/mL which is lower than APGE Q6M Ctrough."

---

## AE Dose-Response Direction (from APGE/RP)

### The Pattern

**Check whether AE rates increase or decrease with higher exposure. The direction tells you whether the AE is exposure-driven (dose-dependent) or mechanism/idiosyncratic.**

### Framework

| AE Dose-Response | Interpretation | Higher Dose Implication |
|------------------|----------------|------------------------|
| **Monotonic (↑ dose → ↑ AE)** | Exposure-driven toxicity | Higher dose = more AE risk |
| **Flat (↑ dose → same AE)** | Threshold effect or idiosyncratic | Higher dose unlikely to worsen |
| **Inverted (↑ dose → ↓ AE)** | Not exposure-driven | Higher dose may actually be safer |

### Example: Conjunctivitis with IL-13 Inhibitors

**Ebglyss (Lebrikizumab) Data:**

| Period | Q2W Rate | Q4W Rate | Direction |
|--------|----------|----------|----------|
| Induction (0-16 wks) | 10% | - | Baseline |
| Maintenance (16-52 wks) | 1.8% | **10.1%** | **Inverted** |

**Interpretation:** During maintenance, the *lower* exposure arm (Q4W) had *higher* conjunctivitis rate than the higher exposure arm (Q2W). This is inverted dose-response.

**Conclusion:** Conjunctivitis is NOT exposure-driven. It's likely:
- Mechanism-related (on-target effect of IL-13 inhibition)
- Or idiosyncratic (patient-specific susceptibility)

**Implication:** Extended dosing intervals (Q6M) won't reduce conjunctivitis risk, but also won't worsen it beyond what's already seen.

### When to Check AE Dose-Response

| Situation | Check AE Dose-Response? |
|-----------|------------------------|
| AE is key concern for drug class | Yes - determine if dose-related |
| Evaluating higher dose / extended interval | Yes - predict AE trajectory |
| AE appeared in one trial but not another | Yes - may be exposure difference |
| Competitor had dose-limiting toxicity | Yes - understand mechanism |

### Dupixent Confirmation

> "Dupixent induction – 34 events per 100 patient years in induction to 12 events per 100 patient years through 260 weeks open label extension."

Conjunctivitis is front-loaded (induction > maintenance) and shows inverted dose-response across IL-13 inhibitors. This is a class effect, not exposure-driven.

### Source: RP APGE Analysis (Jan 2025)

> "Again, showing an inverted dose response between Q2W and Q4W so I don't think AEs are related to drug exposure consistent with what the Dupixent exposure safety analysis suggests."

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
9. **QTc/safety ceilings can truncate E-R curves — 2nd gen without ceiling can explore further**
