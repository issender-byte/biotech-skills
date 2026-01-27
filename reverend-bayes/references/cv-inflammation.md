# Cardiovascular Outcomes Trials (CVOTs) - Inflammation Axis

Reference module for CVOTs targeting inflammatory pathways. Based on CANTOS, colchicine trials, and IL-6 program analyses.

---

## The CRP-CV Benefit Mechanism

### Validated Chain (CANTOS)

```
IL-1β inhibition (canakinumab)
    ↓
IL-6 reduction
    ↓
CRP reduction (target: < 2 mg/L)
    ↓
CV event reduction (MACE)
    ↓
HR ~0.75 in responders
```

### Key Insight from CANTOS Subgroups

| Achieved CRP | HR | p-value |
|--------------|----|---------| 
| < 2 mg/L | 0.75 | Significant |
| > 2 mg/L | 0.95 | Not significant |
| Overall | 0.85 | p < 0.001 |

**The threshold matters.** Achieving CRP < 2 mg/L is what drives benefit, not just "being on an anti-inflammatory."

---

## CVOT Population Benchmarks

### ASCVD + CKD + Elevated CRP (ZEUS-like)

| Parameter | CANTOS CKD Subgroup | ZEUS Population |
|-----------|---------------------|-----------------|
| eGFR | < 60 | < 60 required |
| CRP required | > 2 mg/L | > 2 mg/L |
| ASCVD | Yes | Yes |
| HR achieved | 0.82 | Target |
| IL-6 baseline | Lower | Similar |

**Implication:** ZEUS is enriched for the subgroup that did best in CANTOS.

### Acute MI (ARTEMIS-like)

| Trial | Drug | HR | Notes |
|-------|------|----|---------| 
| COLCOT | Colchicine | 0.77 | p=0.02; marginally powered |
| CLEAR SYNERGY | Colchicine | ~1.0 | Failed |
| Losmapimod AMI | p38 inhibitor | Failed | Tachyphylaxis - CRP merged at 12 weeks |

**Implication:** AMI is hard. CRP naturally falls post-MI, so drug effect is compressed. 50% PoS base rate.

### Heart Failure + Elevated CRP (HERMES-like)

| Subgroup | CANTOS HR | Notes |
|----------|-----------|-------| 
| Prior HF, 300mg | 0.75 | Not statistically significant |
| Prior HF, 150mg | No signal | Lower doses didn't work |
| Prior HF, 50mg | No signal | |

**Implication:** May need higher IL-6 suppression for HF benefit. Dose-response suggests mechanism is real but threshold is high.

---

## Biomarker Thresholds

### CRP

| Threshold | Source | Implication |
|-----------|--------|-------------|
| < 2 mg/L | CANTOS | Responder threshold for CV benefit |
| 40% reduction | Colchicine (LoDoCo2) | Associated with secondary prevention benefit |
| 70-90% reduction | IL-6 mAbs | Best-in-class reduction |

### IL-6

| Threshold | Source | Implication |
|-----------|--------|-------------|
| < 1.65 ng/L | CANTOS median | Below this associated with benefit |
| Endogenous vs ex vivo | Critical distinction | Ex vivo LPS stimulation ≠ true plasma levels |

### Lp(a)

| Drug | Lp(a) Reduction | Contribution to CVOT Benefit |
|------|-----------------|------------------------------|
| Canakinumab | 23% | ~6% of 14% total benefit (post-hoc) |
| Ziltivekimab | ~20% | Similar expected contribution |

---

## Comp Dismissal Framework for CV

### When to Dismiss a Failed CV Trial

**Losmapimod (p38/MK2) Example:**

| Question | Answer | Dismissal? |
|----------|--------|------------|
| Did drug sustain CRP reduction? | No - merged with placebo at 12 weeks | YES |
| Did drug fail in other inflammation populations? | Yes - COPD, RA | YES |
| Is mechanism class problematic? | Yes - p38/MK2 tachyphylaxis known | YES |
| Is mechanism fundamentally different? | Yes - not IL-1/IL-6 axis | YES |

**Verdict:** Losmapimod failure is NOT read-through for IL-6 inhibitors.

### When a Failed Trial IS Relevant

A CV trial failure is relevant read-through if:
- Drug achieved sustained CRP reduction but MACE didn't improve
- Population was appropriately enriched (CRP > 2 mg/L)
- Mechanism is similar (same pathway)
- Trial was adequately powered

---

## CVOT Statistical Considerations

### Typical Significance Bars

| Trial Type | HR Needed | Notes |
|------------|-----------|-------|
| Large secondary prevention | < 0.85-0.90 | Depends on events, power |
| CKD enriched | < 0.89 | ZEUS bar |
| Acute MI | < 0.87 | ARTEMIS bar |
| HF | < 0.87 | HERMES bar |

### Power Considerations

- COLCOT: HR 0.77 but p=0.02 → "probably not big enough"
- Need to check if expected HR is comfortably below significance bar
- Close to bar = high risk of "trend but miss"

---

## Cross-Indication Read-Through

### If ZEUS (ASCVD/CKD/CRP) Succeeds:

| Indication | Read-Through PoS | Rationale |
|------------|------------------|-----------|
| Secondary prevention (no CKD) | +10-15% | Mechanism validated |
| Acute MI (ARTEMIS) | +10-15% | But indication still hard |
| HF (HERMES) | +10-15% | Supportive of CANTOS HF subgroup |

### If ZEUS Fails:

| Indication | Read-Through Impact | Rationale |
|------------|---------------------|-----------|
| Other IL-6 programs | Major negative | If enriched population fails, harder populations unlikely |
| IL-1 programs | Modest negative | Different point in pathway |
| NLRP3 programs | Depends on CRP achievement | If CRP threshold achieved, still potentially viable |

---

## PoS Framework for CV Inflammation

### Base Rates by Indication

| Population | Base PoS | Key Driver |
|------------|----------|------------|
| ASCVD + CKD + CRP > 2 | 70-80% | CANTOS CKD subgroup validated |
| ASCVD + CRP > 2 (no CKD) | 60-70% | CANTOS overall |
| Acute MI | 45-55% | Mixed colchicine results |
| HF + elevated CRP | 55-65% | CANTOS HF subgroup supportive but small |

### Adjustment Factors

**Increase PoS if:**
- Drug achieves more CRP reduction than canakinumab (+5-10%)
- Population enriched for CKD or other responding subgroup (+5%)
- Multiple biomarkers of inflammation reduced (+5%)

**Decrease PoS if:**
- Higher T2D prevalence than CANTOS (-5%)
- Drug has tolerability/adherence concerns (-5-10%)
- Stats bar is tight (expected HR close to threshold) (-5%)
- Indication historically hard (AMI) (-10%)

---

## Integration with Main PoS Framework

For CV inflammation trials:

1. **Use read-through as anchor** - CANTOS provides strong prior
2. **Pillar scoring adjusts the anchor:**
   - Trial design: Is enrichment strategy sound?
   - Population: Matches CANTOS subgroup that worked?
   - Efficacy signal: Does Phase 2 CRP reduction predict threshold achievement?
   - Competitive: Is canakinumab or colchicine the relevant comp?
3. **Stats bar check** - Is expected HR comfortably below threshold?
