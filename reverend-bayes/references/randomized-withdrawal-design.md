# Randomized Withdrawal Trial Design

Framework for analyzing trials that use enrichment designs with open-label run-in followed by randomized withdrawal among responders.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Trial has "Period 1" (open-label) + "Period 2" (randomized) | Yes |
| Responders from open-label phase get randomized | Yes |
| Primary endpoint is "maintenance of response" or "relapse prevention" | Yes |
| Assessing power/probability of success for enrichment design | Yes |
| Evaluating single-arm data from Period 1 only | Yes |

---

## Framework 1: Randomized Withdrawal Mechanics

### Trial Structure

```
PERIOD 1 (Open-Label Run-In)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
All patients (N) → Active drug
    ↓
Responders identified (n = N × response rate)
Non-responders exit

PERIOD 2 (Randomized Withdrawal)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Responders (n) randomized to:
- Continue active drug
- Switch to placebo
    ↓
Primary endpoint: Maintenance of response
```

### Key Insight: Period 1 Drives Everything

> **The Period 1 response rate determines the randomization N, which determines Period 2 power.**

Small changes in Period 1 response rate create large power swings because:
1. Fewer responders = smaller randomization N
2. Smaller N = lower power
3. Underpowered Period 2 = failed trial

---

## Framework 2: Power Analysis for Randomized Withdrawal

### The Math

| Variable | Definition |
|----------|------------|
| N | Total enrolled in Period 1 |
| RR₁ | Period 1 response rate |
| n | Responders for randomization (N × RR₁) |
| k | Number of arms in Period 2 |
| n/k | Patients per arm |
| MR_drug | Maintenance rate on drug |
| MR_pbo | Maintenance rate on placebo |

### IMVT Example: ACR20 in ACPA+ D2T RA

**Scenario A: Period 1 ACR20 = 65%**
```
N = 120 enrolled
n = 120 × 65% = 78 responders
Arms = 3 (600mg, 300mg, pbo)
Per arm = 78/3 = 26 patients

Maintenance assumptions:
- Placebo: 40%
- 300mg: 70%
- 600mg: 75%

Power = 63-78%
```

**Scenario B: Period 1 ACR20 = 60%**
```
N = 120 enrolled
n = 120 × 60% = 72 responders
Arms = 3 (600mg, 300mg, pbo)
Per arm = 72/3 = 24 patients

Maintenance assumptions (more conservative):
- Placebo: 40%
- 300mg: 65%
- 600mg: 70%

Power = 43-59%
```

### Sensitivity Table: Response Rate → Power

| Period 1 RR | Responders (n) | Per Arm | Approx Power |
|-------------|----------------|---------|--------------|
| 70% | 84 | 28 | 80-85% |
| 65% | 78 | 26 | 65-78% |
| 60% | 72 | 24 | 45-60% |
| 55% | 66 | 22 | 35-50% |
| 50% | 60 | 20 | 25-40% |

**Key Takeaway:** 5% change in Period 1 response rate can swing power by 15-20%.

### Placebo Maintenance Rate Benchmarks

Source for placebo maintenance assumptions:

| Study | Design | Pbo Maintenance | Drug Maintenance |
|-------|--------|-----------------|------------------|
| RCI in RA | 12wk open-label + 12wk withdrawal | 42% | 61% |

> "My assumption of 40% pbo maintenance rate is based on the 2-part study of repository corticotropin injection (RCI) in RA, which has a similar trial design."

---

## Framework 3: Single-Arm Open-Label Data Limitations

### When Period 1 Data Alone Can't Solve Debates

Single-arm, open-label data is inherently limited because:

1. **No concurrent control** - can't attribute effect to drug vs. placebo/regression
2. **Selection bias** - patients willing to enroll may differ
3. **Investigator bias** - unblinded assessment
4. **No comparator context** - hard to benchmark vs. SOC

### When Prior RCT Failure Exists

