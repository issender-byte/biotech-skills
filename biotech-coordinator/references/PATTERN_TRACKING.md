# Biotech Analysis Skills - Pattern Tracking

Meta-document tracking analytical patterns extracted from institutional debates, mapped to skills, with implementation status.

**Current file count: 47** (Update this number when adding files)

---

## ⚠️ NEW CONVERSATION START HERE

**If you're starting a new conversation in this project, follow this workflow:**

### Step 1: Verify System Integrity
```bash
find /mnt/skills/user -name "*.md" ! -path "*/autonomous-integration/*" | wc -l
```
Compare result to "Current file count" at top of this file. If mismatch, check PERSISTENCE.md for recovery protocol.

### Step 2: For Investment Case Analysis
When user provides a new investment case/thesis/DD:
1. Read biotech-coordinator/SKILL.md for routing
2. Route to appropriate skills (reverend-bayes → john-snow → graham → keynes → simons)
3. Use 5PTer template for output format

### Step 2b: For Team Work Evaluation
When user provides analyst work for review (emails, pitches, memos):
1. Read skill-iteration-guide.md **Work Evaluation Protocol** section
2. Complete BOTH parts:
   - **Part 1: Coaching identification** - What did they do well? Where did they fall short?
   - **Part 2: Pattern extraction** - What new patterns? What existing patterns applied/missed?
3. Update team-roster.md with Progress Tracking entry
4. Update this file if new patterns identified
5. Produce summary table (Stated view, Provenance, Role execution, Contrary evidence, New patterns)

### Step 3: For Pattern Extraction
When user provides raw materials (emails, DD notes, management calls):
1. Read skill-iteration-guide.md for extraction methodology
2. Identify analytical moves (not just facts)
3. Abstract to ticker-agnostic rules
4. Locate where pattern belongs (see workflow below)
5. Update this file after adding

---

## Source Conversation Index

| Conversation | Date | Ticker(s) | Patterns Extracted |
|--------------|------|-----------|-------------------|
| Clinical Trial Success Probability | Jan 2026 | APGE, framework | Core skill architecture, 5-skill system |
| CRVS/CGON/ALMS Email Analysis | Prior | CRVS, CGON, ALMS | Placebo benchmarks, single-arm comps, read-through, short thesis validation |
| ZEUS/CANTOS Read-Through | Prior | ZEUS, GLUE | Biomarker threshold read-through, competitor dismissal, cv-inflammation module |
| Fintepla E-R Analysis | Prior | Fintepla | Exposure-response mapping, dose cap analysis, concomitant med effects |
| Verdad Biotech Paper Analysis | Jan 2026 | — | Specialist funds, short interest, momentum, EV/R&D |
| RVMD Biotech Skills Test | Jan 2026 | RVMD | Full workflow test, M&A framework trigger |
| RVMD M&A Update | Jan 2026 | RVMD | M&A playbook, deal spread mechanics |
| RVMD Short Cover | Jan 2026 | RVMD | M&A short cover rule, thesis invalidation |
| TERN Email Thread | Jan 2026 | TERN, ELVN | Endpoint manipulation, E-R mapping, chronic therapy economics, KOL integration |
| OCUL SOL-1 Street Expects | Dec 2025 | OCUL | Street expects integration, cross-trial baseline mapping |
| NUVB Short Thesis | Jan 2026 | NUVB, NUVL | Competitor-contingent shorts, bolus→incident dynamics, thesis creep |
| IRON AA Pathway | Jan 2026 | IRON | Biomarker-clinical disconnect, accelerated approval premium, weighted EV for shorts |
| IMVT FcRn Analysis | Jan 2026 | IMVT | Randomized withdrawal power, ACPA+ enrichment, buyside expect check |
| GKOS Product Transition | Jan 2026 | GKOS | Product transition pricing, forced adoption |
| GOSS PAH Analysis | Jan 2026 | GOSS | Subgroup skepticism, OLE reality check, PVR-6MWD regression |
| SLNO Commercial | Jan 2026 | SLNO | Intraquarter tracking, capture rate, persistence curves |
| PGEN Gene Therapy | Jan 2026 | PGEN | Bolus product commercial, PSF tracking, KOL dosing |
| MF DD Session | Jan 2026 | KPTI, CNST | 39 analytical rules, management DD checklist |
| AVTX HS Analysis | Jan 2026 | AVTX | HS competitive landscape, IL-1β framework, **MEDI8968 read-through, time-course analysis (RP)** |
| LEGN CAR-T | Jan 2026 | LEGN | Site-of-care dynamics, partner portfolio, supply utilization |
| **ACAD ADP Analysis (WS)** | Jan 2026 | ACAD | RW vs parallel delta compression, SD by design phase, E-R plateau skepticism, 2nd gen comparison framework, power table construction |
| **APGE E-R Analysis (RP)** | Jan 2026 | APGE | Withdrawal floor, biomarker→MEC mapping, AE dose-response direction, placebo inflation risk, Ctrough ratio cross-molecule |
| **CGON PIVOT-006 (LA)** | Jan 2026 | CGON | US periop chemo adoption reality, trial design signals, management Q&A gap-filling, FDA control precedent, cross-trial efficacy hierarchy |

