# Novel Target Safety Assessment

Framework for evaluating safety risk for first-in-class drugs against poorly characterized targets.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| First-in-class mechanism with no clinical precedent | Yes |
| Target biology not well characterized | Yes |
| Structural similarity to known toxic targets | Yes |
| Assessing repro tox, developmental tox risk | Yes |
| Management claims target is "safe" based on preclinical | Yes - verify |

---

## Framework 1: Genetic Essentiality Assessment

### The Question
Is this target essential for normal cell function?

### Primary Tool: DepMap
DepMap (Dependency Map) screens genetic knockout effects across hundreds of cancer cell lines over 14-21 days.

### Interpreting Results

| DepMap Result | Interpretation | Safety Signal |
|---------------|----------------|---------------|
| KO is benign across cell lines | Target not essential for proliferation | Positive |
| KO lethal in subset of lines | May have tissue-specific toxicity | Caution |
| KO lethal across most lines | Essential gene; high tox risk | Red flag |

### Limitations

| Limitation | Why It Matters |
|------------|----------------|
| Cancer cell lines only | May miss normal tissue effects |
| 14-21 day assessment | May miss chronic/developmental effects |
| Genetic KO ≠ pharmacological inhibition | Drug may have off-target effects |
| No organism-level effects | Can't assess repro, developmental, CNS |

### Supporting Data to Seek
- Conditional KO mice phenotype
- Proliferation assays across cell types
- Phosphoproteomics for pathway effects

---

## Framework 2: Clinical Precedent Analysis

### The Question
If another drug has hit this target in humans, what can we learn about safety?

### The Selectivity Confound
When a multi-target drug has hit your target clinically, the observed toxicity may not be due to your target.

### Selectivity Gap Analysis

| Scenario | Read-Through Confidence |
|----------|------------------------|
| Precedent drug equipotent on your target | High - relevant signal |
| Precedent drug 10x more potent on other targets | Medium - confounded |
| Precedent drug 100x+ more potent on other targets | Low - likely not your target's effect |

### Validation Test
If other drugs in the same class cause the same toxicity but DON'T hit your target, the toxicity is likely class-related, not target-related.

### Questions to Ask
1. Does the precedent drug hit your target?
2. Does it cause the toxicity of concern?
3. What's the potency gap between your target and its primary targets?
4. Do other drugs in the class (without your target) show the same toxicity?

---

## Framework 3: Structural Homolog Risk

### The Question
Does your target share structural similarity with a known toxic protein?

### Why It Matters
Drugs designed against your target may inadvertently inhibit structurally similar proteins with different (toxic) biology.

### Questions to Ask
1. What proteins share structural homology with your target?
2. What happens when those homologs are inhibited?
3. How selective is the drug for target vs. homologs?
4. Has selectivity been tested in relevant assays?

### Selectivity Requirements by Homolog Risk

| Homolog Toxicity Profile | Required Selectivity |
|--------------------------|---------------------|
| Homolog is benign | Low bar - 10x may suffice |
| Homolog causes proliferation effects | High bar - 100x+ needed |
| Homolog is essential gene | Very high bar - may be undruggable |

---

## Framework 4: Evidence Hierarchy for Mechanism Claims

### Ranking Evidence Quality

| Evidence Type | Quality | Why |
|---------------|---------|-----|
| **Single siRNA/shRNA** | Low | Off-target effects common; no rescue control |
| **siRNA with rescue experiment** | Medium | Proves specificity of knockdown |
| **CRISPR genetic KO** | Medium-High | Cleaner than RNAi |
| **DepMap (hundreds of lines)** | High | Unbiased, large scale |
| **Phosphoproteomics** | High | Functional readout of pathway effects |
| **Conditional KO mice** | High | Organism-level, tissue-specific |
| **Clinical data** | Highest | Human relevance confirmed |

### Challenging Management Claims
Questions to ask when management claims target is "safe":
1. What's the evidence for the safety concern?
2. Was it properly controlled (rescue experiments)?
3. Has it been replicated across multiple cell lines?
4. Does DepMap/genetic KO support or refute it?
5. Does phosphoproteomics show the expected pathway effects?

---

## Framework 5: GLP Toxicology Hierarchy

### Study Types and What They Prove

| Study Type | What It Tests | Typical Duration |
|------------|---------------|------------------|
| **Acute tox** | Single dose, gross toxicity | Days |
| **Repeat-dose tox** | Chronic organ toxicity | 1-6 months |
| **GLP tox (rat, monkey)** | IND-enabling, organ pathology | 1-6 months |
| **EFD (embryo-fetal development)** | Teratogenicity, repro tox | Dosing during pregnancy |
| **Carcinogenicity** | Long-term cancer risk | 2 years |

### What Each Study DOESN'T Prove
- Acute tox: Doesn't address chronic effects
- Repeat-dose: Doesn't address developmental/repro
- GLP tox (no EFD): Doesn't fully address repro tox
- All preclinical: Doesn't guarantee human translation

---

## Novel Target Safety Checklist