> "Have to view everything in context of prior FcRN failures x2 in RA, and regulatory precedent."
> "JNJ FcRN failed two trials in tx-experienced RA versus controls, so they have already proven this MoA doesn't work well for refractory RA; RCT data will be needed to solve a debate."

**Critical Rule:**
When randomized, controlled data exists showing mechanism failure, single-arm open-label data cannot rehabilitate the mechanism. Only new RCT data can solve the debate.

### Threshold for Commercial Relevance

For single-arm data to generate interest despite mechanism concerns:

| Situation | Required Threshold |
|-----------|-------------------|
| Comps show ACR20 ~55% (range 42-75%) | Need >70% ACR20 |
| Prior mechanism failure in RCT | Need clearly superior single-arm data |
| No CRP reduction (mechanism red flag) | Data unlikely to solve debate regardless |

> "IMVT would IMO need to show an ACR20 of >70% to think the drug's even commercially relevant versus other active drugs."

---

## Framework 4: Regulatory Precedent in Trial Design

### Approval History Matters

> "RA drugs have never been approved based on randomized withdrawal in RA, so this trial's ultimate endpoint of ACR20 relapse prevention has no precedent for approval."

**Implications:**
1. Trial may be Ph2 only, requiring traditional Ph3 for approval
2. FDA guidance typically requires function/radiograph corroboration
3. ACR20 alone may be insufficient for DMARD claim

### FDA Requirements for RA Approval

| Element | Requirement | RW Design |
|---------|-------------|-----------|
| Efficacy endpoint | ACR20/50/70 or DAS28 | ✓ Can measure |
| Functional endpoint | HAQ-DI improvement | ? Often not primary |
| Radiographic | Structural damage prevention | ✗ RW design too short |
| CRP/inflammatory | DAS28-CRP includes it | ✓/✗ Depends on drug |

> "FDA has always wanted function/radiograph endpoint corroboration to support approval of a DMARD claim, making ACR20 alone less derisking."

### Design Classification

| Trial Design | Typical Use | Registrational? |
|--------------|-------------|-----------------|
| Traditional parallel RCT | First approval | Yes |
| Randomized withdrawal | Dose optimization, rare disease | Sometimes |
| Open-label extension | Safety, durability | No |

---

## Framework 5: Mechanism-Specific Red Flags

### CRP as Mechanism Validator in RA

> "Every drug which works in RA has a strong reduction in CRP (~-60%), however JNJ's nipo FcRN ph2 did not reduce CRP at all (it increased in fact, yet BL were elevated per usual)."

**CRP Benchmark:**
| Drug Class | CRP Reduction | Implication |
|------------|---------------|-------------|
| Approved RA drugs | ~60% | Standard for mechanism validation |
| JNJ FcRn (Nipocalimab) | 0% (increased) | Mechanism red flag |

### When Mechanism Data Conflicts with Efficacy Data

JNJ FcRn Ph2 showed:
- ACR20/50 comparable to comps (net of placebo)
- But: No CRP reduction
- But: No added benefit over TNF when dosed on top

**Interpretation:**
> "FcRN data on ACR and joint count endpoints net of pbo looks comparable to the other active drugs, but FcRN data focused on drug arm only gets only about 75% of the magnitude of benefit."

The placebo-adjusted data looks okay, but the absolute drug arm data is weaker, suggesting potentially easier-to-treat population rather than true efficacy.

---

## Framework 6: Catalyst Assessment for Randomized Withdrawal Data

### Questions to Ask

1. **What data is being released?**
   - Period 1 only (open-label) → Limited value
   - Period 2 (randomized) → More informative
   
2. **Does prior RCT data exist for mechanism?**
   - Yes, failed → Single-arm data can't solve debate
   - Yes, succeeded → Single-arm data confirms
   - No → Single-arm data creates hypothesis
   
3. **Is there regulatory precedent for this design?**
   - Yes → Path to approval clearer
   - No → May need additional trials
   
