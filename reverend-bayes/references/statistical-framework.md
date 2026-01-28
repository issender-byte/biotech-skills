# Statistical Framework for PoS Assessment

Quantitative methods for probability of success estimation, including Bayesian updating and power analysis.

## Bayesian PoS Methodology

### Conceptual Framework

PoS = P(Trial Success | Available Data)

Where trial success typically means:
- Primary endpoint achieves statistical significance (p < 0.05)
- Effect size is clinically meaningful
- Safety is acceptable

### Step 1: Construct Prior Distribution

**Option A: Historical Base Rate Prior**

Use indication/phase-specific success rates as Beta distribution:
```
Prior ~ Beta(α, β)
where α = historical successes + 1
      β = historical failures + 1
```

Example: I&I Phase 3 historical ~50% success
- Prior ~ Beta(51, 51) → mean = 0.50, moderate confidence

**Option B: Informative Prior from Phase 2**

If Phase 2 data available with effect size δ and SE:
```
P(Phase 3 success) = P(true effect > MCID) × P(statistical significance | true effect)
```

Construct prior on true effect size:
```
δ_true ~ Normal(δ_phase2 × shrinkage_factor, SE_phase2 × inflation_factor)
```

### Step 2: Phase 2→3 Shrinkage Adjustment

**Historical shrinkage factors by therapeutic area:**

| TA | Mean Shrinkage | 80% Range | Notes |
|----|----------------|-----------|-------|
| I&I | 25% | 10-40% | Well-characterized |
| Oncology (targeted) | 20% | 5-35% | Biomarker-selected |
| Oncology (IO) | 30% | 15-50% | Higher variability |
| CNS | 35% | 20-55% | High placebo |
| CV | 20% | 10-35% | Large trials |

**Shrinkage distribution:**
```
Shrinkage ~ Beta(α_shrink, β_shrink)
Example for I&I: Beta(3, 9) gives mean ~25%, range 5-50%
```

**Adjusted effect size:**
```
δ_adjusted = δ_phase2 × (1 - Shrinkage)
```

### Step 3: Power-Based Success Probability

Given:
- Phase 3 N (sample size)
- Expected δ_adjusted
- α = 0.05 (one or two-sided per protocol)
- σ (standard deviation, from Phase 2 or literature)

**For continuous endpoint:**
```
Power = Φ(δ_adjusted × √(N/2) / σ - Z_{1-α/2})
where Φ is standard normal CDF
```

**For binary endpoint (difference in proportions):**
```
Power = Φ((p1 - p2) / √(p̄(1-p̄)(2/N)) - Z_{1-α/2})
where p̄ = (p1 + p2)/2
```

**For time-to-event (hazard ratio):**
```
Power = Φ(log(HR) × √(events/4) - Z_{1-α/2})
```

### Step 4: Bayesian Update

**Posterior PoS:**
```
P(Success | Phase 2) ∝ P(Phase 2 result | true effect) × Prior(true effect)
```

In practice, use Monte Carlo:
1. Draw δ_true from prior
2. Apply shrinkage draw
3. Calculate power given δ_adjusted
4. Repeat 10,000+ times
5. Posterior PoS = mean(power draws)

### Step 5: Credible Interval

Report 80% credible interval:
- 10th percentile of power draws = lower bound
- 90th percentile = upper bound

This captures uncertainty in effect size, shrinkage, and power.

## Power Analysis Reference

### Sample Size Rules of Thumb

**Continuous endpoint (two-arm, 1:1):**
```
N per arm ≈ 16 × (σ/δ)² for 80% power, α=0.05 two-sided
N per arm ≈ 21 × (σ/δ)² for 90% power
```

**Binary endpoint:**
```
N per arm ≈ 2 × (Z_{α/2} + Z_{β})² × p̄(1-p̄) / (p1-p2)²
```

**Time-to-event:**
```
Events needed ≈ 4 × (Z_{α/2} + Z_{β})² / log(HR)²
```

### Power Sensitivity Tables

**Continuous (SD=1, α=0.05 two-sided):**
| Effect Size (δ/σ) | N per arm (80% power) | N per arm (90% power) |
|-------------------|----------------------|----------------------|
| 0.2 (small) | 394 | 527 |
| 0.3 | 175 | 234 |
| 0.4 | 99 | 132 |
| 0.5 (medium) | 64 | 85 |
| 0.8 (large) | 25 | 34 |

