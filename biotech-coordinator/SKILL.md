---
name: biotech-coordinator
description: "Orchestrates biotech investment analysis by routing to specialized sub-skills and synthesizing outputs. Use this skill FIRST when asked to analyze a biotech company, evaluate a clinical trial, or assess an investment opportunity. Routes to: reverend-bayes (regulatory PoS), john-snow (commercial peak sales), graham (valuation). Triggers: biotech analysis, investment thesis, company analysis, position recommendation, IC memo."
---

# Biotech Analysis Coordinator

**Purpose:** Orchestrate biotech investment analysis across specialized skills.

**Sub-skills:**
| Skill | Named For | Does |
|-------|-----------|------|
| `reverend-bayes` | Thomas Bayes | Probability of regulatory success |
| `john-snow` | John Snow | Market sizing and peak sales |
| `graham` | Benjamin Graham | Valuation and intrinsic value |
| `keynes` | John Maynard Keynes | Position management, sentiment, timing |
| `simons` | Jim Simons | Portfolio construction, risk management |

## Routing Logic

```
START: What is the analytical question?
│
├─ "What's the PoS for this trial?"
│  └─ Route to: reverend-bayes ONLY
│     Output: PoS estimate with key debates
│
├─ "What are peak sales for this drug?"
│  └─ Route to: john-snow ONLY
│     Input needed: TPP assumptions
│     Output: Peak sales range
│
├─ "What's the stock worth?"
│  └─ Route to: graham
│     Inputs needed: PoS + Peak Sales
│     → May need to run reverend-bayes first
│     → May need to run john-snow first
│
├─ "Should we buy/sell/short this?"
│  └─ FULL ANALYSIS:
│     1. reverend-bayes → PoS
│     2. john-snow → Peak Sales
│     3. graham → Fair Value
│     4. keynes → Timing, standalone size
│     5. simons → Portfolio-adjusted size
│
├─ "What's the market expecting?"
│  └─ Route to: keynes
│     Inputs needed: Fair value (from graham)
│     Output: Sentiment, positioning, timing recommendation
│
├─ "How does this fit in the portfolio?"
│  └─ Route to: simons
│     Inputs needed: Position recommendation (from keynes)
│     Output: Final size, correlation impact, exposure changes
│
├─ "Write an IC memo"
│  └─ FULL ANALYSIS + IC MEMO FORMAT
│
└─ Unclear question
   └─ Ask clarifying questions before routing
```

## Information Gathering

Before routing, gather key context:

### For Reverend Bayes (Clinical PoS)
- [ ] Trial phase and design
- [ ] Primary endpoint
- [ ] Prior data (Phase 1/2 if Phase 3)
- [ ] Competitive context
- [ ] Relevant prior trials in mechanism

### For John Snow (Commercial)
- [ ] Target Product Profile (TPP)
- [ ] Competitive set
- [ ] Market size data
- [ ] Pricing analogs

### For Graham (Valuation)
- [ ] Current stock price and market cap
- [ ] Cash position
- [ ] Pipeline beyond lead asset
- [ ] Catalyst timeline

## Skill Sequencing

### Full Analysis Sequence

```
STEP 1: REVEREND BAYES
├─ Input: Trial data, prior results, competitive context
├─ Output: PoS estimate (XX-YY%) with key debates
└─ Pass forward: PoS range

STEP 2: JOHN SNOW
├─ Input: TPP (often derived from expected trial results)
├─ Input: Competitive set, market size
├─ Output: Peak sales ($X-YB) with assumptions
└─ Pass forward: Peak sales range

STEP 3: GRAHAM
├─ Input: PoS from Step 1
├─ Input: Peak sales from Step 2
├─ Input: Current price, cash, other pipeline
├─ Output: Fair value, implied PoS, recommendation
└─ Final: Investment thesis
```

### Partial Analysis (When Full Not Needed)

| User Question | Skills Needed |
|---------------|---------------|
| "What's the PoS?" | reverend-bayes only |
| "Given 50% PoS, what's fair value?" | john-snow + graham |
| "Is this a good short?" | graham (may need others for inputs) |
| "What's the market opportunity?" | john-snow only |

## Synthesis: IC Memo Format

After running relevant skills, synthesize into IC-ready memo:

