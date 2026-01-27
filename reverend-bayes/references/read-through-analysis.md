# Read-Through Analysis Framework

How to use evidence from one drug/indication to predict outcomes in another. This is distinct from single-trial PoS assessment.

---

## When to Use Read-Through Analysis

| Situation | Use This Framework |
|-----------|-------------------|
| Drug A in Indication X succeeded → What does this mean for Drug B in Indication X? | Yes |
| Drug A in Indication X succeeded → What does this mean for Drug A in Indication Y? | Yes |
| Drug A in Indication X failed → Is Drug B in Indication X still viable? | Yes |
| Competitor readout → Update PoS for your drug | Yes |
| Single drug, single indication, no external data | No - use standard PoS framework |

---

## The Weiliang Method: Mechanistic Read-Through

### Core Principle

**The pathway matters more than the specific drug.**

If Drug A works via Pathway → Biomarker → Clinical Outcome, then Drug B working via the same pathway should also work, IF:
1. Drug B achieves similar or better biomarker effect
2. The population is similar
3. The biomarker-outcome relationship is causal (not just correlative)

### Framework Structure

```
1. ESTABLISH THE MECHANISM CHAIN
   Drug → Target → Biomarker → Clinical Outcome
   
2. VALIDATE THE CHAIN WITH PRIOR DATA
   Did biomarker responders have better outcomes than non-responders?
   
3. COMPARE YOUR DRUG TO THE VALIDATED DRUG
   Does your drug achieve the same biomarker threshold?
   
4. ADJUST FOR POPULATION DIFFERENCES
   Is your population easier or harder than the validated population?
   
5. ASSIGN READ-THROUGH PoS
   Base rate from validated trial × adjustments
```

---

## Worked Example: ZEUS Read-Through from CANTOS

### Step 1: Establish the Mechanism Chain

```
Canakinumab (IL-1β mAb) → IL-1β inhibition → IL-6 ↓ → CRP ↓ → CV events ↓
Ziltivekimab (IL-6 mAb) → IL-6 inhibition → CRP ↓ → CV events ↓
```

**Key insight:** Both drugs converge on CRP reduction. If CRP reduction drives CV benefit, then ziltivekimab should work too.

### Step 2: Validate the Chain with CANTOS Subgroups

| Subgroup | HR | Interpretation |
|----------|----|-----------------| 
| CRP < 2 mg/L achieved | 0.75 | Biomarker responders did better |
| CRP > 2 mg/L | 0.95 | Non-responders had minimal benefit |
| Overall | 0.85 | Blended effect |

**Validation:** The CRP threshold matters. Achieving CRP < 2 mg/L is the mechanistic driver, not just "being on drug."

### Step 3: Compare Ziltivekimab to Canakinumab on Biomarker

| Drug | CRP Reduction | Lp(a) Reduction |
|------|---------------|-----------------|
| Canakinumab 150mg | ~40% | 23% |
| Ziltivekimab | ~80-90% | ~20% |

**Ziltivekimab achieves MORE CRP reduction.** If CRP is the driver, ziltivekimab should work at least as well.

### Step 4: Adjust for Population Differences

| Factor | CANTOS | ZEUS | Impact |
|--------|--------|------|--------|
| CKD required | No (subgroup only) | Yes | ZEUS is enriched for responders (CKD subgroup had HR 0.82 vs 0.86) |
| CRP required | Yes (>2 mg/L) | Yes (>2 mg/L) | Similar |
| T2D prevalence | ~40% | Higher | Negative (T2D subgroup did worse in CANTOS) |
| ASCVD required | Yes | Yes | Similar |

**Net adjustment:** CKD enrichment is positive; T2D prevalence is negative. Roughly offsetting.

### Step 5: Assign Read-Through PoS

```
CANTOS overall HR: 0.85 (p<0.001)
CANTOS CKD subgroup HR: 0.82
ZEUS stats sig bar: HR < 0.89

Base PoS from CANTOS CKD: ~75%
- Ziltivekimab has better CRP reduction: +5%
- Higher T2D in ZEUS: -5%
- Stats bar is 0.89 (easier than CANTOS 0.85): +5%

Final PoS: ~75-80%
```

---