**Binary (α=0.05 two-sided):**
| Control Rate | Treatment Rate | Δ | N per arm (80%) |
|--------------|----------------|---|-----------------|
| 20% | 35% | 15% | 121 |
| 20% | 40% | 20% | 64 |
| 30% | 50% | 20% | 81 |
| 40% | 60% | 20% | 97 |

**Hazard Ratio (α=0.05 two-sided, 80% power):**
| HR | Events Needed |
|----|---------------|
| 0.50 | 52 |
| 0.60 | 98 |
| 0.70 | 198 |
| 0.75 | 304 |
| 0.80 | 526 |

## Red Flags in Statistical Design

### Underpowering

**Warning signs:**
- Power calculated at optimistic effect size only
- No sensitivity analysis in protocol
- Phase 2 point estimate used without CI consideration
- Effect size assumes no shrinkage

**Adjustment:** If powered at δ_optimistic, calculate power at δ_conservative:
```
δ_conservative = δ_phase2 × 0.7 (30% shrinkage)
Re-calculate power at this effect size
```

### Multiplicity Issues

**Warning signs:**
- Multiple primary endpoints without α adjustment
- Multiple doses without clear primary
- Interim analyses without clear stopping rules
- Subgroup analyses pre-specified as primary

**Impact:** Effective α inflation → true PoS lower than nominal

### Placebo Assumption Errors

**Warning signs:**
- Placebo rate assumption below historical
- No sensitivity analysis on placebo rate
- Ignoring recent trials with higher placebo

**Adjustment:** Calculate power at pessimistic placebo rate:
```
δ_net = δ_treatment - δ_placebo_pessimistic
Power at δ_net
```

## Qualitative-to-Quantitative Bridge

### Pillar Score to PoS Adjustment

Use pillar scores to adjust base rate:

| Total Score (0-60) | Adjustment | Resulting Range |
|--------------------|------------|-----------------|
| 50-60 | +15% | Base + 15% |
| 40-49 | +5% | Base + 5% |
| 30-39 | 0% | Base rate |
| 20-29 | -10% | Base - 10% |
| <20 | -20% | Base - 20% |

### Hybrid Approach

1. Calculate Bayesian quantitative PoS
2. Calculate qualitative pillar total
3. If qualitative suggests concern not in quantitative (execution risk, competitive dynamics):
   - Apply 5-10% haircut
4. If qualitative suggests strength not in quantitative (experienced sponsor, fast enrollment):
   - Apply 5% uplift (cap at +10%)

## Event-Driven Trial Analysis

### Framework 1: Event-Driven Parameter Back-Solving

**The Question:** Given company's data timeline guidance for an event-driven trial, what does that imply about control arm performance and event trigger?

**When to use:** Company guides topline data in [timeframe], trial is event-driven (prespecified number of events triggers analysis), and you want to constrain the solution space.

**Methodology:**

1. **Gather inputs:**
   - Enrollment timeline (start, completion, rate per month)
   - Sample size (N)
   - Guided data readout date
   - Minimum follow-up required (if any)

2. **Back-solve for event requirements:**
   - Calculate months from enrollment completion to guided readout
   - Estimate minimum events needed = N × (1 - RFS_rate) for each arm
   - Map: what RFS rates yield required events by guided date?

3. **Build sensitivity table:**

   | Control Arm RFS | Event Trigger (% of N) | Creto Arm Must Achieve | Trial Hits? |
   |-----------------|------------------------|------------------------|-------------|
   | 50% | 50% | ≥70% | Check dates |
   | 55% | 55% | ≥72% | Check dates |
   | 60% | 60% | ≥75% | Check dates |

4. **Reality-check assumptions:**
   - Is event trigger plausible vs typical trials?
   - Does control arm estimate align with comps?
   - Are enrollment + event timing internally consistent?

**Example (CGON PIVOT-006):**
- N=364, enrolled by Sept 2025, guided 1H26 data
- Back-solving: requires ≤50-55% event trigger AND ≤55% control arm 12m RFS
- Implication: Trial parameters suggest aggressive biology driving faster events than company initially projected