---

## Complete Case Study Index

| # | Ticker | Primary Skill | Key Patterns | Reference File |
|---|--------|---------------|--------------|----------------|
| 1 | CRVS | reverend-bayes | Placebo benchmarks I&I | immuno-inflammation.md |
| 2 | CGON | reverend-bayes | Cross-trial benchmarking, **US periop chemo reality (10-15%)**, **trial design signals**, **management Q&A gap-filling**, **FDA control precedent**, **efficacy hierarchy** | cross-trial-comparison.md, ta-bladder-cancer.md |
| 3 | ALMS | graham | Price/volume decomposition, short thesis | short-thesis-validation.md |
| 4 | TERN/ELVN | reverend-bayes | Endpoint manipulation, E-R | analytical-rules.md (Rules 5-8) |
| 5 | APGE | reverend-bayes | Withdrawal durability floor, biomarker→MEC threshold, AE dose-response direction, placebo inflation risk, Ctrough ratio cross-molecule | pk-pd-exposure-response.md, cross-trial-comparison.md |
| 6 | RVMD | keynes | M&A playbook, short cover | m-and-a-playbook.md |
| 7 | OCUL | biotech-coord | Street expects, baseline mapping | street-expects-integration.md |
| 8 | GLUE | reverend-bayes | Novel target safety | novel-target-safety.md |
| 9 | GKOS | john-snow | Product transition pricing, forced adoption, tiered launch | product-transition-commercial.md |
| 10 | IRON | graham | AA pathway, biomarker coherence | short-thesis-validation.md |
| 11 | IMVT | reverend-bayes | Randomized withdrawal power, single-arm data limitations | randomized-withdrawal-design.md |
| 12 | SLNO | john-snow | Intraquarter tracking | intraquarter-commercial-tracking.md |
| 13 | GOSS | reverend-bayes | Subgroup skepticism, PVR regression | pah-pulmonary.md |
| 14 | NUVB | graham | Competitor-contingent shorts | short-thesis-validation.md |
| 15 | PGEN | john-snow | Bolus product commercial | bolus-product-commercial.md |
| 16 | ZEUS | reverend-bayes | CV inflammation read-through | cv-inflammation.md |
| 17 | Fintepla | reverend-bayes | E-R mapping | pk-pd-exposure-response.md |
| 18 | KPTI | reverend-bayes | MF benchmarks, DD framework | ta-hematology-mf.md |
| 19 | CNST | reverend-bayes | MF benchmarks | ta-hematology-mf.md |
| 20 | AVTX | john-snow | HS market dynamics, IL-1 pathway, NLRP3 read-through, bermekimab correction, **MEDI8968 failure read-through**, **biomarker validates dosing**, **time-course kinetics**, **error bar discipline** | ta-hidradenitis-suppurativa.md |
| 21 | LEGN | john-snow | CAR-T commercial, site-of-care, supply utilization | cell-therapy-commercial.md |
| 22 | ACAD | reverend-bayes | RW vs parallel delta compression, SD by design phase, E-R plateau skepticism, power tables, "juice left to squeeze", cross-indication validation, NPIC non-linearity, QTc dose headroom | randomized-withdrawal-design.md, pk-pd-exposure-response.md, scale-properties.md |

