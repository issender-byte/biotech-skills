# Analytical Rules

48 rules (45 main + 3 sub-rules) for evaluating clinical trial design, data integrity, and thesis validation. Apply these to ANY thesis - your own analysis, sellside reports, or management claims.

---

## Statistical Design Rules

1. **MMRM vs observed data** - MMRM includes all data (completers + dropouts), which can deflate SD vs observed. If company reports Ph2 "observed" SD but powers Ph3 assuming MMRM deflation, they may be sandbagging.

2. **SAP flexibility** - Ask whether SAP allows switching from ANCOVA to Wilcoxon if data non-normal. Flexibility = less commitment to assumptions.

3. **SD tracking** - If blinded SD is tracking below assumption, trial may be overpowered. If above, may be underpowered at margin.

4. **Power for street bar vs stats sig** - A trial can be well-powered for statistical significance but underpowered for the EFFECT SIZE the street expects. Calculate both.

---

## Endpoint Decomposition Rules

5. **Composite endpoint dissection** - Break composites into components. A drug that moves 3/7 domains strongly but 4/7 not at all may "hit" but have limited clinical meaning.

6. **Biomarker-clinical domain mismatch** - If mechanism affects biomarker X but endpoint has domains Y and Z, biomarker success may not translate. (Example: SVR in MF doesn't drive systemic symptoms; only 3/7 TSS domains are spleen-related.)

7. **Scale normalization** - Different trial generations may use different scales (60pt vs 70pt). Always rescale before cross-trial comparison. Formula: (result) × (new scale / old scale).

8. **"At vs by" timing manipulation** - "By Week 24" includes early responders in numerator but excludes ongoing non-responders from denominator. Always ask for "at Week 24" data.

---

## Missing Data & Dropout Rules

9. **Treatment d/c ≠ Study d/c** - Patients can stop drug but remain in study and provide endpoint data. Conflating these inflates "missing data" concerns.

10. **Dropout classification by reason** - SCT dropouts in heme trials are often BEST responders (disease resolved). AML transformations are failures. Track each dropout's fate individually.

11. **n reconciliation** - If n=X for endpoint A but n=Y for endpoint B, identify each "missing" patient. Their fate is often more informative than completers.

12. **Extension study absence** - If no extension study and trial runs to survival, dropout patterns differ from typical trials with OLE rollover.

---

## Dosing & Exposure Rules

13. **Dose intensity as efficacy predictor** - If >30% dose reduce the experimental arm, efficacy may be underestimated. If >30% dose reduce the BACKBONE in combinations, you're "fighting with one hand tied behind your back."

14. **Concomitant medication confounds** - If 85% have AE X in Ph1 despite prophylaxis, most Ph3 patients will get rescue medication. This may confound symptom/inflammation endpoints.

15. **Dose reduction protocol availability** - Can patients step down (60→40→20mg) and stay in trial? This affects both completion rates and efficacy interpretation.

15b. **Inverse dose-response red flag** - If Ph2 shows HIGH dose performing WORSE than MIDDLE dose (Luti: 300mg EW 14% delta vs 300mg EOW 24% delta), question whether dose optimization was suboptimal. Creates uncertainty for competitors extrapolating from that data.

---

## Historical Comparison Rules

16. **Baseline severity anchoring** - Know baseline severity in historical trials. Sicker baseline → larger absolute improvement but similar relative improvement.

17. **Futility analysis back-solve** - Passing futility tells you data aren't dead, not that they're winning.

18. **Prespecified interim bars** - If company shows interim beat futility bar, ask what the EFFICACY interim bar was. Futility ≠ success.

---

## Competitor Read-Through Rules

19. **Explain competitor failures** - If similar drug failed, demand specific explanation why your situation is different (dose, population, endpoint, timing).

20. **Subgroup anomaly flagging** - If competitor showed counterintuitive subgroup results (high-risk did better than low-risk), investigate whether your trial has same dynamics.

21. **Off-label competition dynamics** - Track whether competitors are being used off-label in your target population. Changes "white space" calculus.

21b. **Cross-indication read-through** - If Drug A (targeting pathway node X) works in Indication Y, it validates the pathway for drugs targeting upstream/downstream nodes. Example: AVTX-009 (IL-1β) success would validate inflammasome engagement for NLRP3/NEK7 inhibitors (BIOA, GLUE). Map the pathway before assuming read-through.

21c. **Isoform-specific read-through** - When comparing single-isoform vs dual-blocker, check prior single-isoform data in that indication. If IL-1α alone showed signal (bermekimab: 60% vs 10%), bull case for IL-1β alone must explain why dual isn't needed.

---

## Toxicity-Efficacy Linkage Rules

22. **AE-endpoint component linkage** - If drug causes fatigue (AE) and endpoint includes fatigue domain, how separated? If grade 3 anemia also worsens "abdominal discomfort," map which AEs affect which endpoint domains.

23. **Dose reduction cascade** - Toxicity → dose reduction → reduced efficacy → worse outcome. Model this cascade explicitly; don't assume dose reductions are benign.

24. **Published tox-efficacy correlations** - Check if prior trials published subgroup analyses by toxicity grade.

---

## Enrollment & Population Rules

25. **Enrollment criteria vs real-world** - If enrollment requires specific baseline symptoms, confirm patients CAN'T enroll with only excluded symptoms.

26. **High-risk subgroup inclusion** - Verify whether high-risk patients are included and stratified. They often behave differently.

---

## Data Integrity Rules

27. **Cross-check competitor's data** - Before accepting a bear thesis on competitor, verify the data claims. Bulls often strawman competitor efficacy.

28. **Durability curve comparison** - Use waterfall plots and K-M curves, not just responder rates. Duration of response matters more than rate.

29. **Subpopulation decomposition** - If one subgroup drives result (e.g., previously untreated), model the OTHER subgroup's contribution to understand market relevance.

30. **Competitor explanation requirement** - If similar MOA failed elsewhere, demand specific mechanistic explanation for why this trial is different.

---

## Missing Data Pattern Rules

31. **Dropout timing analysis** - Early dropouts (weeks 1-4) often different from late dropouts (months 6+). Early = tolerability; Late = efficacy or competing risk.

32. **Rescue medication tracking** - Heavy rescue use may mask underlying disease progression. Track % on rescue and timing.

33. **Hybrid imputation scrutiny** - Many trials use hybrid methods (LOCF for some, MMRM for others). Know which applies to your endpoint.

---

## Trial Design Red Flags

34. **Adaptive design exploitation** - Sample size re-estimation can mask early futility signals. Ask what triggered any mid-trial changes.

35. **Rolling enrollment** - If enrollment was slow initially then accelerated, population may have shifted (site selection, inclusion creep).

36. **Country/site mix shifts** - If Ph3 has different geographic mix than Ph2, different standard of care and placebo response expected.

37. **Protocol amendments timing** - Mid-study amendments to endpoints, visit schedules, or analysis plans = red flag. Unwind the "why."

---

## Mechanism-Efficacy Ceiling Rules

38. **Biomarker ceiling effect** - Beyond a threshold, more biomarker improvement may not translate to more clinical improvement. (Example: 10% and 50% spleen reduction may show similar symptom improvement.)

39. **Toxicity-symptom offset** - If drug mechanism causes toxicity that worsens the symptom endpoint (fatigue from heme tox worsening fatigue component of TSS), the drug is fighting itself. Net effect may be zero even with biomarker improvement.

---

## Data Provenance Rules

40. **Citation before assertion** - NEVER state specific numbers (response rates, deltas, n's) without a traceable source. "Bermekimab showed 37% vs 37%" requires citation. If you don't have a source, say "I don't have bermekimab data - worth checking."

41. **Distinguish data tiers** - Peer-reviewed publication > conference abstract > press release > analyst report > "I recall seeing" > fabrication. Label your confidence accordingly.

42. **Absence of mention ≠ Absence of data** - If an analyst doesn't cite a competitor trial, they may not have data (reasonable) or may be ignoring contrary evidence (concerning). Don't assume the latter without evidence.

43. **Check your own citations** - Before criticizing someone for "not addressing X," verify X exists as you characterize it. Inventing contrary evidence to critique someone is worse than the error you're criticizing.

44. **Source documents trump memory** - If you "remember" a trial result but can't find the source, flag it as uncertain. Memory is unreliable; documents are not.

45. **Hallucination red flags** - Be especially cautious when: (a) stating specific percentages, (b) claiming something "failed" or "succeeded," (c) characterizing data you haven't directly viewed, (d) the data conveniently supports your thesis.

---

## Quick Reference by Situation

| Situation | Rules to Apply |
|-----------|----------------|
| Evaluating Ph3 design | 1-4, 16-18 |
| Comparing to historical | 7, 16, 27-31 |
| High dropout rate | 9-12, 30-31, 36-37 |
| Combination trial | 13, 23 |
| Composite endpoint | 5-6, 8, 32-33 |
| Competitor failed | 19-21, **40-44** |
| Data looks too good | 35-37 |
| Symptom endpoint | 6, 14, 22, 38-39 |
| **Critiquing someone else's work** | **40-45** |
| **Stating trial results** | **40-42, 44-45** |

---

## Sources

- MF DD session (KPTI selinexor + rux): Rules 1-26
- KPTI bull/bear analysis: Rules 27-39
- GOSS PAH analysis: Subgroup skepticism patterns
- PGEN gene therapy: Dropout tracking patterns
- **AVTX bermekimab hallucination incident (Jan 2026): Rules 40-45** - Fabricated "37% vs 37%" data when critiquing analyst work; actual Tanni et al data was 60% vs 10%. Lesson: citation before assertion.

*See also: management-due-diligence.md for detailed DD frameworks and checklists*