```
═══════════════════════════════════════════════════════════════
INVESTMENT COMMITTEE MEMO
Company: [Name] | Ticker: [Symbol]
Analyst: [Name] | Date: [Date]
═══════════════════════════════════════════════════════════════

RECOMMENDATION: [Buy/Hold/Sell/Short] [X bps]
Current Price: $[X] | Target: $[Y] | Downside: $[Z]

THESIS SUMMARY (2-3 sentences):
[Core thesis in plain language]

───────────────────────────────────────────────────────────────
REVEREND BAYES: CLINICAL ASSESSMENT
───────────────────────────────────────────────────────────────

PoS: [XX-YY%] for [specific outcome]

Key Debates:
1. [Debate 1]: [Your position]
2. [Debate 2]: [Your position]
3. [Debate 3]: [Your position]

Key Risks: [What could make you wrong]

───────────────────────────────────────────────────────────────
JOHN SNOW: COMMERCIAL ASSESSMENT
───────────────────────────────────────────────────────────────

Peak Sales: $[X-Y]B (US) / $[A-B]B (WW)
Peak Year: [Year]

Market Positioning: [Best-in-class / Me-too / Niche]
Key Assumption: [Most important driver of peak sales]

───────────────────────────────────────────────────────────────
GRAHAM: VALUATION
───────────────────────────────────────────────────────────────

Fair Value: $[X-Y] per share
Current Implied PoS: [X%] vs. Your PoS: [Y%]
Valuation Floor: $[Z] (cash + other pipeline)

Scenario Analysis:
│ Scenario │ Probability │ Value │ Weighted │
│ Bull │ │ │ │
│ Base │ │ │ │
│ Bear │ │ │ │

───────────────────────────────────────────────────────────────
CATALYSTS
───────────────────────────────────────────────────────────────

│ Date │ Event │ Expected Impact │
│ │ │ │
│ │ │ │

───────────────────────────────────────────────────────────────
POSITION MANAGEMENT
───────────────────────────────────────────────────────────────

Current Position: [X bps]
Recommended Position: [Y bps]
Entry: $[X] | Add: $[Y] | Trim: $[Z] | Exit: $[W]

═══════════════════════════════════════════════════════════════
```

## Handling Incomplete Information

### When Information is Missing

```
If missing trial data:
→ Ask user for specifics
→ Or search ClinicalTrials.gov / company materials
→ Flag assumptions clearly

If missing TPP:
→ Derive from clinical data if available
→ Or use competitor TPP as proxy
→ Flag as assumption

If missing market data:
→ Use published epidemiology
→ Or competitor disclosures as proxy
→ Flag uncertainty in peak sales range
```

### When User Provides Partial Inputs

```
User: "Assume 50% PoS - what's fair value?"
→ Skip reverend-bayes
→ Run john-snow (may need TPP)
→ Run graham with provided PoS

User: "Peak sales should be $2B - is this stock cheap?"
→ Skip john-snow
→ Run graham with provided peak sales
→ May still need PoS → run reverend-bayes if not provided
```

## Quality Checklist

Before finalizing output, verify:

- [ ] **PoS is specific:** "50% PoS for Phase 3 primary endpoint" not "50% it works"
- [ ] **Peak sales have assumptions:** Share %, pricing, market size stated
- [ ] **Valuation shows math:** Not just "stock is cheap" but "implies X% PoS vs. my Y%"
- [ ] **Key debates named:** 3-5 specific uncertainties, not generic risks
- [ ] **Position is actionable:** Entry/exit triggers, not just "buy"
- [ ] **Risks acknowledged:** What makes this wrong

## Skill Dependencies

```
biotech-coordinator (7 refs)
    │   ├── PATTERN_TRACKING.md (master inventory)
    │   ├── 5pter-template.md, skill-iteration-guide.md
    │   ├── team-roster.md, kol-integration.md
    │   └── street-expects-integration.md, PERSISTENCE.md
    │
    ├── reverend-bayes (13 refs)
    │   ├── analytical-rules.md (48 rules - ALWAYS READ)
    │   ├── analytical-questions.md, scorecard-rubric.md
    │   ├── cross-trial-comparison.md, read-through-analysis.md
    │   ├── statistical-framework.md, pk-pd-exposure-response.md
    │   ├── randomized-withdrawal-design.md, novel-target-safety.md
    │   └── TAs: immuno-inflammation, cv-inflammation, pah-pulmonary, ta-hematology-mf
    │
    ├── john-snow (7 refs)
    │   ├── launch-analogs.md, pricing-access.md
    │   ├── bolus-product-commercial.md, cell-therapy-commercial.md
    │   ├── product-transition-commercial.md, intraquarter-commercial-tracking.md
    │   └── TAs: ta-hidradenitis-suppurativa.md
    │
    ├── graham (2 refs)
    │   ├── rnpv-methodology.md
    │   └── short-thesis-validation.md
    │
    ├── keynes (6 refs)
    │   ├── catalyst-playbook.md, m-and-a-playbook.md
    │   ├── sentiment-indicators.md, positioning-analysis.md
    │   └── insider-activity.md, technical-basics.md
    │
    └── simons (3 refs)
        ├── exposure-limits.md, correlation-clusters.md
        └── position-sizing.md
```