4. **What threshold must be exceeded?**
   - Benchmark against comps
   - Add premium for mechanism concerns

### IMVT Case Assessment

| Question | Answer | Implication |
|----------|--------|-------------|
| What data in 2026? | Period 1 open-label ACR20 | Limited - can't solve debates |
| Prior RCT data? | JNJ failed 2 Ph2s | RCT needed to rehabilitate |
| Regulatory precedent? | No RW approvals in RA | Ph3 likely needed |
| Required threshold? | >70% ACR20 vs ~55% comps | High bar |

**Conclusion:**
> "The 2026 single-arm ACR20 response rate data from IMVT will not solve any debates and thus likely not generate meaningful POS value for the asset in RA."

---

## Integrated Checklist: Randomized Withdrawal Assessment

```
RANDOMIZED WITHDRAWAL TRIAL ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TRIAL STRUCTURE:
□ Period 1 duration: _____ weeks
□ Period 1 N enrolled: _____
□ Period 1 responder definition: _____
□ Period 2 duration: _____ weeks
□ Period 2 arms: _____
□ Primary endpoint: _____

POWER ANALYSIS:
□ Expected Period 1 response rate: _____%
□ Expected responders (n): _____
□ Patients per Period 2 arm: _____
□ Placebo maintenance rate assumption: _____%
□ Drug maintenance rate assumption: _____%
□ Estimated power: _____%

SENSITIVITY CHECK:
□ If Period 1 RR drops 5%: Power = _____%
□ If Period 1 RR drops 10%: Power = _____%
□ Minimum Period 1 RR for adequate power: _____%

PRIOR DATA CONTEXT:
□ Prior RCT data for mechanism? [ ] Yes [ ] No
□ If yes, outcome: [ ] Success [ ] Failure
□ Mechanism-specific biomarker (e.g., CRP): _____
□ Benchmark drug response rate: _____%

REGULATORY PRECEDENT:
□ Prior approvals using this design? [ ] Yes [ ] No
□ Additional trials likely needed? [ ] Yes [ ] No
□ Endpoint alignment with FDA guidance? [ ] Yes [ ] No

CATALYST ASSESSMENT:
□ Data release: [ ] Period 1 only [ ] Period 2
□ Can this data solve key debate? [ ] Yes [ ] No
□ Required threshold for interest: _____%
□ Probability of exceeding threshold: _____%
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Case Study: IMVT-1402 in ACPA+ D2T RA

### Background

- **Drug:** IMVT-1402 (FcRn inhibitor)
- **Indication:** ACPA+ difficult-to-treat RA
- **Design:** Randomized withdrawal (Period 1 open-label + Period 2 randomized)
- **Prior data:** JNJ nipocalimab failed 2 Ph2 RCTs in RA

### Trial Structure

| Phase | Duration | N | Endpoint |
|-------|----------|---|----------|
| Period 1 | 14-16 wks | 120 | ACR20 (open-label) |
| Period 2 | 12 wks | Responders | ACR20 maintenance |

### Power Analysis

**Bull case (65% ACR20):**
- 78 responders → 26/arm → 63-78% power

**Base case (60% ACR20):**
- 72 responders → 24/arm → 43-59% power

### 2026 Catalyst Assessment

| Element | Assessment |
|---------|------------|
| Data type | Period 1 open-label ACR20 only |
| Prior mechanism data | JNJ failed 2 RCTs |
| Regulatory precedent | None for RW in RA |
| Debate solved? | No - RCT needed |
| Interest threshold | >70% ACR20 |
| Conclusion | **Not a meaningful catalyst** |

### Mechanism Concerns

| Metric | FcRn | Approved RA Drugs |
|--------|------|-------------------|
| ACR20 (pbo-adj) | Comparable | Benchmark |
| ACR20 (drug arm) | ~75% of comps | Full effect |
| CRP reduction | 0% (increased) | ~60% |
| Add-on to TNF | No benefit | Expected benefit |

### Key Quote

> "Even the IMVT final trial endpoint of ACR20 relapse prevention in 2027 won't answer the question of whether this is really any better than just giving a different biologic."

---

## Key Principles for Randomized Withdrawal Analysis

1. **Period 1 response rate drives everything** - small changes create large power swings
2. **Single-arm data can't rehabilitate failed mechanism** - only new RCT data solves debate
3. **Regulatory precedent matters** - check if design has approval history in indication
4. **Benchmark against comps with margin** - add premium for mechanism concerns
5. **Mechanism biomarkers validate** - CRP, inflammatory markers should move
6. **5% response rate change = 15-20% power change** - sensitivity matters
7. **Open-label data from RW trial is not a catalyst** - randomized portion is the test

---

## Framework 5: The "Juice Left to Squeeze" Problem

### Core Insight (from MM/AG on ACAD)

**In RW designs, the DB baseline = end of OL (responders at/near ceiling). The remaining DB delta is *marginal* — on top of the OL improvement already captured.**

> "If the baseline for that is the end of the open label period, maybe seeing only a two point delta with minimal incremental drop should be expected. Most of the benefit has already occurred."

### Visual Representation

```
NPIC Score
    ^
    |                                    
 30 |●────────────────────────────────── Baseline (sick)
    |     \
    |      \
    |       \
 20 |        ●━━━━━━━━━━━━━━━━━━━━━━━━━ End of OL (responders)
    |         \____ OL Improvement     │
    |              (the big delta)     │ DB Delta
    |                                  │ (small, but expected)
 18 |                                  ●━━ Drug arm (DB)
    |                                  
 22 |                                  ●━━ Placebo arm (DB, relapsing)
    |________________________________________> Time
         OL Period          DB Period