---

## Pattern Catalog by Skill

### reverend-bayes Patterns (Clinical PoS)

| Pattern | Description | Source | File | Status |
|---------|-------------|--------|------|--------|
| Placebo benchmarking | Always check historical placebo rates | CRVS | immuno-inflammation.md | ✅ |
| Cross-trial comparison | Map baseline characteristics first | CGON, OCUL | cross-trial-comparison.md | ✅ |
| E-R quartile analysis | Check dose selection basis | TERN, Fintepla | pk-pd-exposure-response.md | ✅ |
| Biomarker-clinical disconnect | Red flag if biomarker ≠ clinical | IRON | SKILL.md | ✅ |
| Endpoint manipulation | "At vs by" timing tricks | TERN | analytical-rules.md (5-8) | ✅ |
| Novel target safety | DepMap, homolog, selectivity | GLUE | novel-target-safety.md | ✅ |
| Subgroup skepticism | Post-hoc from failed Ph2 | GOSS | pah-pulmonary.md | ✅ |
| % CFB normalization | Adjust for baseline severity | KPTI | ta-hematology-mf.md | ✅ |
| RW vs parallel delta compression | Parallel designs show smaller deltas than RW | ACAD, SLNO | randomized-withdrawal-design.md | ✅ |
| SD by design phase | OL has higher SD than DB (responder selection) | ACAD | randomized-withdrawal-design.md | ✅ |
| E-R plateau skepticism | If curve flattens at high conc, "dose higher" thesis is suspect | ACAD | pk-pd-exposure-response.md | ✅ |
| Power table construction | Explicit assumptions: n, SD, effect size, stats bar | ACAD | statistical-framework.md | ✅ |
| FDA rejection despite stats | Hitting stats ≠ approval; weak efficacy can still fail | ACAD | randomized-withdrawal-design.md | ✅ |
| 2nd gen molecule comparison | Evaluate PK/potency/safety enabling; improvement must matter for E-R | ACAD | pk-pd-exposure-response.md | ✅ |
| "Juice left to squeeze" | DB delta is marginal after OL ceiling; total effect = OL + DB | ACAD (MM) | randomized-withdrawal-design.md | ✅ |
| Cross-indication validation | Test methodology on population with ground truth | ACAD (MM) | randomized-withdrawal-design.md | ✅ |
| Non-linear scale caution | NPIC, PANSS — point changes ≠ uniform across severity | ACAD (AG) | scale-properties.md | ✅ |
| QTc dose ceiling | No QTc = higher dose potential = E-R exploration possible | ACAD (AG) | pk-pd-exposure-response.md | ✅ |
| Subpopulation power | RW in DRP not powered for ADP subgroup — underpowered post-hoc | ACAD (AG) | randomized-withdrawal-design.md | ✅ |
| Same-receptor failure read-through | If blocking receptor (all ligand signaling) failed, why would partial block work? | AVTX (RP) | ta-hidradenitis-suppurativa.md | ✅ |
| Biomarker validates dosing | If biomarker moves as expected, can't claim underdosed; defeats that thesis | AVTX (RP) | ta-hidradenitis-suppurativa.md, analytical-rules.md | ✅ |
| Target engagement ≠ clinical efficacy | CRP/fibrinogen down but trial failed → mechanism doesn't translate | AVTX (RP) | ta-hidradenitis-suppurativa.md | ✅ |
| Consistent separation > end-of-study | Drug should separate early and maintain; end-only separation = red flag | AVTX (RP) | analytical-rules.md (38-42) | ✅ |
| Error bar discipline | Wide CIs = high variability, low confidence; overlapping CIs = noise | AVTX (RP) | analytical-rules.md (41) | ✅ |
| Positive control benchmarking | Compare kinetics to known winner in same indication (e.g., Bimzelx) | AVTX (RP) | analytical-rules.md (40) | ✅ |
| Withdrawal durability floor | Mine competitor withdrawal studies; efficacy loss at zero exposure = floor | APGE (RP) | pk-pd-exposure-response.md | ✅ |
| Biomarker rebound → MEC | Map biomarker rebound timing to concentration; establishes minimum effective conc | APGE (RP) | pk-pd-exposure-response.md | ✅ |
| AE dose-response direction | Inverted dose-response = AE not exposure-driven; monotonic = exposure-driven | APGE (RP) | pk-pd-exposure-response.md | ✅ |
| Placebo inflation risk | If placebo >50% higher than historical, use delta as primary metric | APGE (RP) | cross-trial-comparison.md | ✅ |
| Ctrough ratio cross-molecule | If your Ctrough > competitor's at known efficacy interval, that's your floor | APGE (RP) | cross-trial-comparison.md | ✅ |
| Exposure/IC50 ratio comparison | Normalize cross-molecule comparisons to Ctrough/IC50; receptor blockers vs ligand neutralizers need different calculations | AVTX (ZH) | pk-pd-exposure-response.md | ✅ |
| US periop chemo adoption reality | Database studies (Lee 2022, Lewicki 2022) show 10-15% US adoption, not majority; ex-US studies overstate | CGON (LA) | ta-bladder-cancer.md | ✅ |
| Trial design signals | Sample size reduction post-initiation signals faster enrollment and/or events; interrogate management | CGON (LA) | analytical-rules.md | ✅ |
| Management Q&A gap-filling | Direct management engagement fills specific analytical gaps (enrollment composition, stratification) | CGON (LA) | analytical-rules.md | ✅ |
| FDA control precedent | FDA acceptance of simpler control (e.g., TURBT+observation) in similar trials = acceptable for your trial | CGON (LA) | cross-trial-comparison.md | ✅ |
| Cross-trial efficacy hierarchy | Build efficacy ladder across trials (active vs observation) to establish where new drug fits | CGON (LA) | cross-trial-comparison.md | ✅ |

