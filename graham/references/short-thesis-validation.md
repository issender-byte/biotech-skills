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
