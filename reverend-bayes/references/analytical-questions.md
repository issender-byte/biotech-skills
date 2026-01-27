# Analytical Questions Framework

Structured questions to identify data inconsistencies and pressure-test investment theses. Modeled on institutional biotech investment debate.

## The Mike Metschl Method: Finding Data Inconsistencies

When reviewing trial data, systematically ask:

### Design Questions

1. **Randomization**: Did the randomization ratio change between cohorts? If yes, why?
   - 3:1 → 1:1 change suggests sponsor wanted more placebo data (could be good or bad)
   - Different ratios make cross-cohort pooling questionable

2. **Treatment duration**: Did it change between cohorts?
   - Longer treatment = more placebo drift (usually up, then down)
   - Makes efficacy comparison across cohorts harder

3. **Endpoints**: Are they measuring the same thing at the same timepoint?
   - Week 4 data vs week 8 data are not directly comparable
   - Net delta can change dramatically over time

### Placebo Questions

4. **Why is placebo performing differently between cohorts?**
   - If pooled placebo ≠ cohort-specific placebo, investigate why
   - Higher placebo in one cohort could be noise, or systematic

5. **How does placebo compare to historical benchmarks?**
   - Not just "historical range" - cite specific trials
   - If placebo is lower than historical, be skeptical (may not replicate)
   - If placebo is higher than historical, drug effect may be inflated

6. **What design features affect placebo response?**
   - Visit frequency (more visits = higher placebo)
   - Rescue medication rules
   - Background therapy allowed
   - Enrollment at disease flare vs stable

### Biomarker Questions

7. **Does the timecourse make sense?**
   - If MOA is "Drug → Biomarker change → Clinical effect"
   - Then biomarker should move before or with clinical
   - If clinical effect appears before biomarker, MOA may be incomplete

8. **Is there dose-response on biomarker?**
   - If higher dose → more biomarker change → more clinical effect, strong support
   - If biomarker doesn't show dose-response but clinical does, concerning

9. **Are the error bars acceptable?**
   - If 95% CI includes zero, it's noise
   - Wide error bars on n=12 are expected; don't overinterpret

10. **How does biomarker change compare to validated drugs?**
    - If dupilumab reduces TARC 80% and your drug reduces it 15%, that's a signal about potency

### Efficacy Questions

11. **What's the NET delta (drug - placebo)?**
    - Don't be fooled by impressive drug arm numbers with high placebo
    - Net delta is what matters for powering future trials

12. **Is there internal consistency?**
    - If cohort 3 and cohort 4 are same dose, why different results?
    - If one cohort's placebo = another cohort's drug arm, red flag

13. **What about secondary endpoints?**
    - If primary is positive but secondaries are flat, raises questions
    - Concordance across endpoints strengthens thesis

### Prior Treatment Questions

14. **What % had prior systemic therapy?**
    - This is a harder population to treat
    - Success here is more meaningful signal, not less

15. **How did prior-treatment patients perform vs naive?**
    - If drug works equally well in both, suggests robust mechanism
    - If drug only works in naive, may not differentiate

16. **What about truly refractory patients?**
    - Patients who failed multiple mechanisms
    - Small n but highly informative if signal present

## The Raj Patel Method: Building a Constructive Thesis

### Contextualize, Don't Dismiss

1. **Benchmark to specific drugs, not "historical range"**
   - "Placebo response of 34% is close to Dupixent trials at 15-20%" → that's actually concerning, not reassuring
   - Be specific about which trials you're comparing to

2. **Explain why data might look noisy but still be informative**
   - "The biomarker data is messy, but directionally consistent with MOA"
   - "Small n means wide CIs, but all point in same direction"

3. **Identify what would change your view**
   - "If Phase 2 placebo is >30%, I'd revise down"
   - "If dose-response flattens, reduces upside"

### Build the Bull Case with Evidence

4. **What's the single most important piece of evidence?**
   - "Activity in refractory patients is the key - not possible with placebo effect"
   - "Dose-response on both biomarker and clinical is compelling"

5. **Why might the skeptic be wrong?**
   - Address the bear case directly
   - "The placebo concern is valid, but Phase 2 design should normalize it"

6. **What's the upside scenario?**
   - "If they dose higher and see more biomarker movement, could be best-in-class"

### Quantify Everything

7. **PoS with rationale**
   - Not just "I'm bullish" but "65% PoS because..."
   - Explain what assumptions drive that number

8. **Valuation implications**
   - "At 25% PoS I get $7-14/sh, at 50% I get $15-25/sh"
   - Current price implies what PoS?

9. **Position sizing**
   - "Fine at current size" vs "would add on pullback" vs "would trim at $X"

## Red Flag Checklist

Automatic concerns if:

- [ ] Placebo arm changed between cohorts without explanation
- [ ] Design features changed (randomization, duration) mid-trial
- [ ] Biomarker moves opposite to expectation
- [ ] Clinical effect appears before biomarker effect with mechanistic drug
- [ ] No dose-response on either biomarker or clinical
- [ ] Efficacy only in one cohort but not replicated
- [ ] Company highlights relative numbers but hides absolute/net delta
- [ ] Error bars on biomarker include zero
- [ ] Placebo response well below historical benchmarks (may not replicate)
- [ ] Dose cap binds in >30% of patients (exposure ceiling)
- [ ] E-R curve still rising at max achieved exposure (leaving efficacy on the table)

## Green Flag Checklist

Supportive if:

- [ ] Consistent direction across multiple cohorts
- [ ] Clear dose-response on biomarker AND clinical
- [ ] Biomarker kinetics match stated MOA
- [ ] Activity in refractory/prior-treatment patients
- [ ] Durability of response off treatment
- [ ] Secondary endpoints concordant with primary
- [ ] Placebo response in line with or above historical (conservative)
- [ ] Safety profile clean relative to mechanism expectations
- [ ] Exposure in optimal range of E-R curve
- [ ] Most patients achieve target exposure (not cap-limited)