```

### The Interpretation Error

| WS's Interpretation | Correct Interpretation |
|---------------------|------------------------|
| DB delta of ~2 pts = "true drug effect" | DB delta = *marginal* effect after OL selection |
| Small DB delta = drug doesn't work well | Small DB delta = responders already at ceiling |
| Focus on DB period alone | Total effect = OL improvement + DB maintenance |

### MM's Analytical Prescription

> "Compare how that drug arm did during the open label portion to what the placebo arm did in the prior study."

**Translation:** The relevant comparison isn't "drug vs placebo in DB period" (which is what the RW measures). It's "OL drug arm improvement vs parallel placebo-controlled improvement in a separate trial."

This requires adjustment:
- Discount OL for lack of blinding (responder bias, investigator bias)
- Adjust for baseline differences
- Account for population selection (RW recruited responders, parallel recruits all comers)

### Application Rule

**When interpreting RW results:**
1. Calculate the OL improvement (baseline → end of OL)
2. Calculate the DB delta (end of OL → end of DB)
3. Total drug effect = OL improvement + DB maintenance value
4. Don't interpret DB delta in isolation

---

## Framework 6: Cross-Indication Validation Method

### Core Insight (from MM on ACAD)

**Test your delta-derivation methodology on a population where ground truth exists.**

> "Do the same thing with Parkinson's patients. We have a lot of data for the Parkinson's indicator for induction RCTs for Pima. Is the Delta for Parkinson's patients in the withdrawal trial's RCT portion of a similar magnitude to the several phase 3 studies ran in Parkinson's?"

### The Validation Framework

| Step | Action |
|------|--------|
| 1 | Apply your methodology to derive delta from RW data in Indication A |
| 2 | Apply same methodology to derive delta from RW data in Indication B |
| 3 | Compare Indication B RW-derived delta to actual parallel RCT delta |
| 4 | If match → methodology validated, apply to Indication A |
| 5 | If mismatch → methodology suspect, revisit assumptions |

### ACAD Example

| Indication | RW Data Available | Parallel RCT Data Available | Use |
|------------|-------------------|-----------------------------|----- |
| ADP (Alzheimer's) | Yes (subgroup) | No | Target (want to predict) |
| PDP (Parkinson's) | Yes (main trial) | Yes (multiple Ph3s) | Validation set |

**Validation Test:**
1. Use WS's methodology to derive expected parallel delta from PDP RW data
2. Compare to actual PDP parallel Phase 3 results
3. If delta matches → methodology works, apply to ADP
4. If delta doesn't match → methodology needs revision

### Why This Works

- PDP is "solved" — we know the true parallel RCT effect size
- Any methodology applied to PDP RW should reproduce the known answer
- If it doesn't reproduce, it's miscalibrated
- If it does reproduce, we gain confidence in applying it to ADP

### Generalized Pattern: Use Known Outcomes to Validate Methodology

| Situation | Validation Approach |
|-----------|---------------------|
| Extrapolating from RW to parallel | Test on indication with both designs |
| Cross-trial comparison | Test on trials with similar patients |
| Biomarker → clinical correlation | Test on drug with both data types |
| Peak sales model | Backtest on comparable launches |

---

## Framework 7: RW vs Parallel Design Comparison (Delta Compression)

### Delta Compression Rule (from ACAD/SLNO)

**Key Insight: Parallel designs show smaller treatment deltas than randomized withdrawal designs.**

This is because RW designs:
- Pre-select responders (enrichment)
- Measure "loss of response" which is easier to detect than "achievement of response"
- Placebo arm deteriorates from a good baseline (responder) rather than improving from a bad baseline

### Quantitative Reference (SLNO)

| Design | Treatment Delta | Ratio |
|--------|-----------------|-------|
| **Parallel (SOL-1)** | 1.5-3.0 points | 1x |
| **Randomized Withdrawal** | ~5 points | 1.7-3.3x |

**Rule:** When extrapolating from RW data to predict parallel trial performance, expect the delta to compress by 40-70%.

### Application (ACAD)

Pima RW showed SAPS H+D delta of 2.1 points among responders.
Expected parallel delta: <2 points (after compression).
With stats bar at 2.7, this creates low PoS for parallel design.

---

## Framework 8: Standard Deviation by Design Phase

### SD Differences in RW Trials (from ACAD)

| Phase | Population | Typical SD | Reason |
|-------|------------|------------|--------|
| **Open-label (OL)** | All comers | Higher (~10) | Full population variability |
| **Double-blind (DB)** | Responders only | Lower (~5) | Responder selection reduces variability |

**Power Analysis Implication:**

When building power tables for RW trials, use SD from the appropriate phase:
- If comparing to Period 1 OL data → use OL SD
- If powering Period 2 (among responders) → use DB SD

**ACAD Example:**
- OL portion: SD = 9.5-10.5 (CFB at wk4-8)
- DB portion: SD = 5 (CFB at wk6)
- Using OL SD for Period 2 power calculation would be conservative
- Using DB SD would be more accurate but data often not available

---

## Framework 9: FDA Rejection Despite Stats

### Regulatory Risk in Weak Efficacy (from ACAD/Pima)

**Hitting stats does not guarantee approval.**

| Scenario | Pima ADP Example |
|----------|------------------|
| Trial 1 (Parallel) | p=0.045, missed (bar was 0.05) |
| Trial 2 (RW) | HR 0.35, hit primary endpoint |
| FDA Decision | **CRL - rejected for weak efficacy** |

**Rule:** If parallel design shows borderline or failed result, even a successful RW trial may not rescue the program. FDA considers totality of evidence.

**Red Flags for Regulatory Risk:**
- Parallel trial p-value 0.04-0.06 (barely hit or barely missed)
- RW delta small in clinical terms even if stat sig
- No signal on secondary endpoints
- Safety concerns require strong efficacy to justify

**Application:** When assessing PoS, distinguish:
- P(hit stats) - Can we get p<0.05?
- P(approval | hit stats) - Will FDA approve even if we hit?

In weak efficacy scenarios, P(approval | hit stats) < 100%.
