# Hidradenitis Suppurativa (HS) Therapeutic Area Reference

Disease-specific guidance for commercial and clinical assessment in HS.

---

## Market Overview

**Addressable Population:**
- US prevalence: ~1-4% of population (wide range due to underdiagnosis)
- Moderate-to-severe: ~30-40% of diagnosed patients
- Treated with biologics: Rapidly expanding, historically underpenetrated

**Key Market Characteristics:**
- Historically undertreated specialty dermatology/rheumatology condition
- High unmet need despite new entrants
- Strong TNF-IR and inadequate responder populations
- Long duration of therapy (chronic, lifelong disease)

---

## Competitive Landscape (as of 2024-2025)

### Approved Therapies

| Drug | Company | MOA | Peak Sales Est. | Dosing | Key Notes |
|------|---------|-----|-----------------|--------|-----------|
| **Humira** (adalimumab) | ABBV | TNF-α | Declining (biosimilar) | Q1W or Q2W | First approved, now biosimilar |
| **Cosentyx** (secukinumab) | NOVN | IL-17A | ~$2.5B (HS portion) | Q4W maintenance | Biosimilar imminent (2025-2026) |
| **Bimzelx** (bimekizumab) | UCB | IL-17A/F | ~$3.0B | Q4W maintenance | BIC efficacy, dual IL-17 |
| **Lutikizumab** | ABBV | IL-1α/β | ~$1.5B (HS) | TBD | FIC IL-1 inhibitor (approved 2024) |
| **Brinsupri** (izokibep) | INSM | IL-17A nanobody | ~$2.1B | Q4W maintenance | Novel format (approved 2024) |

### Pipeline

| Drug | Company | MOA | Stage | Peak Sales Est. | Key Notes |
|------|---------|-----|-------|-----------------|-----------|
| **AVTX-009** | AVTX | IL-1β | Phase 2b | $0.75-1.5B | SIC to Luti, single isoform |

---

## Mechanism-Specific Considerations

### IL-17 Pathway (Bimzelx, Cosentyx, Brinsupri)

**Clinical Benchmarks:**
| Endpoint | Bimzelx | Cosentyx | Brinsupri |
|----------|---------|----------|-----------|
| HiSCR50 Week 16 | ~45-55% | ~40-45% | ~45-50% |
| HiSCR75 Week 16 | ~30-35% | ~25-30% | ~28-32% |
| HiSCR90 Week 16 | ~15-20% | ~12-15% | ~15-18% |

**Key IL-17 Dynamics:**
- Dual IL-17A/F inhibition (Bimzelx) shows numerically better efficacy than IL-17A alone
- Candida risk is class effect (~5-10% oral candidiasis)
- Dosing interval convergence at Q4W maintenance

### IL-1 Pathway (Lutikizumab, AVTX-009)

**Mechanism Rationale:**
- IL-1 is upstream inflammatory driver in HS pathophysiology
- Inflammasome activation → IL-1β release → neutrophil recruitment
- Different mechanism than IL-17 (may work in IL-17 failures)

**IL-1α "Alarmin" Biology:**
IL-1α behaves as an "alarmin" and can be abundant/early in cutaneous inflammation in HS (Cavalli et al). This is an **inflammasome-independent process**, meaning IL-1α contributes materially to HS pathogenesis through a separate pathway from IL-1β.

**Critical Read-Through Data:**
| Drug | Target | HiSCR50 | Placebo | Delta | N | Outcome |
|------|--------|---------|---------|-------|---|---------|
| Bermekimab | IL-1α only | 60% | 10% | **+50%** | 20 | Promising (but small N) |
| Lutikizumab | IL-1α + IL-1β | 59.5% | 35% | ~24.5% | Large | Ph3 advancing |
| MAS825 | IL-1β + IL-18 | ~44% | ~35% | ~9% | — | Underwhelming |
| AVTX-009 | IL-1β only | ? | ? | ? | — | TBD |

**CORRECTION:** Earlier analysis cited bermekimab as failed with 0% delta. Actual data from Tanni et al Ph2 (n=20): HiSCR 60% vs 10% pbo at 12 weeks. The small N creates uncertainty, but the signal was NOT zero.

**Lutikizumab Inverse Dose-Response (Key Uncertainty):**
In Luti's Ph2b, the high dose did WORSE than the middle dose:
| Dose | Regimen | Pbo-adj HiSCR50 | Pbo-adj HiSCR75 |
|------|---------|-----------------|-----------------|
| 300mg | EW (high) | 14% | 21% |
| 300mg | EOW (middle) | 24% | 28% |

This raises questions about whether Luti "left efficacy on the table" - unclear if dose optimization was suboptimal.

