# Therapeutic Area: Ophthalmology (Retinal Disease)

Clinical trial analysis patterns for wet AMD, DME, and other retinal indications.

---

## Source Cases

| Ticker | Drug | Indication | Key Pattern | Analyst |
|--------|------|------------|-------------|---------|
| OCUL | Axpaxli (OTX-TKI) | wAMD, DME | Rescue paradox, baseline confound | ZH, RP, MM, MZ |
| EYPT | — | wAMD, DME | Maintenance potency vs naïve | RP |
| KOD | Tarcocimab | wAMD | Dosing inflexibility failure | MZ, MM |

---

## Pattern 1: Rescue Paradox (MM)

### The Problem

In trials with rescue design, a drug that **delays rescue but doesn't prevent it** may show:
- ✅ Better rescue-free rate (primary endpoint hit)
- ❌ Worse BCVA (because rescue injections would have helped more)

This creates the "stat sig but disappointing" scenario.

### The Math

Assume:
- Implant arm: 30% require rescue
- Placebo arm: 60% require rescue
- Rescued patients: BCVA returns to baseline (0 letters)
- Non-rescued implant patients: -4 letters (drug less effective than anti-VEGF)
- Non-rescued placebo: 0 letters (by definition, didn't need rescue)

| Arm | Rescued % | BCVA (Rescued) | BCVA (Non-Rescued) | Weighted BCVA |
|-----|-----------|----------------|--------------------|--------------:|
| Implant | 30% | 0 | -4 | **-2.8** |
| Placebo | 60% | 0 | 0 | **0** |
| **Net** | -30% | | | **-2.8 letters worse** |

**Translation:** Implant shows 30pp better rescue-free rate but 2.8 letter worse BCVA.

### When This Applies

- Trial uses rescue-permitted design
- Study drug is less potent than rescue therapy (anti-VEGF IVT)
- Primary is rescue-free rate, secondary is BCVA

### Checklist Before Going Long on Rescue Design

1. **Is study drug MORE effective than rescue therapy?**
   - If no → rescue paradox risk
2. **Model BCVA trajectory assuming delayed but eventual rescue**
   - How much BCVA loss occurs before rescue threshold?
3. **What's the rescue threshold?**
   - Strict threshold (small BCVA/CST change) → earlier rescue → less paradox
   - Liberal threshold → more drift before rescue → more paradox
4. **Is rescue truly prevented or just delayed?**
   - Check KM curves at extended timepoints (9m, 12m)
   - If curves converge at longer timepoints, drug only delays

### OCUL Specific Application (MM)

> "Everyone is super adequately dosed with Eylea at run-in, so their BL BCVA is maxed out at its peak. The implant helps you barely survive, and your BCVA drips slowly down to the -15 threshold before rescue."

The problem: patients start at peak BCVA (Eylea-loaded), implant can't maintain → gradual drift → eventual rescue. But by the time rescue happens, BCVA has fallen.

---

## Pattern 2: Baseline Severity Confound (MZ)

### The Problem

Phase 1 data from sick populations doesn't predict Phase 3 in milder populations.

### OCUL Example

| Study | Baseline CST | Population | Implication |
|-------|--------------|------------|-------------|
| Australia Ph1 (naïve) | 570um | Very sick | Misleading efficacy signal |
| Australia Ph1 (experienced) | ~470um | Refractory | Still sicker than typical |
| US Ph1 | ~250um | Well-controlled | Relevant to maintenance |
| Other Ph3s (KOD, HD Eylea) | 350-370um | Standard naïve | Benchmark |

**Key insight (MZ):** The Australia study pooled Cohorts 1-3 (200, 400, 600ug doses), but only 600ug is used in Ph3. Pooling diluted the relevant signal.

### Why Baseline CST Matters

| Baseline CST | Expected CST Improvement | Interpretation |
|--------------|-------------------------|----------------|
| >500um | Large (-100 to -150um) | Sick patients respond well |
| 350-400um | Moderate (-75 to -100um) | Standard naïve |
| 250-300um | Small (-25 to -50um) | Already controlled, maintenance |

**Pattern:** Drugs that look impressive in very sick patients (high baseline) may underwhelm in controlled patients (low baseline).

### Cross-Study Mapping

Before comparing efficacy across studies:
1. Match on baseline CST (±50um)
2. Match on prior treatment (naïve vs experienced)
3. Match on disease severity (BCVA at entry)
4. Adjust expectations accordingly

---

## Pattern 3: Maintenance vs Induction Potency (RP)

### The Thesis

> "These drugs are better at holding the line than reversing established pathology."

Drugs can fail in naïve patients (high CST, need strong drying) but succeed in maintenance (already controlled, just need to sustain).

### Supporting Evidence

**1. KOD DAYBREAK Data:**
- When disease well-controlled, patients stretched to 16-20 weeks
- Q12W minimum interval "stretched it too far" for subset with aggressive disease
- **Implication:** Less potent drug can work if baseline is controlled

**2. Beovu Switch Study:**
- ~35um CST difference between arms
- No BCVA difference
- Same CST delta that failed in naïve KOD study worked in switch setting
- **Implication:** CST delta tolerance is different in maintenance vs naïve

**3. Eylea View 1/2 Maintenance:**
- CST delta of 10-20 units at steady state
- No difference in overall BCVA
- 2Q4 arm had only 1 letter delta over 2Q8 arm
- **Implication:** Half dose in maintenance didn't compromise efficacy much

**4. Eylea Label:**
- Monthly loading → PRN maintenance = standard practice
- **Implication:** Less drug needed to maintain than to induce

### When to Apply

Use maintenance thesis when:
- Trial design has anti-VEGF run-in (patients already controlled)
- Baseline CST is low (<300um)
- Drug is clearly less potent than standard anti-VEGF in naïve setting

Don't apply when:
- No run-in period
- Patients are naïve or have high baseline CST
- Drug claims to be as potent as anti-VEGF

### OCUL SOL-R Design (RP Thesis)

SOL-R has Eylea loading phase → patients enter Phase 3 with controlled disease → baseline CST should be ~250um (like US Ph1) → maintenance thesis applies.

---

## Pattern 4: KOD Failure Read-Through (MZ)

### What Happened

Kodiak's tarcocimab failed in wAMD despite positive biomarker signal.

### Failure Factors

| Factor | KOD | Risk for Other Implants |
|--------|-----|-------------------------|
| **Potency** | ~Eylea 0.5mg equivalent (based on CST improvement ~100um after loading) | Need to establish potency vs standard |
| **Dosing Flexibility** | None - Q3M forced regardless of response | If interval fixed, subset will be underdosed |
| **CST Improvement** | ~100um after loading | Compare to Eylea (~125um) as benchmark |

### Why Q3M Failed

> "Some pts required more frequent dosing, but they had the option of discontinuing or stretching till next scheduled dosing. That's why Q3M dosing did really poorly."

**Pattern:** Fixed interval dosing fails if any meaningful subset needs more frequent treatment. The aggressive disease patients drive the miss.

### Pre-Screening Checklist

Before going long on retinal implant:
1. What's the potency vs Eylea (based on CST improvement)?
2. Is dosing flexible or fixed?
3. What happens to patients who need more frequent dosing?
4. What's the rescue/re-treatment criterion?

### OCUL Risk (MZ observation)

> "OCUL amended SOL-R rescue dosing criterion last year and made it stricter, which is not helping imo."

Stricter rescue criteria = fewer patients get retreatment when needed = higher risk of KOD-type failure in subset.

---

## Pattern 5: Drug Delivery Uncertainty (MM)

### The Question

Is the drug actually reaching the target tissue?

### OCUL Specific Concern (MM)

> "There also remains the outstanding questions about whether the drug is really getting to the active site because it's highly protein and melanin bound and must diffuse through protein and melanin rich tissues before getting to the site of action."

### When to Flag Drug Delivery Risk

- Novel delivery mechanism (implant, injection depot)
- Drug is highly protein-bound
- Target tissue has barriers (melanin, protein)
- PK data doesn't measure drug at site of action
- Efficacy-exposure relationship is weak/unclear

### What to Look For

- PK studies measuring drug at target (not just plasma)
- Correlation between local concentration and biomarker response
- Preclinical distribution studies
- Any red flags from imaging (drug accumulation, clearance)

---

## Key Endpoints in Retinal Disease

### Primary Endpoints

| Endpoint | Definition | What It Measures |
|----------|------------|------------------|
| **Rescue-Free Rate (RFR)** | % patients not requiring rescue treatment | Durability |
| **BCVA Change** | Letters gained/lost from baseline | Visual function |
| **Time to First Rescue** | Days until rescue needed | Durability |

### Secondary Endpoints

| Endpoint | Definition | What It Measures |
|----------|------------|------------------|
| **CST (Central Subfield Thickness)** | Retinal thickness in microns | Anatomic response (drying) |
| **Total Fluid** | SRF + IRF volume | Anatomic response |
| **Injection Burden** | Number of injections over period | Treatment convenience |

### Endpoint Hierarchy

1. **Regulators care most about:** BCVA (the outcome patients experience)
2. **Durability trials focus on:** RFR and time to rescue
3. **Anatomic endpoints (CST, fluid):** Supporting data, not primary

### Endpoint Traps

| Trap | Description | Example |
|------|-------------|---------|
| **RFR without BCVA** | Good durability but worse vision | Rescue paradox |
| **CST without BCVA** | Drug dries retina but vision unchanged | CST-BCVA disconnect |
| **Per protocol vs ITT** | Per protocol inflates efficacy | OCUL Ph1 showed 100% PP vs 73% investigator |

---

## Competitive Landscape (wAMD/DME)

### Current Standard of Care

| Drug | Mechanism | Dosing | Notes |
|------|-----------|--------|-------|
| **Eylea (aflibercept)** | Anti-VEGF | Q8W after loading | Gold standard |
| **Vabysmo (faricimab)** | Anti-VEGF/Ang-2 | Up to Q16W | Premium durability |
| **Lucentis (ranibizumab)** | Anti-VEGF | Monthly or PRN | Older, less durable |
| **Beovu (brolucizumab)** | Anti-VEGF | Q8-12W | IOI safety concerns |

### Emerging Competitors

| Drug | Company | Mechanism | Differentiation |
|------|---------|-----------|-----------------|
| **Axpaxli (OTX-TKI)** | OCUL | TKI implant | 6-month durability target |
| **EYP-1901** | EYPT | Tyrosine kinase implant | Durability |
| **HD Eylea** | Regeneron | Higher dose anti-VEGF | Q12-16W |

### Key Commercial Question

For any new entrant: Does durability improvement justify adoption friction?
- New implant requires procedural training
- Surgeons comfortable with current injectables
- Insurance/access considerations

---

## PoS Framework for Retinal Trials

### Phase 3 Non-Inferiority (vs anti-VEGF)

| Factor | Assessment |
|--------|------------|
| Phase 2 BCVA delta vs control | >-2 letters: Likely NI. >-5 letters: Risky |
| Phase 2 CST maintenance | Within 25um: Good. >50um worse: Risky |
| Phase 2 rescue-free rate | >70%: Good. <50%: Risky |
| KOD-like risks (dosing, potency) | Any present: Reduce PoS by 15-20% |

### Phase 3 Superiority (vs single dose)

| Factor | Assessment |
|--------|------------|
| Control arm (single anti-VEGF dose) | Should be ~100% failure at 6m |
| Drug rescue-free rate target | >65% = success |
| BCVA maintenance requirement | Stay within 2-3 letters of control |

### OCUL SOL-1 PoS Matrix

| Analyst | PoS | Rationale |
|---------|-----|-----------|
| ZH | 95% | Ph1 100% RFR per protocol; will report PP if needed |
| RP | High | Maintenance thesis; run-in design appropriate |
| MM | Low (<50%?) | Rescue paradox; BCVA will miss |
| MZ | 60% | Australia Ph1 flawed; dose pooling concern |

---

## Checklist: Retinal Trial Evaluation

```
RETINAL TRIAL ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

BASELINE CHARACTERISTICS:
□ Baseline CST: ______um (250-300 = controlled, >400 = sick)
□ Prior treatment: [naïve / experienced / switch]
□ Baseline BCVA: ______ letters
□ Does baseline match relevant comparator trials? [Y/N]

POTENCY ASSESSMENT:
□ Phase 2 CST improvement vs Eylea: _____um
□ Estimated potency equivalent: _____
□ Phase 2 BCVA maintenance: _____ letters vs control
□ Drug delivery concerns? [Y/N]

TRIAL DESIGN:
□ Primary endpoint: [RFR / BCVA / Time to rescue]
□ Dosing flexibility: [Fixed / PRN / Rescue-permitted]
□ Rescue threshold: _____
□ Run-in period: [Y/N] - If yes, patients are controlled

RESCUE PARADOX CHECK:
□ Is study drug less potent than rescue therapy? [Y/N]
□ If yes, model BCVA with delayed rescue: _____
□ Expected RFR: _____% vs Control RFR: _____%
□ Expected BCVA delta: _____ letters (positive = drug better)

KOD FAILURE FACTORS:
□ Dosing flexibility adequate? [Y/N]
□ Stricter rescue criteria than competitors? [Y/N]
□ Clear potency data vs standard? [Y/N]

OVERALL POS: _____%
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## References

- OCUL SOL-1 Street Expects (Adrian, Dec 2025)
- OCUL Internal Debate (ZH, RP, MM, MZ - Jan 7, 2026)
- KOD DAYBREAK trial data
- Eylea View 1/2 trial data
- Beovu switch study (Helsinki)
