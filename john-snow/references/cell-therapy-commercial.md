# CAR-T / Cell Therapy Commercial Framework

Framework for analyzing commercial dynamics of cell therapies including CAR-T, site-of-care considerations, supply constraints, and competitive positioning.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Analyzing CAR-T commercial trajectory | Yes |
| Site-of-care analysis (community vs tertiary) | Yes |
| Supply-constrained product modeling | Yes |
| Competitor sequencing effects | Yes |
| Partner portfolio dynamics | Yes |

---

## Framework 1: Site-of-Care Dynamics

### The Core Tension

| Setting | % of Patients | CAR-T Capable | Bispecific Capable | Referral Willing |
|---------|---------------|---------------|-------------------|------------------|
| **Tertiary/Academic** | 20-30% | Yes | Yes | N/A (destination) |
| **Community** | 70-80% | Rarely | Yes | Reluctant |

**Key Insight:**
> "70-80% of MM patients are treated in the community setting. As the community setting will likely possess the infrastructure necessary to administer bispecifics, but not the infrastructure necessary to administer CAR-T, community doctors will choose to treat their patients with T+D rather than risk losing their patients to the academic setting."

### Infrastructure Requirements

| Therapy Type | Requirements | Community Feasible |
|--------------|--------------|-------------------|
| **Bispecifics** | Step-up dosing, CRS monitoring, outpatient infusion | Yes |
| **CAR-T** | Apheresis, REMS, ICU access, specialized monitoring | Rarely |
| **Transplant** | Full transplant center certification | No |

### "Patient Loss" Psychology

Community docs fear:
1. Referring patient to tertiary center
2. Tertiary center "keeping" the patient
3. Lost revenue from ongoing management

**Reality (per LEGN management):**
> "HCPs don't 'lose' the pts forever. Pts will require extensive monitoring at regular intervals. Tertiary centers have no incentive to keep pts. Tertiary centers don't have the bandwidth to keep these pts."

### Transplant Analogy

LEGN uses transplant as precedent:
- Transplant has been MM SoC for decades
- Community docs refer to transplant centers
- Community docs don't get paid for referral
- BUT community docs get paid for ALL follow-up care
- Patient returns to community for monitoring

**Commercial Message:**
> "Like transplant, referring a pt out of the community doesn't mean losing that pt forever."

---

## Framework 2: Hub-and-Spoke Model

### Structure

```
TERTIARY CENTERS (existing)
    ↓
COMMUNITY HUBS (new)
- Multi-site practices (Florida Cancer Specialists, Texas Oncology)
- Infusion beds
- Trained nurses
- Monitoring capabilities
    ↓
COMMUNITY SPOKES (majority)
- Refer patients to hubs
- Maintain relationship for follow-up
- Get paid for monitoring
```

### LEGN Implementation

| Metric | Value |
|--------|-------|
| Total infusion sites | 141 |
| Community sites | 40-45 (28-32%) |
| Target | Increase community % |
| Hub partners | Florida Cancer, Texas Oncology, etc. |

### GPO Engagement

- JNJ engaging with GPOs (undisclosed which ones)
- Large community networks (Florida Cancer, Texas Oncology) are "very important"
- Many smaller practices affiliated with these networks

---

## Framework 3: Supply Utilization Revenue Model

### The Formula

```
Revenue = Manufacturing Slots × (1 - OOS Rate) × Utilization Rate × Price
```

### Component Definitions

| Component | Definition | LEGN Example |
|-----------|------------|--------------|
| **Manufacturing Slots** | Capacity to manufacture product | 12,500 (FY26) |
| **OOS Rate** | Out-of-specification (failed manufacturing) | 9% (CI: 7.8-9.8%) |
| **Utilization Rate** | % of good slots actually used | ~90% |
| **Price** | Net price per treatment | US: ~$465K, ex-US: ~$300K |

### OOS Rate Nuance

