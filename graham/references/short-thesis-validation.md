# Short Thesis Validation & Contrarian Sanity Checks

How to stress-test a short thesis (or any thesis) by asking the questions that could invalidate it. Critical for avoiding value traps and understanding risk/reward asymmetry.

---

## When to Use This Framework

| Situation | Use This Framework |
|-----------|-------------------|
| Evaluating a short position | Yes - what could go wrong? |
| Thesis seems "obvious" | Yes - what's priced in? |
| Comparing drugs across mechanism | Yes - are they truly comparable? |
| Extrapolating financial metrics | Yes - is the methodology appropriate? |
| Low market cap with binary event | Yes - is skew favorable? |

---

## The Mike Contrarian Method

When someone presents a bearish thesis, ask three categories of questions:

### 1. Methodology Sanity Checks

**"Are we measuring the right thing the right way?"**

#### Price vs. Volume Decomposition

**The problem:** If a drug took a price cut but you're extrapolating $ growth, you're understating true demand.

```
Example: Sotyktu
- Sales flat y/y in $ terms
- But volume grew 50-60%
- Implies: Price cut masked real demand growth
- Linear $ extrapolation would UNDERSTATE forward trajectory
```

**Questions to ask:**
- Is the projection based on $ or units?
- Has there been a recent price change?
- What's the net price trend vs. list price?
- Are payer dynamics (rebates, access) changing?

#### Metric Selection

| If projecting... | Check for... |
|------------------|--------------|
| Revenue | Price changes, rebate dynamics |
| Scripts | New patient vs. refills, duration |
| Market share | Denominator changes, market growth |
| Peak sales | Analog selection, pricing assumptions |

### 2. Valuation Floor / Risk-Reward Asymmetry

**"Does the current price already reflect the bear case?"**

#### The Mike Question

"At $1.2bn cap and $850mm EV, and an MOA that is almost certain to hit stats, the skew seems up to me."

**Framework:**

```
Current EV: $850M
Cash: ~$350M
Pipeline value at current price: ~$500M implied

If trial hits (high probability given MOA):
- Stock likely doesn't go to cash
- Could re-rate to $1.5-2B on positive data
- Upside: +50-100%

If trial misses (low probability):
- Stock goes toward cash (~$350M)
- Downside: ~60%

But if P(hit) = 80%, expected value favors long, not short
```

**Questions to ask:**
- What's the implied pipeline value at current price?
- What probability of failure is priced in?
- Is there a floor (cash, other assets)?
- What's the magnitude of move on hit vs. miss?
- Is the skew actually favorable for a short?

#### Valuation Floor Sources

| Floor Type | How to Calculate |
|------------|------------------|
| Cash | Net cash per share |
| Other pipeline | Value of non-target assets |
| Acquisition value | Strategic premium potential |
| Royalty/milestone | Contracted payments |
| Platform value | Even if lead fails, what's platform worth? |

### 3. Mechanism Comparability

**"Are the comps actually comparable at a molecular level?"**

#### The Mike Question

"I'd also wanna make sure the comps we're talking about are all similarly allosteric inhibitors of TYK2 to make sure the exposure response stuff is apples to apples. It's possible that if one is an orthosteric inhibitor and more JAK-like, the efficacy could be greater."

**Why this matters:**
- Different binding sites = different pharmacology
- Allosteric vs. orthosteric inhibitors can have very different E-R curves
- "Same target" ≠ "same drug"

#### Molecular-Level Comparability Checklist

| Factor | Why It Matters |
|--------|----------------|
| **Binding site** | Allosteric vs. orthosteric = different kinetics |
| **Selectivity** | TYK2-selective vs. pan-JAK = different safety/efficacy |
| **Potency (IC50)** | Determines achievable target coverage |
| **Half-life** | QD vs. BID dosing affects trough coverage |
| **Metabolites** | Active metabolites can extend effect |

#### Example: TYK2 Inhibitor Comparison

| Drug | Binding Type | Selectivity | IC50 Coverage | Comparability |
|------|--------------|-------------|---------------|---------------|
| Sotyktu (deucravacitinib) | Allosteric | TYK2-selective | ~IC80 at Cmax | Reference |
| Nimbus TYK2 | Allosteric | TYK2-selective | ~IC80 24hr | Comparable |
| PF-06826647 | ? (less selective) | Less TYK2-selective | Good IC90 | Less comparable |
| ESK-001 | ? | ? | ? | Verify before comparing |