### john-snow Patterns (Commercial)

| Pattern | Description | Source | File | Status |
|---------|-------------|--------|------|--------|
| Launch curve analogs | Use similar launches as guide | Core | launch-analogs.md | ✅ |
| Net price vs list | Always model net | ALMS | pricing-access.md | ✅ |
| Late-to-market BIC discount | 25-50% of incumbent peak | TERN | SKILL.md | ✅ |
| Site-of-care dynamics | Community vs tertiary split, hub-and-spoke | LEGN | cell-therapy-commercial.md | ✅ |
| Intraquarter tracking | Script → revenue calibration | SLNO | intraquarter-commercial-tracking.md | ✅ |
| Bolus product commercial | PSF tracking, TAM depletion | PGEN | bolus-product-commercial.md | ✅ |
| Molecule ownership history | Multiple ownership changes = prior owners saw limited value | AVTX | (to add) | ⏳ |
| SSE vs DSE biosimilar dynamics | Switching vs de novo erosion; DSE unlikely in severe disease | AVTX | (to add) | ⏳ |
| Clinical bar definition | Commercial must define efficacy thresholds for each scenario | AVTX | SKILL.md (handoff section) | ✅ |

### graham Patterns (Valuation)

| Pattern | Description | Source | File | Status |
|---------|-------------|--------|------|--------|
| Implied PoS back-solve | Edge = gap between your PoS and market's | Core | rnpv-methodology.md | ✅ |
| Cash floor | Never short below cash | ALMS | short-thesis-validation.md | ✅ |
| Competitor-contingent shorts | Time to competitor success | NUVB | short-thesis-validation.md | ✅ |
| Weighted EV for shorts | Must be negative | ALMS, IRON | short-thesis-validation.md | ✅ |

### keynes Patterns (Position Management)

| Pattern | Description | Source | File | Status |
|---------|-------------|--------|------|--------|
| M&A short cover rule | Cover on M&A unless differentiated view | RVMD | m-and-a-playbook.md | ✅ |
| Sellside sentiment | Rating distribution, PT clustering | Verdad | sentiment-indicators.md | ✅ |
| Short interest dynamics | >15% = squeeze risk | Verdad | positioning-analysis.md | ✅ |
| Insider activity | Cluster buying = strong signal | APGE | insider-activity.md | ✅ |
| Catalyst positioning | Pre-event run, EV analysis | Core | catalyst-playbook.md | ✅ |
| Technical basics | Support/resistance, volume | Core | technical-basics.md | ✅ |