## Exposure-Response (E-R) Questions

**The Mike Challenge Questions:**

17. **Can you show patient weight distribution?**
    - Validate that weight difference is meaningful
    - Calculate % of patients hitting dose cap

18. **Is the E-R curve from the same indication?**
    - Dravet E-R may not apply to LGS
    - Different diseases may have different E-R relationships

19. **Wouldn't mg/kg dosing equalize exposure?**
    - Not if there's a dose cap - heavier patients hit cap first
    - Calculate: cap ÷ target mg/kg = weight at which cap binds

20. **What's the source of the concentration data?**
    - Observed vs modeled can differ significantly
    - Observed quartile analysis often more robust

21. **How noisy is the E-R model?**
    - Wide confidence intervals = less reliable
    - Check if observed data matches model predictions

22. **Are concomitant medications affecting efficacy?**
    - Background meds can reduce efficacy (PD competition)
    - Background meds can change exposure (DDIs)
    - Compare allowed meds between your trial and comp

**The Raj E-R Thesis Elements:**

1. **Show the E-R curve** - Where does efficacy plateau?
2. **Calculate exposure differential** - Are patients achieving optimal range?
3. **Identify the ceiling** - What's limiting exposure (cap, tolerability, formulation)?
4. **Compare potency-adjusted exposure** - Not raw mg dose
5. **Quantify concomitant med impact** - Subgroup analysis by background therapy
6. **Propose design improvement** - "Enroll fewer patients on clobazam/valproate to juice efficacy"

## Cross-Trial Comparison Questions

**The Mike Method: Comparator Skepticism**

23. **Why did the comparator arm perform so differently than historical?**
    - Small n = high variance
    - Different dosing regimen (induction vs maintenance)
    - Different patient selection
    - Sponsor quality issues

24. **What's the appropriate benchmark range?**
    - Use multiple trials if available
    - Weight by n and sponsor quality
    - Big pharma n=1000 > small biotech n=40

25. **Is transitive efficacy logic valid here?**
    - Same line of therapy?
    - Same population?
    - Same endpoint definitions?
    - Comparator performed normally?

26. **What specific threshold would be "clearly derisking"?**
    - Set explicit bars before data drops
    - "Need >93% CR to derisk 1L" not "hope it's good"

27. **What's the spread between positive and failed trials?**
    - Positive trials showed ~5% delta over SOC
    - Failed trials showed ~2% delta
    - Your drug needs to beat the positive trial delta

**The Leo Thesis Elements:**

1. **Build the efficacy hierarchy** - Drug A > Drug B > Drug C from head-to-head or cross-trial
2. **State explicit PoS for specific thresholds** - "65% PoS for >90% CR"
3. **Identify what data would derisk** - Monotx derisks combo, combo derisks label expansion
4. **Connect efficacy to durability** - CR rate vs CR durability vs EFS/PFS

## Commercial Launch Analysis Questions

**The Raj Launch Pattern:**

28. **Has first-mover launch underwhelmed expectations?**
    - Track scripts if available
    - Compare to pre-launch TAM assumptions
    - Note sellside awareness of tracking

29. **Is your stock/space at risk of de-rating?**
    - Products viewed as similar?
    - First-mover sets expectations?
    - "Nobody cared that X was a little bit better"

30. **What would differentiate from first-mover?**
    - Different MOA?
    - Different patient population?
    - Meaningfully better efficacy (not just "little bit better")?

31. **What's the timeline for launch read-through?**
    - When will we know launch trajectory?
    - J-code timing?
    - How long to wait before declaring weak?

**The Alex Counterpoint:**

- Time between now and your launch may allow differentiation
- Acquisitions can provide exit even if space de-rates
- First-mover problems (reimbursement, site setup) may help followers

## Short Thesis Validation Questions

**The Mike Contrarian Method:**

32. **Are we projecting the right metric?**
    - $ growth after price cut understates volume growth
    - Volume growth after price increase overstates demand
    - Always decompose price × volume

33. **What's the valuation floor?**
    - Net cash per share
    - Value of other pipeline assets
    - Platform value if lead fails
    - Acquisition premium potential

34. **What failure probability is priced in?**
    - Current EV minus cash = implied pipeline value
    - Compare to success scenario value
    - Back into implied PoS

35. **Is catalyst asymmetry favorable for a short?**
    - Calculate weighted EV across scenarios
    - If EV > 0, short doesn't work on risk/reward
    - "Stat sig but underwhelming" may still move stock up

36. **Are the mechanism comps truly comparable?**
    - Allosteric vs. orthosteric binding
    - Selectivity profile (pan-JAK vs. selective)
    - Same target ≠ same drug
    - E-R comparison requires molecular similarity

37. **What could make this short wrong?**
    - M&A / strategic interest
    - Hidden differentiation dimension
    - Pipeline optionality not reflected
    - Execution surprises

**The Raj E-R Ceiling Analysis:**

1. **Show the E-R plateau** - Higher exposure → marginal efficacy gain = ceiling
2. **Compare to better mechanisms** - TYK2 (70% PASI-75 plateau) vs. IL-23 (90%)
3. **Identify dose-response failure** - "Tripling dose gave minimal improvement"
4. **Apply to commercial** - If drug can't differentiate on efficacy, what's left?

**The Zhenhua Bear Construction:**

1. **Class-level thesis** - Is the entire class disadvantaged vs. alternatives?
2. **Intra-class ranking** - Is this drug worst-in-class?
3. **Commercial positioning** - Third to market with no differentiation
4. **Explicit NPV** - Show the math on peak sales assumptions