**If mechanism differs, E-R comparison may not hold.**

---

## Short Thesis Validation Checklist

Before putting on a short, answer:

### Bear Case Validation
- [ ] Is the bearish data interpretation correct?
- [ ] Are we using the right projection methodology?
- [ ] Are the comps truly comparable (mechanism, population, endpoint)?

### Valuation Check
- [ ] What's implied pipeline value at current price?
- [ ] What probability of failure is market pricing?
- [ ] Is there a valuation floor (cash, other assets)?
- [ ] What's the magnitude of move on positive vs. negative outcome?
- [ ] Is the risk/reward actually favorable for a short?

### Catalyst Asymmetry
- [ ] What's the probability of the bearish catalyst?
- [ ] How much of the bear case is already priced in?
- [ ] Could a "stat sig but underwhelming" outcome still move stock up?
- [ ] Is there acquisition/M&A risk to the short?

### Position Sizing
- [ ] Is the position size appropriate for the thesis confidence?
- [ ] What's the max loss scenario?
- [ ] Is there a stop-loss or cover trigger?

---

## The Zhenhua/Raj Bear Thesis (ALMS)

### Original Thesis

1. **TYK2 is a losing class** - PTGX oral IL-23 beat Sotyktu head-to-head
2. **ESK-001 is worst-in-class** - Lower PASI scores than competitors
3. **Third-to-market with no differentiation** - Sotyktu only $246M in 2024
4. **E-R analysis shows ceiling** - More exposure doesn't yield more efficacy

### Mike's Challenges

| Challenge | Bear Thesis Risk |
|-----------|------------------|
| **Price/volume decomposition** | Sotyktu volume growing 50-60% despite flat $; price cut may unlock more growth |
| **Valuation floor** | $850M EV with cash runway; "almost certain to hit stats" = skew up |
| **Mechanism comparability** | Are all TYK2 inhibitors allosteric? Different binding = different E-R |

### Revised Risk/Reward

| Scenario | Probability | Stock Move | EV |
|----------|-------------|------------|-----|
| Stat sig, differentiated | 20% | +100% | +$850M |
| Stat sig, undifferentiated | 60% | +20% | +$170M |
| Misses stats | 20% | -50% | -$425M |
| **Weighted EV** | | | **+$177M** |

**If EV is positive, short thesis doesn't work** - even if you're right about the drug being undifferentiated.

---

## E-R Ceiling Analysis (Raj's Contribution)

### When E-R Shows Efficacy Plateau

**Key insight:** If higher exposure doesn't yield better efficacy, the drug class may have a ceiling.

#### Sotyktu E-R Analysis

| Exposure (Cavg) | Relative to Approved | Efficacy Gain |
|-----------------|---------------------|---------------|
| 20 ng/mL | 1x (approved dose) | Baseline |
| 100 ng/mL | 5x | Marginal improvement |

**Interpretation:** "Even patients who had 5x more exposure only had incremental benefit" → efficacy plateau

#### Stelara E-R vs. Pure IL-23 Inhibitors

| Drug | Mechanism | PASI-75 Plateau |
|------|-----------|-----------------|
| Stelara | IL-12/IL-23 (like TYK2) | ~70% |
| Skyrizi | Pure IL-23 | ~90% |
| Tremfya | Pure IL-23 | ~90% |

**Interpretation:** TYK2/IL-12+IL-23 mechanism has lower ceiling than pure IL-23.

#### Nimbus Dose-Response Failure

| Dose | PASI Reduction | Delta vs. Lower Dose |
|------|----------------|---------------------|
| Lower | X% | Baseline |
| 3x higher | X+small% | Minimal improvement |

**Interpretation:** "Failed to show much of a dose response despite tripling the dose" → ceiling reached

### When to Trust E-R Ceiling Analysis

| Condition | Trust E-R Ceiling |
|-----------|-------------------|
| Multiple drugs in class show same plateau | High |
| Clear pharmacological explanation | High |
| Small n, early phase | Medium |
| Single drug, single trial | Low |
| Mechanism allows for differentiation | Revisit |