| Patient Population | OOS Rate |
|--------------------|----------|
| 1 prior line of therapy | 7.8% |
| >4 prior lines of therapy | 10.8% |
| Blended | ~9% |

**Implication:** Earlier-line patients have better manufacturing success.

### LEGN FY26 SWAG

```
Assumptions:
- 12,500 manufacturing slots
- 91% OOS-adjusted (1 - 9%)
- 90% utilization
- US: 60% × $465K, ex-US: 40% × $300K

Calculation:
- Effective slots: 12,500 × 91% × 90% = 10,238 treatments
- US treatments: 6,143 × $465K = $2.86B
- Ex-US treatments: 4,095 × $300K = $1.23B
- Total: ~$4.1B (vs consensus $3.0B)
```

**Caveat:** This back-solve implies significant beat vs. consensus. Management commentary should be triangulated with WSP script data.

### Supply Status Signaling

| Management Commentary | Interpretation |
|----------------------|----------------|
| "Supply constrained" | Demand > capacity, can't serve all patients |
| "No longer supply constrained" | Capacity ≥ demand |
| "~90% utilization" | Near capacity, little wiggle room |
| "Plenty of wiggle room" | Below capacity, demand softening? |

**LEGN Status (Jan 2026):**
> "Not supply constrained anymore. No need to worry about being in queue or waiting list. But utilization of supply will be in high 90%s this yr. We don't have a lot of wiggle room here."

---

## Framework 4: Competitor Sequencing Effects

### BCMA Targeting Order Matters

| Sequence | Efficacy Impact | Clinical Rationale |
|----------|-----------------|-------------------|
| **CAR-T → Bispecific** | Bispecific efficacy preserved | CAR-T targets same antigen but different mechanism |
| **Bispecific → CAR-T** | CAR-T efficacy BLUNTED | T-cell exhaustion, antigen modulation |

**KOL Quotes:**
> "Bispecifics blunt the efficacy of CAR-T" (Dr. Carney)
> "Activity of bispecifics after CAR-T is high. But the reverse is not true." (Dr. Chakraborty)
> "Give most efficacious regimen ASAP" (Dr. Chakraborty)

### Sequencing Implication for Commercial

If optimal sequence is CAR-T first:
- Arguments for early-line CAR-T strengthen
- Bispecific 2L approval may not capture expected share
- "Most patients will get both CAR-T and bispecific" (multiple KOLs)

### T+D (Tecvayli + Darzalex) Specific Issues

| Issue | Details |
|-------|---------|
| **Dara-refractory excluded** | MAJESTEC-3 excluded Dara-refractory, but 1L is now DRd/DVRd |
| **Real-world translation** | "Maybe means real world is 10-20% worse than clinical trial" |
| **Continuous therapy** | Quality of life negative vs "1-and-done" CAR-T |

---

## Framework 5: KOL Impact Quantification

### Methodology

Ask KOLs: "How would [competitive event] change your use of [drug]?"

Quantify as:
- % change in 2L Carvykti use
- Before/after estimates
- Capture uncertainty range

### LEGN KOL Summary (n=9)

| Event | Avg Impact on Carvykti 2L | Range |
|-------|---------------------------|-------|
| **T+D approval in 2L** | -17% | Modest |
| **Anito-cel approval in 4L** | -24% | Modest (most still use Carvykti 2L) |
| **Anito-cel approval in 2L** | -89% | Severe (safety advantage) |

### Anito-cel Specific Dynamics

| Factor | Anito-cel vs Carvykti |
|--------|----------------------|
| **Efficacy** | Perceived as equivalent |
| **Safety** | Anito-cel advantage (lower ICANS, delayed neurotox) |
| **Parkinsonism** | Key differentiator - Carvykti has signal, anito-cel TBD |