## Comp Dismissal: When NOT to Read Through

### The Losmapimod Example

Losmapimod (p38/MK2 inhibitor) failed in AMI CVOT. Is this negative for IL-6 inhibitors?

**Answer: No.** Here's how to dismiss a comp:

| Question | Losmapimod | IL-6 inhibitors |
|----------|------------|-----------------|
| Does drug sustain biomarker effect? | No - tachyphylaxis (CRP merged with placebo at 12 weeks) | Yes - sustained CRP reduction |
| Did drug work in other CRP-elevated populations? | No - failed in COPD and RA | N/A (different drug) |
| Is mechanism validated? | No - p38/MK2 class has tachyphylaxis issues | Yes - IL-1β/IL-6 axis validated |

**Dismissal criteria met:**
1. Drug didn't achieve sustained biomarker effect
2. Drug failed in other elevated-CRP populations
3. Mechanism class has known issues (tachyphylaxis)

### When to Dismiss a Comp

A failed trial is NOT relevant read-through if:

- [ ] Drug didn't achieve the biomarker threshold that predicted success
- [ ] Drug failed due to drug-specific issues (tachyphylaxis, PK problems, tolerability)
- [ ] Mechanism is fundamentally different (different pathway)
- [ ] Population was not enriched for the biomarker-outcome relationship
- [ ] Trial was underpowered (failed on stats, not biology)

### When a Failed Trial IS Relevant

A failed trial IS relevant read-through if:

- [ ] Drug achieved biomarker threshold but outcome didn't follow → biomarker may not be causal
- [ ] Drug and mechanism are similar to yours
- [ ] Population was appropriately enriched
- [ ] Trial was well-powered
- [ ] No drug-specific explanation for failure

---

## Biomarker Threshold Analysis

### The Key Question

Not "did the biomarker move?" but "did it cross the threshold that predicts benefit?"

### Framework

1. **Identify the threshold from prior data**
   - CANTOS: CRP < 2 mg/L → HR 0.75
   - CANTOS: IL-6 < 1.65 ng/L associated with benefit

2. **Assess whether your drug can achieve it**
   - GLUE: Achieved IL-6 < 1.65 ng/L from higher baseline (2.58 ng/L)
   - This is endogenous plasma, not ex vivo stimulation

3. **Assign PoS uplift if threshold is achievable**
   - If drug achieves threshold: Use responder subgroup HR as base
   - If drug may not achieve threshold: Use overall HR or non-responder HR

### Example Table

| Drug | Baseline IL-6 | Achieved IL-6 | Threshold (1.65 ng/L) | PoS Adjustment |
|------|---------------|---------------|----------------------|----------------|
| Canakinumab | Lower | ~1.65 | At threshold | Base |
| GLUE | 2.58 ng/L | < 1.65 | Below threshold | +5-10% |

---

## Subgroup Mining: Rules of Engagement

### What Subgroups Tell You

| Subgroup Result | Interpretation |
|-----------------|----------------|
| Biomarker responders >> non-responders | Biomarker is likely causal driver |
| High-risk subgroup does better | Drug works via risk factor modification |
| High-risk subgroup does worse | Drug may have ceiling effect or adverse interaction |
| Subgroup with feature X does better | Your trial should enrich for X |

### Weiliang's Subgroup Extractions from CANTOS

| Subgroup | HR | Implication for ZEUS |
|----------|----|-----------------------| 
| CKD (eGFR < 60) | 0.82 | ZEUS enriches for CKD → positive |
| Non-CKD | 0.86 | Less relevant to ZEUS |
| CRP < 2 achieved | 0.75 | Ziltivekimab achieves more CRP reduction → positive |
| CRP > 2 | 0.95 | Non-responders don't benefit |
| T2D | Worse than non-T2D | ZEUS has more T2D → negative |
| Prior HF (300mg) | 0.75 | Supports HERMES indication |

### Rules for Using Subgroups

**DO:**
- Use subgroups that match your trial's enrichment criteria
- Use biomarker responder subgroups to validate mechanism
- Adjust PoS based on subgroup direction

**DON'T:**
- Use subgroups as primary evidence (underpowered)
- Cherry-pick only favorable subgroups
- Ignore subgroups that go against your thesis