---

## Commercial Projection Pitfalls

### Price vs. Volume Confusion

**Scenario:** Sotyktu sales flat y/y, so bear thesis extrapolates flat growth

**Reality check:**
- Volume grew 50-60% y/y
- Sales flat because of price cuts / rebates
- BMS pushing volume via patient connect platform
- Forward $ growth could accelerate if price stabilizes

**Correct methodology:**
1. Project volume trajectory (units/scripts)
2. Apply expected net price
3. Adjust for access / payer dynamics

### Third-to-Market Discount

**Bear thesis:** "Third to market with no differentiation should have minimal sales"

**Counterpoint (implicit):**
- Third-to-market can still capture share if differentiated on convenience, safety, or access
- Payer strategies may favor later entrants
- Some physicians wait for more options before adopting

**Question to ask:** Is there ANY dimension of differentiation, even if not efficacy?

---

## Integration with Main PoS Framework

### Where Short Validation Fits

| Pillar | Short Validation Questions |
|--------|---------------------------|
| 1. Trial Design | Is the trial powered to show differentiation? |
| 2. Population | Same population as comps? |
| 3. Comparator | Are comps truly comparable (mechanism)? |
| 4. Efficacy | Is there an E-R ceiling? |
| 5. Competitive | Is third-to-market really death? |
| 6. Execution | Any M&A risk to the short? |

### Short-Specific Additions

| Factor | What to Check |
|--------|---------------|
| Valuation floor | Cash, other pipeline, acquisition value |
| Catalyst asymmetry | Magnitude of up vs. down move |
| Implied probability | What failure rate is priced in? |
| Projection methodology | Price vs. volume, metric selection |

---

## Template: Short Thesis Validation

```
═══════════════════════════════════════════════════════════════
SHORT THESIS VALIDATION
Company: [Name] | Ticker: [Symbol]
Catalyst: [Event] | Timing: [Date]
═══════════════════════════════════════════════════════════════

BEAR THESIS SUMMARY:
1. [Point 1]
2. [Point 2]
3. [Point 3]

METHODOLOGY SANITY CHECK:
- Projection metric: [$ / Volume / Share]
- Any recent price changes? [Y/N - impact]
- Are comps mechanism-comparable? [Y/N - detail]
- Is E-R analysis applicable? [Y/N - caveats]

VALUATION FLOOR ANALYSIS:
- Current market cap: $[X]
- Net cash: $[Y]
- Implied pipeline value: $[X-Y]
- Other assets: [List]
- Acquisition premium potential: [Y/N]

CATALYST ASYMMETRY:
| Scenario | Probability | Stock Move | $ Impact |
|----------|-------------|------------|----------|
| Bull case | X% | +Y% | +$Z |
| Base case | X% | +Y% | +$Z |
| Bear case | X% | -Y% | -$Z |
| **Weighted EV** | | | $[Sum] |

Is weighted EV negative? [Y/N]
If NO → Short thesis doesn't work on risk/reward

CONTRARIAN RISKS:
1. [What could make the short wrong?]
2. [What's not priced in that could go right?]
3. [Any M&A / strategic interest?]

RECOMMENDATION:
[Short / Don't Short / Reduce Size / Wait for Better Entry]
═══════════════════════════════════════════════════════════════
```

---

---

## AA vs Full Approval Pathway Risk

### The Pattern

**If a competitor is on track for full approval before your accelerated approval (AA) PDUFA, FDA may question whether AA is still appropriate.**

From MM's DYN analysis: *"The street remains concerned that a full approval for RNA ahead of DYN's AA PDUFA might put DYN's AA at risk."*

### Why This Matters for Valuation

| Scenario | AA Likelihood | Valuation Implication |
|----------|---------------|----------------------|
| No competitor with approval | High | Standard AA timeline |
| Competitor with same-mechanism full approval | Lower | Regulatory uncertainty = discount |
| Competitor with different-mechanism full approval | Medium | May still have unmet need argument |
| Competitor full approval AFTER your AA | Low risk | AA bridges to your own full approval |