**Parkinsonism Thresholds:**
> "0 cases = definitively not a class effect, 90% anito-cel" (Dr. Carney)
> "1-2 cases = anito-cel better than Carvykti" (Dr. Chakraborty)
> "Few cases = 75-80% anito-cel" (Dr. Carney)

### Community Cuts Both Ways

| Pro-Carvykti | Pro-Competitor |
|--------------|----------------|
| Established relationships | Bispecifics easier in community |
| Onboarding new CAR-T challenging | Lower ICANS may expand community |
| Referral patterns exist | Avoid referral entirely |

---

## Framework 6: Partner Portfolio Dynamics

### The Tension

When partner has both CAR-T and bispecific:
- Internal positioning debates
- Potential for cannibalization
- Commercial team incentives

### JNJ Portfolio (LEGN Partner)

| Product | Class | Line | Positioning |
|---------|-------|------|-------------|
| Carvykti | CAR-T | 2L+ | "Preferred 2L therapy" |
| Tecvayli | Bispecific | 2L+ | Continuous therapy |
| T+D (combo) | Bispecific | 2L+ | MAJESTEC-3 data |
| Darzalex | mAb | 1L | Standard of care |

**LEGN's View:**
> "Discussions with JNJ have reinforced JNJ's intentions to position Carvykti as the preferred 2L therapy."

### Monitoring Partner Commitment

| Signal | Bullish for CAR-T | Bearish for CAR-T |
|--------|-------------------|-------------------|
| Commercial messaging | "CAR-T before bispecific" | "Options in 2L" |
| Sales force allocation | CAR-T specialists | Generalist coverage |
| Pricing | Premium maintained | Discounting |
| Supply investment | Capacity expansion | Flat |

---

## Framework 7: Ex-US Growth Modeling

### Geography-Specific Pricing

| Market | Net Price | Notes |
|--------|-----------|-------|
| **US** | ~$465K | Reference price |
| **Germany** | ~$328K | Only BCMA CAR-T available |
| **Spain** | ~$308K | Pent-up demand |
| **France** | ~$270K | Later markets lower |
| **Later markets** | <$270K | Price pressure |

### US/Ex-US Split Trajectory

| Product | Mature US/Ex-US Split |
|---------|----------------------|
| Yescarta (CAR-T comp) | 60% US / 40% ex-US |
| Carvykti target | Similar to Yescarta |

**LEGN FY26 Guidance:**
- 30% ex-US growth expected
- 10 new markets coming online (Italy, France, UK public, etc.)
- Eventually stabilize to Yescarta-like split

### Ex-US Considerations

| Factor | Impact |
|--------|--------|
| Reimbursement timing | Country-by-country, can take years |
| Manufacturing capacity | Must allocate between US and ex-US |
| Supply logistics | Vein-to-vein time constraints |
| Currency | Translation risk |

---

## Framework 8: DTC and Commercial Investment

### DTC Campaign Elements

| Channel | LEGN Example |
|---------|--------------|
| Digital | Roku, Golf Channel, YouTube |
| Spend | "Double-digit millions" |
| Target | Patients + caregivers |

### Commercial Targeting

| Metric | LEGN Data |
|--------|-----------|
| Target hematologists | 6-8K |
| Offices | 5K |
| Profile | High-volume prescribers |
| Geographic targeting | "Know the zip codes of pts" |

### Community-Specific Messaging

| Audience | Message |
|----------|---------|
| **Tertiary** | Already familiar with CAR-T |
| **Community** | 50% not aware of CAR-T; emphasize survival, no patient loss |

---

## Integrated Checklist: CAR-T Commercial Assessment