---

## Cross-Indication Read-Through

### Same Drug, Different Indication

When Drug A succeeds in Indication X, what's the read-through to Indication Y?

| Question | Positive Read-Through | Negative Read-Through |
|----------|----------------------|----------------------|
| Is mechanism relevant to Y? | Same pathway drives Y | Different pathway in Y |
| Does drug achieve threshold in Y population? | Yes | No |
| Has the indication been validated before? | Other drugs worked in Y | Indication historically hard |
| Is the bar achievable? | Similar to X | Much higher than X |

### Example: ZEUS → ARTEMIS → HERMES

| Trial | Indication | Weiliang PoS | Rationale |
|-------|------------|--------------|-----------|
| ZEUS | CKD + ASCVD + CRP | 75% | CKD subgroup in CANTOS had HR 0.82; population enriched for responders |
| ARTEMIS | Acute MI | 50% | AMI is hard; colchicine 1/2; CRP naturally falls post-MI so less room for drug effect |
| HERMES | HF + CRP | 60% | CANTOS HF subgroup had HR 0.75 at high dose; supportive but small |

**Order matters:** ZEUS reading out first is positive because it's the highest-PoS study. If ZEUS hits, ARTEMIS and HERMES get PoS uplift.

---

## Statistical Power Awareness

### Know the Bar

| Trial | HR Needed for Significance | Current Estimate | Gap |
|-------|---------------------------|------------------|-----|
| ZEUS | < 0.89 | 0.82 (from CANTOS CKD) | Comfortable |
| ARTEMIS | < 0.87 | Uncertain | Tight |
| HERMES | < 0.87 | 0.75 (CANTOS HF, 300mg only) | May be ok |

### Power Implications

- If expected HR is close to significance bar → high risk of "trend but not significant"
- COLCOT example: HR 0.77 but p=0.02 only ("prob not big enough")
- Always check if the positive comp was adequately powered

---

## Read-Through PoS Template

```
═══════════════════════════════════════════════════════════════
READ-THROUGH ANALYSIS
Target Trial: [Your trial]
Reference Trial: [The comp with prior data]
═══════════════════════════════════════════════════════════════

MECHANISM CHAIN COMPARISON:
Reference: [Drug] → [Target] → [Biomarker] → [Outcome]
Target:    [Drug] → [Target] → [Biomarker] → [Outcome]
Convergence point: [Where the chains meet]

BIOMARKER THRESHOLD ANALYSIS:
Reference threshold for benefit: [X]
Your drug achieves: [Y]
Assessment: [Above/At/Below threshold]

POPULATION COMPARISON:
| Factor | Reference | Target | Impact |
|--------|-----------|--------|--------|
| [Factor 1] | | | |
| [Factor 2] | | | |

SUBGROUP RELEVANCE:
Most relevant subgroup from reference: [X]
Subgroup HR: [Y]
Applicability to target: [High/Medium/Low]

COMP DISMISSAL CHECK:
Potential negative comp: [Failed trial]
Dismissal reason: [Drug-specific / Underpowered / Different mechanism]
Relevant to target? [Yes/No]

PoS CALCULATION:
Base rate from reference: [X%]
Adjustments:
  - [Positive factor]: +[Y%]
  - [Negative factor]: -[Z%]
Final read-through PoS: [A%]

STATS BAR CHECK:
HR needed for significance: [X]
Expected HR from read-through: [Y]
Gap: [Comfortable / Tight / Risky]
═══════════════════════════════════════════════════════════════
```

---

## Integration with Standard PoS Framework

Read-through analysis is **complementary** to the 6-pillar PoS framework:

| Pillar | How Read-Through Informs It |
|--------|----------------------------|
| 1. Trial Design | Reference trial design as template |
| 2. Baseline Population | Subgroup matching |
| 3. Comparator Arm | Placebo rates from reference |
| 4. Efficacy Signal | Biomarker threshold validation |
| 5. Competitive Context | Reference trial sets bar |
| 6. Execution Risk | Reference trial's operational learnings |

**When you have strong read-through evidence, it should ANCHOR your PoS estimate.** The 6-pillar scoring becomes an adjustment around that anchor, not the primary driver.