**Key IL-1 Debate (Updated):**
Given bermekimab's actual signal (60% vs 10%), the debate shifts:
1. If IL-1α alone shows meaningful efficacy, why would IL-1β alone (AVTX) match dual inhibition?
2. Strong biologic rationale exists for IL-1α contribution (alarmin, inflammasome-independent)
3. AVTX bulls need to argue IL-1β is primary driver despite IL-1α evidence

**Important Finding:** Literature shows BOTH IL-1α AND IL-1β are elevated in HS lesional skin. Claims that "only IL-1β is elevated" are factually incorrect.

### NLRP3/NEK7 Read-Through (BIOA, GLUE)

**If AVTX-009 (IL-1β) works in HS, positive read-through to NLRP3/NEK7 inhibitors:**

IL-1β is directly downstream from NLRP3/NEK7, so AVTX success validates the upstream pathway.

**Evidence for NLRP3 Engagement in HS:**

| Finding | Source | Implication |
|---------|--------|-------------|
| **Activated caspase-1 in HS skin** | Kelly et al | NLRP3 inflammasome is engaged |
| **Enhanced NLRP3 expression** | Kelly et al | Upstream target is active |
| **IL-18 elevation in HS** | Kelly et al | NLRP3 downstream mediator present |
| **GSDMD/GSDME in HS serum/skin** | Tyczyńska et al | Gasdermin-mediated pyroptosis engaged |

**Mechanistic Logic:**
```
NLRP3 inflammasome activation
    ↓
Caspase-1 activation (confirmed in HS)
    ↓
├── IL-1β cleavage/release ← AVTX-009 target
├── IL-18 cleavage/release ← Also elevated in HS
└── GSDMD cleavage → Pyroptosis ← Confirmed in HS
```

**Investment Implication:**
- If AVTX shows IL-1β inhibition works in HS, it validates inflammasome engagement
- NLRP3 inhibitors (BIOA, GLUE) would benefit from HS indication expansion
- NLRP3/NEK7 inhibition would hit IL-1β AND IL-18 AND pyroptosis simultaneously

**Companies to Watch:**
| Company | Target | Relevance |
|---------|--------|-----------|
| BIOA | NLRP3 | Direct upstream of IL-1β |
| GLUE | NEK7 (NLRP3 co-activator) | Same pathway, different node |

### TNF Pathway (Humira)

**Status:** Legacy therapy, biosimilar erosion
- Humira was first-approved biologic for HS
- Now biosimilar but NOT focal point for prescribers
- May serve as "step" before IL-17 or IL-1 in some payer pathways

---

## Clinical Endpoints

### HiSCR (Hidradenitis Suppurativa Clinical Response)

| Endpoint | Definition | Use |
|----------|------------|-----|
| HiSCR50 | ≥50% reduction in abscess + nodule count, no new abscesses/draining fistulas | Standard approval threshold |
| HiSCR75 | ≥75% reduction | Higher bar, differentiation threshold |
| HiSCR90 | ≥90% reduction | Stretch goal, BIC territory |

**Placebo Response Benchmarks:**
| Population | HiSCR50 Placebo | Notes |
|------------|-----------------|-------|
| Biologic-naive | ~35-40% | Higher placebo |
| Anti-TNF failures | ~25-35% | Lower placebo, harder population |
| All-comers (mod-severe) | ~30-35% | Mixed |

### Draining Tunnel Count

Secondary endpoint tracking fistula/tunnel progression. Important for severe HS.

---

## Commercial Dynamics

### FIC vs. SIC Dynamics (IL-1 Space)

**Cosentyx → Bimzelx Analog:**
Despite Cosentyx being first IL-17 approved, Bimzelx has performed well because:
1. Superior efficacy with parity dosing convenience
2. Dual IL-17A/F mechanism (clear differentiation)
3. Strong clinical data presentation

**Application to Luti → AVTX-009:**
- AVTX-009 will be SIC but not significantly behind Luti
- Differentiation required on at least one dimension:
  - Better efficacy (unlikely if single isoform)
  - Better safety (ADA profile)
  - Better dosing convenience
  - Better pricing/access

### Market Share Heuristics

| Positioning | Expected Share | Rationale |
|-------------|----------------|-----------|
| BIC IL-1 (clear superiority) | $1.5B | Captures majority of IL-17 inadequate responders |
| Me-too IL-1 (parity to Luti) | $0.75B | Splits market with Luti, limited differentiation |
| Worse than Luti | $0.3-0.5B | Niche use only if significant price advantage |

### Biosimilar Overhang Analysis

**Key Finding:**
Biosimilar risk in specialty I&I (particularly HS) is LESS severe than oncology/mass market:
- Humira biosimilar is available and was first HS biologic
- NOT a focal point among prescribers
- Specialty markets favor innovation over cost
- Cosentyx biosimilar (2025-2026) expected to have limited impact

**Implication:** Biosimilar overhang is NOT a killer for new entrants
- May create "SSE" (single-source equivalent) behavior with bHumira/bCosentyx
- Unlikely to create "DSE" (direct switch) pressure given disease severity
- New mechanisms (IL-1) differentiated from biosimilar options anyway