### Framework: AA Pathway Risk Assessment

```
AA PATHWAY RISK ANALYSIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Your drug: [Name] | Pathway: [AA/Full]
Competitor: [Name] | Pathway: [AA/Full]

1. TIMELINE COMPARISON
   Your PDUFA: [Date]
   Competitor PDUFA: [Date]
   Who files/approves first? [Competitor/You]

2. MECHANISM COMPARISON
   Same target? [Y/N]
   Same indication? [Y/N]
   Same patient population? [Y/N]
   Your differentiation: [List]

3. UNMET NEED ARGUMENT
   If competitor approved, what unmet need remains?
   - Different patient subgroup? [Y/N]
   - Better safety? [Y/N]
   - More convenient dosing? [Y/N]
   - Different MOA for non-responders? [Y/N]

4. FDA PRECEDENT
   Has FDA granted AA when full approval exists? [Y/N - examples]
   Recent FDA signaling? [Any relevant guidance]

RISK LEVEL: [High/Medium/Low]
VALUATION IMPACT: [X% discount to base case]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### FDA Precedent Analysis

| Scenario | FDA Typical Response | Examples |
|----------|---------------------|----------|
| AA before any approval exists | More willing to grant | Most oncology AA |
| AA in subpopulation not covered | May still grant | Specific mutations |
| AA for same population after full approval | Reluctant | Limited precedent |
| AA with meaningful differentiation | Case-by-case | Safety, convenience |

### Key Questions to Research

1. **Has FDA granted AA in this indication after full approval existed?**
   - If yes, what was the justification?
   - If no, is your situation different?

2. **What's the confirmatory trial requirement?**
   - If your confirmatory = competitor's pivotal, FDA may question redundancy
   - If confirmatory shows different population, stronger case

3. **What did FDA say at your EOP2/pre-BLA meeting?**
   - Any mention of competitive landscape?
   - Specific guidance on AA vs full approval path?

### Worked Example: DYN vs RNA in DM1

```
Your drug: DYN z-basivarsen | Pathway: AA (1Q28 PDUFA)
Competitor: RNA | Pathway: Full Approval (YE27 PDUFA)

1. TIMELINE
   RNA PDUFA: YE27 (full approval)
   DYN AA PDUFA: 1Q28
   Risk: RNA approved ~3 months before DYN's AA decision

2. MECHANISM
   Same target? Yes - both TfR1-DMPK knockdown
   Same indication? Yes - DM1
   Same population? Yes - adult DM1
   DYN differentiation: ?

3. UNMET NEED
   If RNA approved: What unmet need does DYN address?
   - Different mechanism? No (same)
   - Better efficacy? Unknown (Ph2 data "similar")
   - Better safety? Unknown
   - Better dosing? Unknown

4. FDA PRECEDENT
   No clear precedent for AA when full approval exists for same target/indication