## Example Routing

### Example 1: Full Analysis Request

**User:** "Can you analyze CRVS and tell me if we should own it?"

**Coordinator action:**
1. Gather context: Trial data, competitive set, market size, current price
2. Run `reverend-bayes` → Get PoS for Phase 2 AD
3. Run `john-snow` → Get peak sales given TPP
4. Run `graham` → Get fair value, implied PoS, recommendation
5. Synthesize into IC memo

### Example 2: Targeted Question

**User:** "What's the PoS for ZEUS?"

**Coordinator action:**
1. Route directly to `reverend-bayes`
2. Use read-through analysis (CANTOS data exists)
3. Output: PoS estimate only
4. Note: "Run john-snow and graham if you want fair value"

### Example 3: Short Thesis

**User:** "Is ALMS a good short?"

**Coordinator action:**
1. Run `reverend-bayes` → PoS for Phase 3 (likely high given MOA)
2. Run `john-snow` → Peak sales (likely low if undifferentiated)
3. Run `graham` with focus on short thesis validation:
   - Valuation floor analysis
   - Catalyst asymmetry
   - Is weighted EV actually negative?
4. Output: Short recommendation with explicit risk/reward

### Example 4: Partial Input

**User:** "Assuming 60% PoS and $1.5B peak, what's XYZ worth?"

**Coordinator action:**
1. Skip `reverend-bayes` (PoS provided)
2. Skip `john-snow` (peak sales provided)
3. Run `graham` directly with provided inputs
4. Output: Fair value and recommendation

---

## Cross-Reference Map

### Multi-Skill Reference Files

Some reference files serve multiple skills:

| File | Primary Skill | Also Useful For |
|------|---------------|-----------------|
| `ta-hidradenitis-suppurativa.md` | john-snow | reverend-bayes (IL-1 pathway read-through) |
| `cell-therapy-commercial.md` | john-snow | reverend-bayes (sequencing effects on efficacy) |
| `catalyst-playbook.md` | keynes | reverend-bayes (catalyst timing) |
| `analytical-rules.md` | reverend-bayes | ALL skills (provenance rules 40-45) |
| `skill-iteration-guide.md` | biotech-coordinator | ALL skills (provenance protocol) |

### Cross-Skill Patterns

| Pattern | Where Documented | When to Apply |
|---------|------------------|---------------|
| **Data provenance** | analytical-rules.md #40-45, skill-iteration-guide.md | ANY analysis citing trial data |
| **Cross-indication read-through** | analytical-rules.md #21b | When pathway is validated in adjacent indication |
| **Isoform-specific read-through** | analytical-rules.md #21c | When comparing single vs dual blockers |
| **Inverse dose-response** | analytical-rules.md #15b | When Ph2 high dose underperforms middle |
| **Competitor sequencing** | cell-therapy-commercial.md | When order of therapies affects efficacy |

### Citation Requirements (All Skills)

Every output should include a Sources section. **→ See `references/5pter-template.md` for format.**

**Rule:** If you cite a trial result without a source, flag it as "UNVERIFIED - need to confirm" or say "I don't have [X] data - worth checking."

---

## Reference Files

| File | Use When |
|------|----------|
| `references/PATTERN_TRACKING.md` | **Start here** - master inventory, case study index, pattern catalog |
| `references/PERSISTENCE.md` | Recovery protocol if files missing |
| `references/5pter-template.md` | Writing investment memos |
| `references/skill-iteration-guide.md` | Adding new patterns, provenance protocol |
| `references/team-roster.md` | **Team profiles, coaching notes, role clarity** |
| `references/kol-integration.md` | KOL call planning and synthesis |
| `references/street-expects-integration.md` | Consensus expectations analysis |

---

## Skill Gaps and Future Development

| Area | Current State | Needed |
|------|---------------|--------|
| **graham** | 3 files (light) | Add: comparable transactions, SBC frameworks, LOE scenarios |
| **simons** | 4 files | Add: pair trade construction, factor exposure |
| **TA-specific** | HS, heme-MF, PAH only | Need: oncology solid tumor, CNS, rare disease |
| **Platform** | None | Need: gene therapy valuation, cell therapy lifecycle |

### Priority Additions (Next Sessions)

1. `graham/references/comparable-transactions.md` - M&A comp frameworks
2. `graham/references/probability-weighted-scenarios.md` - Scenario math
3. `simons/references/pair-trade-construction.md` - Hedging methodology
4. `reverend-bayes/references/ta-oncology-solid.md` - Solid tumor endpoints