---

## Dosing Interval as Competitive Moat

**Benchmark:** Q4W maintenance is table stakes
- Bimzelx: Q2W loading → Q4W maintenance
- Cosentyx: Q1W loading x5 → Q4W maintenance
- Brinsupri: Q2W loading → Q4W maintenance

**Minimum Threshold:** Must match Q4W to be competitive
**Differentiation Opportunity:** Q8W maintenance would be disruptive (none currently)

---

## Anti-Drug Antibodies (ADAs)

### ADA as Risk Factor for IL-1 Programs

**Historical Benchmark:**
- LY2189102 (IL-1β, T2D): 33% ADA rate (26/79 pts) at 13 weeks
- Anakinra (IL-1Ra): ~50-70% ADA rate
- Canakinumab (IL-1β): ~6% ADA rate

**Key Questions for AVTX-009:**
1. What is immunogenicity risk given molecular format?
2. Does the ADA rate predict neutralizing antibody impact?
3. How does ADA rate compare to Lutikizumab?

---

## Peak Sales Scenarios

### AVTX-009 Scenario Matrix

| Scenario | PoS | Peak Sales | Rationale |
|----------|-----|------------|-----------|
| **BIC Profile** | 10-15% | $2.0-3.0B | Clear superiority to Luti - unlikely given single isoform |
| **Me-too to ABBV** | 35-40% | $0.75-1.0B | Parity profile, split IL-1 market |
| **Fail/Me-worse** | 45-55% | $0 | Bermekimab analog, single isoform insufficient |

### Valuation Adjustment

ZH's original model issues:
| Input | ZH's Assumption | Adjusted View |
|-------|-----------------|---------------|
| PoS for positive data | 75% | 40-55% (IL-1α alarmin rationale not addressed) |
| BIC peak sales | $3B | $2B (dual blocker Luti at $1-2B) |
| Failure floor | $1.76/share | ~$5/share (cash floor) |

---

## Case Study: AVTX-009/HS Analysis

### Thesis Classification

**ZH's Claimed Thesis Type:** Clinical Edge (reverend-bayes)
**Actual Thesis Type:** Valuation thesis (gap between assumed PoS and reality)

### Key Analytical Gaps (Updated)

1. **Bermekimab SIGNAL not addressed** - IL-1α alone showed 60% vs 10% pbo (Tanni et al, n=20). Small N but NOT zero delta.
2. **IL-1α alarmin rationale** - Strong biologic evidence IL-1α contributes via inflammasome-independent pathway (Cavalli et al)
3. **Luti inverse dose-response unexplained** - 300mg EW did worse than 300mg EOW. Did Luti leave efficacy on table?
4. **Population mismatch** - Lutikizumab in biologic-failures, LOTUS broader
5. **Endpoint mismatch** - Lutikizumab HiSCR50, AVTX-009 HiSCR75

### Key Debate (Refined)

**Bull Case for AVTX-009:**
- IL-1β is the primary driver, IL-1α contribution is marginal
- Bermekimab was small (n=20) and underpowered
- Single-isoform is sufficient

**Bear Case for AVTX-009:**
- Bermekimab actually showed 50% delta (60% vs 10%)
- Strong biologic rationale for IL-1α as "alarmin" (inflammasome-independent)
- Luti's dual blockade captures both pathways
- Why would IL-1β alone match dual inhibition?

### Recommended Work Before Sizing

1. Clarify LOTUS population - what % biologic-naive vs treated?
2. Reconcile bermekimab signal (60% HiSCR in n=20) with bull thesis
3. Find E-R data for IL-1 pathway in HS
4. Understand Luti dose-response inversion
5. Check AVTX-009 binding affinity vs Lutikizumab

### NLRP3/NEK7 Read-Through

If AVTX-009 works:
- Validates inflammasome → IL-1β pathway in HS
- Positive read-through to BIOA (NLRP3) and GLUE (NEK7)
- These upstream inhibitors would also block IL-18 and pyroptosis

---

## Key Principles for HS Programs

1. **Dual blockers have clearer path than single-isoform** - Bimzelx > Cosentyx (IL-17), Lutikizumab has dual coverage. BUT bermekimab showed signal (60% vs 10%, n=20) - single-isoform NOT definitively ruled out.
2. **Q4W is table stakes** - Match or beat incumbent convenience
3. **Biosimilar overhang limited** - Specialty I&I different from mass market
4. **Population matching critical** - Biologic-naive vs failures are different trials
5. **HiSCR hierarchy** - HiSCR50 (approval), HiSCR75 (differentiation), HiSCR90 (BIC)
6. **ADA monitoring** - IL-1 pathway has immunogenicity concerns
7. **NLRP3/NEK7 read-through** - IL-1β success validates inflammasome pathway for upstream inhibitors
