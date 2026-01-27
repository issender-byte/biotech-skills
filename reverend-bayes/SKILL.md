---
name: reverend-bayes
description: "Clinical trial probability of success (PoS) assessment focused on REGULATORY outcome. Named for Thomas Bayes - we update priors with evidence. Use when analyzing whether a trial will achieve its primary endpoint and support approval. Does NOT assess commercial potential or valuation - use john-snow and graham skills for those. Triggers: trial analysis, Phase 2/3 probability, endpoint analysis, placebo response, power assumptions, biomarker coherence, read-through from prior trials."
---

# Reverend Bayes: Clinical Trial PoS Assessment

*"In the face of uncertainty, we update our beliefs with evidence."*

**Scope:** Probability of regulatory success (trial hits primary endpoint, supports approval).

**Out of scope:** Peak sales, valuation, position sizing → use `john-snow` and `graham` skills.

## Output

```
PoS: [XX-YY%] for [specific regulatory outcome]
Key Debates: [3-5 uncertainties that drive the range]
Recommended Diligence: [What would narrow the range]
```

## Analytical Philosophy

Good PoS analysis:
1. **Names specific uncertainties** - Not "will it work?" but "will placebo normalize?"
2. **Benchmarks to specific trials** - Not "historical range" but "Dupixent SOLO 1/2 showed X"
3. **Checks internal consistency** - Does the data contradict itself?
4. **Takes a position** - State what you believe and why

## Framework Selection

```
START: Do you have relevant prior trial data for this mechanism?
│
├─ YES: Prior trial validates mechanism?
│  ├─ YES → Read-Through Analysis (anchor on prior, adjust)
│  └─ NO → Why did prior fail? Relevant to your drug?
│
├─ NO: Novel mechanism
│  └─ Standard 6-Pillar Framework
│
THEN: Is this single-arm or controlled?
├─ Single-arm → Cross-Trial Comparison (historical benchmark)
└─ Controlled → Standard analysis with comparator assessment
│
THEN: Are you comparing across indications or populations?
├─ YES → E-R Analysis (could exposure explain differences?)
└─ NO → Focus on internal consistency
```

## Step 1: Parameter Intake

| Parameter | Required | Flag If... |
|-----------|----------|------------|
| Drug / mechanism | Yes | Novel target |
| Indication | Yes | High placebo risk |
| Phase | Yes | - |
| Primary endpoint | Yes | Subjective endpoint |
| Sample size (N) | Yes | Underpowered |
| Randomization ratio | Yes | Changed mid-study |
| Treatment duration | Yes | Changed mid-study |
| Comparator | Yes | Active vs placebo |
| Prior treatment allowed | Yes | Affects population difficulty |
| Phase 2 data (if Phase 3) | If available | - |
| Biomarker data | If available | Disconnect with clinical |

## Step 2: Key Debates

**Before scoring pillars, name 3-5 specific uncertainties.**

Format:
```
DEBATE: [Specific question]
BULL: [What you'd need to believe]
BEAR: [What you'd need to believe]
RESOLUTION: [What data would settle it]
MY POSITION: [Clear view]
```

## Step 3: Six Pillar Analysis

### Pillar 1: Trial Design (0-10)
- Power assumptions realistic?
- Endpoint selection appropriate?
- Duration sufficient?
- Multiplicity controlled?

### Pillar 2: Baseline Population (0-10)
- Enrollment feasible?
- Comparable to Phase 2?
- Stratification appropriate?
- Prior treatment mix?

### Pillar 3: Comparator Arm (0-10)
- Placebo response vs historical benchmarks?
- Design features affecting placebo?
- Regression to mean risk?

### Pillar 4: Efficacy Signal (0-10)
- Phase 2 effect size vs historical?
- Internal consistency across cohorts?
- Dose-response present?
- Biomarker coherence?

### Pillar 5: Competitive Context (0-10)
- Regulatory precedent?
- Bar set by approved drugs?
- Evolving SOC during trial?

### Pillar 6: Execution Risk (0-10)
- Sponsor track record?
- Enrollment pace?
- Manufacturing/supply?

## Step 4: Biomarker Coherence Check

**Does biomarker kinetics match stated MOA?**

| Pattern | Score Adjustment |
|---------|-----------------|
| Biomarker precedes clinical | +1-2 |
| Biomarker correlates with clinical | 0 |
| Clinical precedes biomarker | -1-2 |
| No correlation | -2-3 |
| Biomarker contradicts expectation | -3-5 |

## Step 5: Synthesis

### Qualitative Mode
Sum pillar scores (max 60), map to PoS:
- 48-60: 55-75% PoS
- 36-47: 35-55% PoS
- 24-35: 20-40% PoS
- <24: <25% PoS

### With Read-Through
If prior trial validates mechanism, use prior as anchor:
- Prior trial PoS: X%
- Adjustments for your trial: ±Y%
- Final PoS: X ± Y%

## Deliverable: PoS Scorecard

```
═══════════════════════════════════════════════════════════════
CLINICAL TRIAL PoS ASSESSMENT
Drug: [Name] | Indication: [Indication] | Phase: [Phase]
═══════════════════════════════════════════════════════════════

PoS ESTIMATE: [XX-YY%] (Center: ZZ%)

PILLAR SCORES:
│ Pillar                    │ Score │ Key Driver              │
│ 1. Trial Design           │  /10  │                         │
│ 2. Baseline Population    │  /10  │                         │
│ 3. Comparator Arm         │  /10  │                         │
│ 4. Efficacy Signal        │  /10  │                         │
│ 5. Competitive Context    │  /10  │                         │
│ 6. Execution Risk         │  /10  │                         │
│ TOTAL                     │  /60  │                         │

BIOMARKER COHERENCE: [X/10]

KEY DEBATES:
1. [Debate]: [Position]
2. [Debate]: [Position]
3. [Debate]: [Position]

TO TOP OF RANGE: [Conditions]
TO BOTTOM OF RANGE: [Conditions]

RECOMMENDED DILIGENCE:
1. [Action to reduce uncertainty]
2. [Action to reduce uncertainty]

>>> HAND OFF TO: john-snow (for revenue) 
>>> HAND OFF TO: graham (for fair value)
═══════════════════════════════════════════════════════════════
```

## Reference Files

| File | Use When |
|------|----------|
| `references/analytical-rules.md` | **Core rules (48 total) - ALWAYS read first** |
| `references/analytical-questions.md` | Finding inconsistencies |
| `references/read-through-analysis.md` | Prior trial data exists |
| `references/cross-trial-comparison.md` | Single-arm benchmarking |
| `references/pk-pd-exposure-response.md` | Cross-indication comparison |
| `references/statistical-framework.md` | Bayesian methodology |
| `references/scorecard-rubric.md` | Detailed scoring criteria |
| `references/randomized-withdrawal-design.md` | Enrichment designs, Period 1/2 power analysis |
| `references/novel-target-safety.md` | Novel target safety assessment |
| `references/immuno-inflammation.md` | I&I indications |
| `references/cv-inflammation.md` | CVOTs |
| `references/pah-pulmonary.md` | PAH/pulmonary indications |
| `references/ta-hematology-mf.md` | Hematology, myelofibrosis |