### simons Patterns (Portfolio/Risk)

| Pattern | Description | Source | File | Status |
|---------|-------------|--------|------|--------|
| TA concentration limits | Max 30% gross in single TA | Core | exposure-limits.md | ✅ |
| Correlation clusters | Same target/TA = high correlation | Core | correlation-clusters.md | ✅ |
| Analysis-constrained sizing | Don't full-size until analyzed | NUVB | position-sizing.md | ✅ |

---

## Pattern Extraction Methodology

When analyzing new email threads or conversations:

1. **Identify the debate** - What's the bull/bear disagreement?
2. **Extract the analytical technique** - How did the analyst resolve it?
3. **Generalize the pattern** - Does this apply beyond this specific stock?
4. **Map to skill** - Which skill should own this pattern?
5. **Document with source** - Include ticker, date, key quotes
6. **Add to this file** - Update Source Conversation Index and Pattern Catalog
7. **Create/update reference file** - Implement in skill

---

## Known Gaps

Files referenced in memory but not yet created:

| File | Skill | Description | Priority |
|------|-------|-------------|----------|
| `economic-share.md` | graham | LOE framework (BPCIA 12yr, NCE 5yr, ODE 7yr) | High |
| `comparable-transactions.md` | graham | M&A comp frameworks | Medium |
| `probability-weighted-scenarios.md` | graham | Scenario math | Medium |
| `pair-trade-construction.md` | simons | Hedging methodology | Medium |
| `ta-oncology-solid.md` | reverend-bayes | Solid tumor endpoints | Medium |

---

## Version History