RISK LEVEL: Medium-High
VALUATION IMPACT: Should discount AA pathway 10-20%
```

### Integration with Scenario Analysis

In your scenario table, include AA pathway risk:

| Scenario | Base PoS | AA Risk Adj | Final PoS | Peak Sales |
|----------|----------|-------------|-----------|------------|
| RNA succeeds, DYN AA granted | 50% | -10% | 40% | $X |
| RNA succeeds, DYN AA denied | 50% | N/A | 10% | Delay -$Y |
| RNA fails | 30% | N/A | 30% | $X (but Ph3 harder) |

### Bear Thesis: AA Pathway Risk

If building a bear case around AA pathway risk:

**Checklist:**
- [ ] Is competitor actually on track for full approval first?
- [ ] Is the mechanism/population truly identical?
- [ ] What's the FDA precedent for this scenario?
- [ ] Is management discussing this risk on calls?
- [ ] Is the market pricing this risk? (If not, potential short thesis)

**Caution:** This is a longer-term thesis. Short-term, competitor validation may lift all boats. The AA risk crystalizes only if competitor succeeds AND FDA questions your AA path.

---

## Key Takeaways

1. **Challenge the methodology** - Price vs. volume, metric selection, projection assumptions
2. **Check the valuation floor** - Cash, other assets, implied failure probability
3. **Calculate catalyst asymmetry** - Weighted EV must be negative for short to work
4. **Verify mechanism comparability** - Allosteric vs. orthosteric, selectivity, binding site
5. **Beware "obvious" shorts** - If everyone sees it, it's probably priced in
6. **Ask "what makes this wrong?"** - Best shorts survive contrarian challenge
7. **Model AA pathway risk** - If competitor has full approval path ahead of your AA, discount accordingly


---

## Worked Example: ACAD ADP-204 (Why the Short Doesn't Work)

### Background

WS completed clinical analysis of ACAD's ADP-204 (Remlifansirin) for Alzheimer's Disease Psychosis:
- Used cross-indication analysis (PDP vs ADP)
- Identified placebo rebound anomaly (10-15% vs expected 50%)
- Estimated effect size: 0.20 (vs company's 0.40 powered assumption)
- Calculated PoS: 20-25%

**WS's implicit conclusion:** "This is a short candidate - trial is underpowered and likely to fail."

**What WS missed:** The graham step - does the market already agree?

---

### Step 1: Current Market Data (January 2026)

| Metric | Value |
|--------|-------|
| Stock Price | $26.50 |
| Market Cap | $4.50B |
| Cash | $847M |
| **Enterprise Value** | **$3.65B** |
| 2025 Revenue | ~$1.07B |
| EV/Revenue | 3.4x |

---

### Step 2: Base Business Valuation

**NUPLAZID (Parkinson's Disease Psychosis):**
- 2025 guidance: $685-695M
- 2028 ambition: ~$1.0B
- Patent protection: Composition to 2030, Formulation to 2038
- LOE risk post-2030 for composition, but formulation extends to 2038
- Valuation: Mature drug with visible decline trajectory post-2030

**DAYBUE (Rett Syndrome):**
- 2025 guidance: $385-400M
- 2028 ambition: ~$700M
- Orphan drug exclusivity, first-in-class
- Discontinuation concerns (GI side effects ~25% attrition)
- Valuation: Growing but terminal value capped by patient population

**Base Business NPV Build-Up:**

| Component | Bear Case | Base Case | Bull Case |
|-----------|-----------|-----------|-----------|
| NUPLAZID NPV | $1.8B | $2.2B | $2.8B |
| DAYBUE NPV | $1.0B | $1.5B | $2.0B |
| Net Cash | $0.85B | $0.85B | $0.85B |
| **Total Base** | **$3.65B** | **$4.55B** | **$5.65B** |
| **Per Share** | **$22** | **$27** | **$33** |

**Key Finding:** Current EV ($3.65B) equals the BEAR CASE base business valuation.

---

### Step 3: Implied Pipeline Value

```
Implied Pipeline = Current EV - Base Business Value
```

| Scenario | Base Business Value | Implied Pipeline |
|----------|--------------------:|------------------:|
| Bear case | $3.65B | **$0** |
| Base case | $4.55B | **-$0.9B** |
| Bull case | $5.65B | **-$2.0B** |

**Critical Finding:** Market gives **zero to negative** credit to pipeline.

The stock is trading as if ADP-204 (and all other pipeline) will fail.

---

### Step 4: ADP-204 Success Case NPV

**If ADP-204 works:**

| Parameter | Estimate | Source |
|-----------|----------|--------|
| Peak sales (ADP + LBDP combined) | $2.5-3.0B | Company "illustrative" $4B, discounted for competition |
| ADP alone | $1.5-2.0B | ~50% of combined |
| Operating margin | 35-40% | CNS specialty model |
| Peak operating profit | $600-800M | |
| Terminal multiple | 8-10x | Pharma standard |
| **NPV at launch (2029)** | **$5-8B** | |
| **Discounted to today** | **$4.0-6.0B** | 3 years @ 10% |

Using midpoint: **ADP success case NPV = $5.0B**

---

### Step 5: Back-Solve Implied PoS

```
Implied PoS = Implied Pipeline Value / Success NPV
```

| Scenario | Implied Pipeline | Success NPV | **Implied PoS** |
|----------|------------------:|------------:|----------------:|
| Market @ bear base | $0 | $5.0B | **0%** |
| Market @ base base | -$0.9B | $5.0B | **<0%** |
| Generous (assume some pipeline credit) | $0.5B | $5.0B | **10%** |

---

### Step 6: Compare to WS's Estimate

| Source | ADP PoS Estimate |
|--------|------------------|
| **Market Implied** | **0-10%** |
| **WS Estimate** | **20-25%** |
| Street Consensus | 30-40% |
| Company Implied | 50-60%+ |

**WS's PoS (20-25%) is ABOVE market implied (0-10%).**

---

### Why the Short Doesn't Work

**The Logic:**
1. WS is bearish on ADP-204 (PoS 20-25%)
2. But market is MORE bearish (PoS 0-10%)
3. If WS is right, stock is fairly valued to cheap
4. If company is right, stock is significantly undervalued
5. Only if PoS is truly <10% (lower than WS thinks) is stock fairly valued

**The Edge WS Thought He Had:**
> "ADP-204 is underpowered, trial likely fails, short the stock"

**Reality:**
> Market already agrees (or is more bearish). No edge.

**When This Short WOULD Work:**
- If WS's PoS < market implied PoS
- Example: WS thinks PoS = 10%, market implies PoS = 40%
- Then WS has negative edge and short makes sense

---

### The Pattern: "Bearish ≠ Short"

| Scenario | Your PoS | Market Implied | Action |
|----------|----------|----------------|--------|
| Your PoS > Market | 40% | 20% | **LONG** |
| Your PoS ≈ Market | 30% | 25% | **HOLD** |
| Your PoS < Market | 20% | 40% | **SHORT** |
| **Your PoS > Market (even if low)** | **20%** | **10%** | **NOT A SHORT** |

**WS was in the last row.** His clinical analysis was good, but he never completed the valuation loop.

---

### Checklist: Before Recommending a Pipeline Short

- [ ] **Value base business conservatively** - What's the floor?
- [ ] **Calculate implied pipeline value** - EV minus base business
- [ ] **Back-solve implied PoS** - What failure rate is priced in?
- [ ] **Compare your PoS to market implied** - Is your PoS BELOW market?
- [ ] **If your PoS > market implied** - NOT a short (market already agrees)
- [ ] **Only short if your PoS < market implied** - You see MORE risk than market

**WS skipped steps 2-5.** Good clinical work doesn't automatically translate to good investment thesis.

---

### Integration: Complete the Chain

```
reverend-bayes: ES estimate → Power → PoS (WS did this well)
      ↓