### Genetic Essentiality
- [ ] DepMap results reviewed?
- [ ] What's the KO effect across cell lines?
- [ ] Conditional KO mice phenotype?
- [ ] Proliferation assays done?

### Clinical Precedent
- [ ] Any drugs that hit this target in clinic?
- [ ] If yes, what's the selectivity gap?
- [ ] Can toxicity be attributed to your target or confounders?
- [ ] Do other drugs in class (without your target) have same tox?

### Structural Risk
- [ ] What proteins share structural homology?
- [ ] What's the toxicity profile of those homologs?
- [ ] What's the demonstrated selectivity?

### Regulatory Studies
- [ ] GLP tox completed? Results?
- [ ] EFD studies completed? Results?
- [ ] Carcinogenicity studies needed?

### Evidence Quality
- [ ] Are mechanism claims well-controlled?
- [ ] Has data been replicated across multiple systems?
- [ ] Any contradictory evidence?

---

## PoS Adjustments

| Safety Assessment | PoS Adjustment |
|-------------------|---------------|
| DepMap benign + clean GLP + no structural risk | Neutral |
| DepMap benign but EFD studies pending | -5% (uncertainty) |
| Structural homolog to toxic protein, high selectivity shown | -5% |
| Structural homolog to toxic protein, selectivity uncertain | -10-15% |
| DepMap shows some lethality in subset of lines | -10% |
| Mechanism literature is conflicting/poorly controlled | -5% |
| Dirty drug precedent suggests target-related tox | -15-20% |
| First-in-class, no human data on target | -10% baseline |

---

## Output Template

```
═══════════════════════════════════════════════════════════════
NOVEL TARGET SAFETY ASSESSMENT
Drug: [Name] | Target: [Target] | Mechanism: [MOA]
═══════════════════════════════════════════════════════════════

GENETIC ESSENTIALITY:
│ DepMap KO effect │ [Benign/Partial/Lethal] │
│ Conditional KO mice │ [Normal/Abnormal/Not done] │
│ Proliferation assays │ [No effect/Effect seen] │
│ Phosphoproteomics │ [Clean/Concerning/Not done] │

CLINICAL PRECEDENT:
│ Drugs that hit target │ [List] │
│ Selectivity gap │ [Equipotent/10x/100x+] │
│ Attributable to target? │ [Yes/No/Confounded] │

STRUCTURAL RISK:
│ Homologous proteins │ [List] │
│ Homolog toxicity │ [Benign/Toxic] │
│ Demonstrated selectivity │ [X-fold] │

REGULATORY STUDIES:
│ GLP tox │ [Clean/Findings/Pending] │
│ EFD studies │ [Clean/Findings/Pending] │

EVIDENCE QUALITY:
│ Mechanism claims │ [Well-controlled/Weak] │
│ Data replication │ [Yes/No] │

SAFETY PoS ADJUSTMENT: [+/- X%]
RATIONALE: [Why]
═══════════════════════════════════════════════════════════════
```

---

## Case Studies

*Case studies illustrate how the frameworks above are applied to specific situations.*

### Case Study 1: GLUE/NEK7 (Inflammasome Inhibitor)

**Context:** NEK7 degrader for inflammatory diseases. Safety concern around NEK7's potential role in mitosis.

**Framework 1 (Genetic Essentiality):**
- DepMap: KO benign across hundreds of cell lines (vs CDK1 which is lethal) ✓
- Conditional KO mice: Generally normal ✓
- Proliferation assays: No effect across 95 cell lines up to 10µM ✓
- Assessment: Target is non-essential

**Framework 2 (Clinical Precedent):**
- Entrectinib hits NEK7 and causes repro tox
- Selectivity gap: TRK potency >> NEK7 (100x+) → confounded
- Validation test: Other TRK inhibitors (larotrectinib, repotrectinib) cause same repro tox but don't hit NEK7
- Assessment: Repro tox is TRK class effect, not NEK7

**Framework 3 (Structural Homolog):**
- NEK7 shares structure with GSPT1
- GSPT1 inhibition causes proliferation effects
- Required: High selectivity (100x+)
- Assessment: Needs verification of selectivity

**Framework 4 (Evidence Quality):**
- Literature claims on NEK7/mitosis: Low quality (single siRNA, no rescue)
- Company data: High quality (DepMap, phosphoproteomics, large cell panels)
- Assessment: Company data more reliable than literature concerns

**Framework 5 (Regulatory Tox):**
- GLP tox (rat, monkey): Clean ✓
- EFD studies: Scheduled, not complete
- Assessment: EFD is remaining key gate

**Overall Assessment:** Favorable safety profile. Apply -5% PoS adjustment for EFD uncertainty.

---

## Key Principles

1. **DepMap is your friend** - Genetic KO data across cell lines is unbiased safety signal
2. **Dirty drugs confound** - Selectivity gap determines read-through confidence
3. **Structural homologs matter** - Similar structure to toxic protein = selectivity is critical
4. **Evidence hierarchy** - Single siRNA < rescue experiments < DepMap < clinical data
5. **GLP tox ≠ full de-risk** - EFD studies are definitive for repro tox
6. **Management will minimize risk** - Verify their claims against primary data