| Date | Update |
|------|--------|
| 2026-01-25 | Initial creation |
| 2026-01-26 | Added NUVB, GOSS, KPTI patterns |
| 2026-01-27 | Recovered after system loss |
| 2026-01-27 | Full recovery: keynes + simons refs created |
| 2026-01-27 | Added ta-hidradenitis-suppurativa.md (AVTX), product-transition-commercial.md (GKOS), cell-therapy-commercial.md (LEGN), randomized-withdrawal-design.md (IMVT), 43 total files |
| 2026-01-27 | **PROVENANCE INCIDENT:** Added Rules 40-45 (Data Provenance) to analytical-rules.md after bermekimab hallucination. Added provenance protocol to skill-iteration-guide.md. |
| 2026-01-27 | **AUDIT:** Fixed SKILL.md reference listings (reverend-bayes missing 4, graham/simons had non-existent files). Fixed TERN/ELVN mapping. Updated analytical-rules.md header (48 rules). Updated Memory #8 (21 case studies), #15 (economic-share.md PLANNED). |
| 2026-01-27 | **TEAM & PROCESS:** Added team-roster.md (ZH, Ben, LA, AK, BS profiles). Added bidirectional clinical-commercial handoff to john-snow. Added stated view requirement to 5pter-template.md. 44 total files. |
| 2026-01-27 | **REFACTOR:** Deduplicated rNPV content (graham SKILL.md now refs rnpv-methodology.md). Removed duplicate Sources template from biotech-coordinator. Updated skill dependency tree to reflect actual files. All broken refs now in Known Gaps only. |
| 2026-01-27 | **ACAD (WS):** Added Work Evaluation Protocol to skill-iteration-guide.md. Extracted 5 new patterns: RW vs parallel delta compression, SD by design phase, E-R plateau skepticism, 2nd gen comparison framework, FDA rejection despite stats. Updated randomized-withdrawal-design.md and pk-pd-exposure-response.md. Added WS to team-roster.md. 22 case studies. |
| 2026-01-27 | **ACAD (AG/MM feedback):** Added 5 new patterns from senior feedback: "juice left to squeeze", cross-indication validation, non-linear scale caution, QTc dose ceiling, subpopulation power. Created scale-properties.md (NEW). Updated randomized-withdrawal-design.md (Frameworks 5-6), pk-pd-exposure-response.md (QTc section), team-roster.md (WS progress). 45 files. |
| 2026-01-27 | **AVTX (RP feedback):** Added 6 new patterns from RP: MEDI8968 failure read-through, biomarker validates dosing, target engagement ≠ efficacy, time-course consistency, error bar discipline, positive control benchmarking. Updated ta-hidradenitis-suppurativa.md, analytical-rules.md (now 53 rules with new Time-Course section 38-42), team-roster.md (ZH development area #4). Created time-course-kinetics.md (NEW comprehensive reference). 46 files. |
| 2026-01-27 | **APGE E-R Analysis (RP):** Added 5 new patterns from RP's E-R deep dive: withdrawal durability floor, biomarker→MEC threshold mapping, AE dose-response direction, placebo inflation risk, Ctrough ratio cross-molecule inference. Updated pk-pd-exposure-response.md (3 patterns), cross-trial-comparison.md (2 patterns as Part 6-7). 23 case studies. |
| 2026-01-27 | **CGON PIVOT-006 (LA):** Added 5 new patterns from LA's IR NMIBC analysis: US periop chemo adoption reality (10-15%), trial design signals, management Q&A gap-filling, FDA control precedent, cross-trial efficacy hierarchy. Created ta-bladder-cancer.md (NEW). LA showed major development - stated view with numbers (50-65% control, 15-20% delta). 47 files. |
| 2026-01-27 | **AVTX IC50 (ZH):** Added Exposure/IC50 Ratio Comparison pattern to pk-pd-exposure-response.md. Pattern: normalize cross-molecule comparisons to Ctrough/IC50; receptor blockers vs ligand neutralizers require different calculations; Anakinra paradox. Updated team-roster.md with ZH progress.
| 2026-01-28 | **ACAD WS Round 2:** Evaluated WS response to AG/MM. Good engagement - did cross-indication validation (PDP vs ADP), identified placebo rebound anomaly (10-15%), defended view with data. Gaps: no power calc from ES estimate, no implied PoS, deferred dose-response question. Added management call questions to Action Items. Updated team-roster.md. |
| 2026-01-28 | **Effect Size Gap Framework:** Added Framework 3 to statistical-framework.md. Template for: back-solve trial N from powered ES → calculate power at analyst ES → translate to endpoint units → PoS with regulatory haircut → market comparison. ACAD worked example included. Completes reverend-bayes→graham→keynes→simons chain. |

---

## Action Items

### ACAD Dose-Response Management Call Questions (for WS follow-up)

AG raised: "Lack of QTc prolongation enables higher dosing. We don't know what the dose response looks like in ADP."

WS deferred: "Can ask mgmt if they have additional data to support this."

**Specific questions for management:**

1. **Preclinical E-R data:**
   - What does the preclinical model show for dose-response in efficacy?
   - Is there a ceiling effect at higher exposures?
   - At what exposure multiple (vs approved Nuplazid dose) does efficacy plateau?

2. **PDP dose-response:**
   - In the PDP trials, was there a dose-response relationship?
   - What was the magnitude of difference between dose cohorts?
   - Can you share the PK-PD analysis from PDP?

3. **ADP-204 dose selection rationale:**
   - How was the 2x dose selected for ADP-204?
   - Was this based on E-R modeling, or safety margin, or both?
   - What exposure (Ctrough, AUC) are you targeting vs Nuplazid?

4. **Expected effect size:**
   - What effect size is the company powering for?
   - What's the company's base case for SAPS-H+D delta?
   - How does this compare to your internal expectations for Nuplazid if it could be dosed 2x higher?

5. **Competitive context:**
   - Are there any head-to-head comparisons planned?
   - How do you think about differentiation vs other pipeline assets in ADP?

**Why this matters for thesis:**

The bull case rests on "2x dosing enables superior efficacy via E-R." But this thesis requires:
- Evidence that E-R curve isn't plateauing (WS's concern)
- Evidence that higher exposure → better efficacy in relevant population
- Quantification of the expected improvement vs Nuplazid

Without this data, the "better dosing" thesis is unsubstantiated.

---