john-snow: Peak sales estimate → Success case NPV
      ↓
graham: PoS → rNPV → implied PoS → YOUR PoS vs MARKET
      ↓
Decision: LONG if your PoS > market
          SHORT only if your PoS < market
          NO EDGE if your PoS ≈ market
```

**The edge comes from the GAP, not from absolute PoS level.**

A 20% PoS stock can be a buy if market implies 10%.
A 60% PoS stock can be a short if market implies 80%.

---

### ACAD Recommendation Summary

```
═══════════════════════════════════════════════════════════════
SHORT THESIS VALIDATION: ACAD ADP-204
═══════════════════════════════════════════════════════════════

CLINICAL ASSESSMENT (reverend-bayes):
- WS's PoS: 20-25%
- Methodology: Cross-indication analysis, placebo rebound, E-R ceiling
- Quality: Good clinical work

VALUATION ASSESSMENT (graham):
- Base business value: $3.65-4.55B
- Implied pipeline value: $0 to negative
- Market implied PoS: 0-10%
- WS's PoS vs Market: 20% vs 10% → WS is MORE BULLISH

CATALYST ASYMMETRY:
| Scenario | Prob (WS) | Stock Move | EV |
|----------|-----------|------------|-----|
| ADP hits | 20-25% | +50-100% | +$1-2B |
| ADP fails | 75-80% | -10-20% | -$0.5B |
| **Weighted EV** | | | **Positive** |

RECOMMENDATION: NOT A SHORT
- Market already prices in failure
- Weighted EV is positive even at WS's low PoS
- If WS is wrong and trial works, massive upside

What would make this a short:
- Stock rallies 50%+ before data
- Market re-rates to 40-50% implied PoS
- THEN WS's 20% view would be below market

═══════════════════════════════════════════════════════════════
```