**Key insight:** Data timing guidance constrains the solution space. Work backward to identify what must be true for guidance to hold.

---

### Framework 2: Enrollment Rate as Event Signal

**The Question:** What does faster-than-expected enrollment AND sample size reduction tell us about event accrual?

**Pattern:** If company (a) enrolled faster than comps AND (b) reduced sample size post-initiation → event accrual likely faster than planned → control arm doing worse than expected.

**Methodology:**

1. **Compare enrollment rates:**
   - Your company: patients/month
   - Comp trials in same indication: patients/month
   - Ratio = faster/slower than expected

2. **Check for sample size changes:**
   - Original design N vs current N
   - Timing of change (early vs late)
   - Disclosed reason (if any)

3. **Inference table:**

   | Enrollment | Sample Size | Likely Interpretation |
   |------------|-------------|----------------------|
   | Faster | Reduced | Events accruing faster → control arm worse |
   | Faster | Unchanged | Strong demand, events as expected |
   | Slower | Unchanged | Events as expected or slower |
   | Slower | Increased | Events slower than expected → control arm better |

**Example (CGON vs URGN):**
- CGON: ~18 pts/month, reduced from N=426 to N=364
- URGN ATLAS: ~10-11 pts/month, no size change
- Inference: CGON events accruing faster → control arm likely at lower end of expected range

**Caution:** Enrollment speed can also reflect site enthusiasm, referral patterns, competition for patients—not just event rates. Triangulate with other data.

---

## Output Format for Bayesian Mode

```
QUANTITATIVE PoS ESTIMATE

Prior:
- Base rate: [X%] (source: historical I&I Phase 3)
- Adjusted for: [MOA novelty -5%, strong Phase 2 +10%]
- Prior distribution: Beta([α], [β])

Phase 2 Data:
- Effect size: [δ] (95% CI: [lower, upper])
- Shrinkage assumption: [X%] (range: [Y-Z%])
- Adjusted effect: [δ_adj]

Power Analysis:
- Sample size: [N]
- Assumed SD/rates: [values]
- Power at adjusted effect: [X%]
- Power at conservative (30% shrinkage): [Y%]

POSTERIOR PoS: [XX%] (80% CI: [YY-ZZ%])

Key Sensitivities:
- If no shrinkage: [+X%]
- If placebo +5%: [-Y%]
- If effect lower CI: [-Z%]
```


---

## Framework 3: Effect Size Gap Power Analysis

### When to Use

You have:
- Company's powering assumption (ES_powered)
- Your own effect size estimate (ES_analyst)
- ES_analyst < ES_powered

**Goal:** Quantify how underpowered the trial is given your view, and translate to PoS.

### Step 1: Back-Solve Trial Parameters

If company powers at 80% for ES_powered (standard):

```
n per arm ≈ 2 × ((1.96 + 0.84) / ES_powered)²
n per arm ≈ 2 × (2.80 / ES_powered)²
n per arm ≈ 15.68 / ES_powered²
```

| ES_powered | n per arm (80% power) | Total N |
|------------|----------------------|---------|
| 0.30 | 175 | 350 |
| 0.35 | 128 | 256 |
| 0.40 | 98 | 196 |
| 0.45 | 78 | 156 |
| 0.50 | 63 | 126 |

### Step 2: Power at Your Effect Size

Given n per arm from Step 1, calculate power at ES_analyst:

```
λ (non-centrality) = ES_analyst × √(n per arm / 2)
Power = Φ(λ - 1.96)  [one-sided approximation]
```

**Quick Reference Table (n=100 per arm, α=0.05 two-sided):**

| ES_analyst | λ | Power |
|------------|---|-------|
| 0.10 | 0.71 | 11% |
| 0.15 | 1.06 | 18% |
| 0.20 | 1.41 | 29% |
| 0.25 | 1.77 | 42% |
| 0.30 | 2.12 | 56% |
| 0.35 | 2.47 | 69% |
| 0.40 | 2.83 | 81% |
| 0.45 | 3.18 | 89% |
| 0.50 | 3.54 | 94% |

**Scaling for different n:**
```
Power at n' = Power at n=100 scaled by √(n'/100)
```

### Step 3: Translate ES to Endpoint Units

```
Delta (points) = ES × SD
```