```
CAR-T COMMERCIAL ASSESSMENT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SITE-OF-CARE DYNAMICS:
□ Total infusion sites: _____
□ Community sites: _____ (____%)
□ Hub-and-spoke model in place? [ ] Yes [ ] No
□ Key GPO/network partnerships: _____

SUPPLY ANALYSIS:
□ Manufacturing slots (annual): _____
□ OOS rate: _____%
□ Utilization rate: _____%
□ Supply constrained? [ ] Yes [ ] No

REVENUE BACK-SOLVE:
□ Effective treatments: _____ (slots × (1-OOS) × utilization)
□ US price: $_____
□ Ex-US price: $_____
□ US/Ex-US split: ____/____
□ Implied revenue: $_____
□ vs. Consensus: _____% (beat/miss)

COMPETITIVE POSITIONING:
□ Sequencing optimal? (CAR-T before bispecific) [ ] Yes [ ] No
□ KOL impact quantified? [ ] Yes [ ] No
□ Safety differentiation: _____
□ Partner portfolio tension? [ ] Yes [ ] No

EX-US GROWTH:
□ Markets currently live: _____
□ Markets launching this year: _____
□ Target US/Ex-US split: ____/____
□ Ex-US growth rate: _____%

COMMERCIAL INVESTMENT:
□ DTC spend: $_____M
□ Target physicians: _____
□ Community awareness: _____%
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Case Study: LEGN Carvykti (January 2026)

### Background

- **Drug:** Carvykti (ciltacabtagene autoleucel) - BCMA CAR-T
- **Partner:** JNJ (commercial)
- **Indication:** Multiple myeloma 2L+
- **Status:** No longer supply constrained, ~90% utilization expected

### Site-of-Care Strategy

| Element | Status |
|---------|--------|
| Total sites | 141 |
| Community sites | 40-45 (28-32%) |
| Hub partners | Florida Cancer, Texas Oncology |
| Messaging | "Like transplant - don't lose patient" |

### Supply Math

| Input | Value |
|-------|-------|
| FY26 slots | 12,500 |
| OOS rate | 9% |
| Utilization | ~90% |
| Effective treatments | ~10,238 |

### Competitive Dynamics

| Competitor | Impact on Carvykti |
|------------|-------------------|
| T+D (2L approval) | -17% |
| Anito-cel (4L) | -24% |
| Anito-cel (2L) | -89% |

### Key Risk: Anito-cel 2L

If anito-cel achieves 2L approval with:
- Similar efficacy
- Better safety (no parkinsonism signal)

→ Carvykti loses 2L positioning almost entirely

**KOL Quote:**
> "Would be no reason not to use anito-cel if approved in 2L with no parkinsonism" (Dr. Rubinstein)

### Financial Guidance (FY26)

| Line Item | Guidance |
|-----------|----------|
| COGS | "Slightly improve" |
| Gross margin | "Increase in 2027" (economies of scale) |
| R&D | "Increase modestly" (in-vivo CAR-T shift) |
| SG&A | "Increase" (DTC campaign) |
| SG&A % revenue | "Down a few points" |

### Ex-US Growth

| Metric | Value |
|--------|-------|
| FY26 growth | 30% |
| New markets | 10 (Italy, France, UK public) |
| Target split | 60/40 US/ex-US (Yescarta-like) |

---

## Key Principles for CAR-T Commercial

1. **Site-of-care is the battleground** - 70-80% of patients in community, community can't do CAR-T
2. **"Patient loss" is a perception problem** - use transplant analogy, emphasize follow-up revenue
3. **Hub-and-spoke expands reach** - large community networks become hubs for CAR-T
4. **Supply utilization = revenue signal** - back-solve revenue from capacity × utilization × price
5. **Sequencing matters for BCMA** - bispecific before CAR-T blunts CAR-T efficacy
6. **KOL impact can be quantified** - ask "how would X change your use of Y?"
7. **Safety can trump efficacy** - anito-cel 2L would devastate Carvykti despite similar efficacy
8. **Partner portfolio creates tension** - monitor positioning when partner has both CAR-T and bispecific
9. **Ex-US follows established patterns** - Yescarta 60/40 split is benchmark
10. **OOS rate varies by line** - earlier-line patients have better manufacturing success
