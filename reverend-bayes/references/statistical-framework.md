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