Need SD from:
- Phase 2 data (preferred)
- Literature comps
- Trial protocol/SAP

| Endpoint Type | Typical SD Range |
|---------------|------------------|
| Psychiatric scales (PANSS, SAPS) | 7-12 |
| Pain (NRS 0-10) | 2-3 |
| Rheum (ACR components) | Varies by measure |
| Resp (FEV1 % predicted) | 10-15 |
| Derm (EASI, IGA) | Scale-dependent |

### Step 4: PoS Calculation

```
PoS = P(hit stats) × P(approval | hit stats)
```

**P(approval | hit stats) adjustments:**

| Scenario | P(approval | hit) |
|----------|-------------------|
| Strong efficacy (ES > powered) | 90-95% |
| Adequate efficacy (ES ≈ powered) | 85-90% |
| Weak efficacy (ES = 50-75% of powered) | 70-85% |
| Marginal efficacy (ES < 50% of powered) | 50-70% |
| Prior regulatory concern (CRL history) | -10-15% |

### Step 5: Output Template

```
EFFECT SIZE GAP ANALYSIS: [TICKER] [TRIAL NAME]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TRIAL PARAMETERS:
- Primary endpoint: ____________
- Company's powered ES: ____
- Implied n per arm: ____
- Total N: ____

ANALYST VIEW:
- Estimated ES: ____
- Rationale: ____________
- ES gap: ____ (____% of powered)

POWER SENSITIVITY:
| ES | Power | Delta (SD=__) |
|----|-------|---------------|
| [analyst -0.05] | ___% | ___ pts |
| [analyst] | ___% | ___ pts |
| [analyst +0.05] | ___% | ___ pts |
| [powered] | 80% | ___ pts |

PoS CALCULATION:
- P(hit stats) at analyst ES: ____%
- P(approval | hit): ____%
- PoS: ____%

MARKET IMPLIED COMPARISON:
- Current implied PoS: ____%
- Gap (analyst - market): ____ pp
- Directional view: LONG / SHORT / NO EDGE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Worked Example: ACAD ADP-204

```
EFFECT SIZE GAP ANALYSIS: ACAD ADP-204
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TRIAL PARAMETERS:
- Primary endpoint: SAPS-H+D (CFB)
- Company's powered ES: 0.40
- Implied n per arm: ~100
- Total N: ~200

ANALYST VIEW (WS):
- Estimated ES: 0.20
- Rationale: PDP parallel delta 3.37 pts, ADP should be 
  lower based on cross-indication comparison + placebo 
  rebound anomaly (only 10-15% rebound in ADP RW)
- ES gap: 0.20 (50% of powered)

POWER SENSITIVITY (SD=8 assumption):
| ES   | Power | Delta    |
|------|-------|----------|
| 0.15 | 18%   | 1.2 pts  |
| 0.20 | 29%   | 1.6 pts  |
| 0.25 | 42%   | 2.0 pts  |
| 0.40 | 81%   | 3.2 pts  |

PoS CALCULATION:
- P(hit stats) at ES=0.20: 29%
- P(approval | hit): 70% (weak efficacy + PIMA CRL precedent)
- PoS: 20%

MARKET IMPLIED COMPARISON:
- Current implied PoS: [TBD - graham step]
- Gap (analyst - market): [TBD]
- Directional view: [TBD]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Common Pitfalls

| Pitfall | Problem | Fix |
|---------|---------|-----|
| Using powered ES as "expected" | Overstates PoS | Always discount for shrinkage |
| Ignoring SD uncertainty | Delta range too narrow | Use SD range, not point |
| Skipping P(approval\|hit) | PoS too high for weak efficacy | Apply regulatory haircut |
| No market comparison | Can't act on PoS | Complete the graham step |
| Point estimate only | False precision | Report range (ES ± 0.05) |

### Integration with Other Frameworks

This framework feeds into:
- **graham:** PoS → rNPV → fair value
- **keynes:** PoS gap vs market → position direction
- **simons:** PoS confidence → position sizing

**The complete chain:**
```
reverend-bayes: ES estimate → Power → PoS
      ↓
graham: PoS → rNPV → implied PoS from price
      ↓
keynes: PoS gap → directional view → catalyst timing
      ↓
simons: Conviction + edge → position size
```
