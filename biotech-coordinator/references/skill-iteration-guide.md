# Skill Iteration Guide

How to improve biotech analysis skills by extracting transferable frameworks from specific cases.

---

## ⚠️ MANDATORY DUAL-OBJECTIVE FOR ALL WORK

**Every piece of submitted work serves TWO purposes. BOTH must be explicitly addressed.**

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  OBJECTIVE 1: COACHING GAPS                                    │
│  Where is this person falling short?                           │
│  What can they be coached to improve?                          │
│                                                                 │
│  OBJECTIVE 2: PATTERN EXTRACTION                               │
│  What new analytical techniques did they use?                  │
│  What patterns should we codify that we haven't yet?           │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**If you only do coaching without pattern extraction:** You miss the opportunity to learn from good work.

**If you only do pattern extraction without coaching:** You miss the opportunity to develop the team.

**EVERY evaluation must produce:**
1. Coaching gaps identified (with specific examples and coaching script)
2. New patterns extracted (or explicit statement "No new patterns identified")
3. Updates to team-roster.md AND PATTERN_TRACKING.md

---

## Core Principle

**Extract the generalizable analytical move, not the specific case.**

The goal is to build skills that work across any ticker, any therapeutic area, any mechanism. Specific examples exist only to illustrate how frameworks apply.

---

## The Hierarchy

| Level | Content | Location | Token Cost |
|-------|---------|----------|------------|
| **Analytical Rules** | Abstract patterns that always apply | SKILL.md (top) | Low - always loaded |
| **Frameworks** | Step-by-step methodologies | SKILL.md or references/ | Medium |
| **Case Studies** | Specific examples illustrating frameworks | references/ (end of file) | Load on demand |

---

## When Processing New Material

### Step 1: Identify the Analytical Move

Ask: **"What is the generalizable thinking pattern here?"**

| Specific Case | Generalizable Pattern |
|---------------|----------------------|
| "NEK7 shares structure with GSPT1" | Check structural homologs for toxicity signals |
| "Entrectinib hits NEK7 but TRK is 100x more potent" | Dirty drug precedent requires selectivity gap analysis |
| "SOL-1 patients are milder than Lucentis MARINA" | Map baseline characteristics before cross-trial comparison |
| "GKOS discontinuing Photrexa forces Epioxa adoption" | Product transition can force premium pricing |

### Step 2: Write the Rule First

Formulate as an imperative instruction that applies broadly.

**Bad (too specific):**
> "When analyzing NEK7, check if it shares structure with GSPT1"

**Good (generalizable):**
> "When evaluating novel target safety, identify structural homologs and assess their toxicity profiles"

### Step 3: Determine Location

| If the pattern... | Put it in... |
|-------------------|--------------|
| Always applies when skill is invoked | Analytical Rules (SKILL.md) |
| Applies in specific situations | Framework section (SKILL.md or references/) |
| Is detailed methodology with multiple steps | Reference file |
| Is a worked example showing framework application | Case Studies section (end of reference file) |

### Step 4: Add Case Study Last

After the framework is written, add the specific case as an illustration:

```markdown
## Case Studies

*Case studies illustrate how the frameworks above are applied.*

### Case Study 1: [Ticker/Situation]

**Context:** [Brief setup]

**Framework X Applied:**
- [How framework was used]
- [What was found]
- Assessment: [Conclusion]
```

---

## Reference File Structure

Every reference file should follow this structure:

```markdown
# [Topic] Framework

[One-line description of what this framework does]

---

## When to Use This Framework

[Table of triggering situations]

---

## Framework 1: [Name]

### The Question
[What analytical question does this framework answer?]

### Methodology
[Step-by-step approach]

### Interpretation
[How to translate output to PoS/commercial/valuation impact]

---

## Case Studies

[Examples at the END showing framework application]
```

---

## Quality Checks

### The Abstraction Test
> "Could this rule apply to a different ticker in a different therapeutic area?"

If no, it's too specific.

### The Framework Test
> "Does this framework answer a clear analytical question?"

Every framework should start with "The Question" it answers.

### The Case Study Test
> "Is the specific example at the END, separate from the framework?"

Case studies prove frameworks work. They don't explain how frameworks were invented.

### The Token Efficiency Test
> "Is this pattern placed at the right level of the hierarchy?"

- Core rules → SKILL.md (always loaded)
- Detailed methodologies → Reference files (loaded on demand)
- Specific examples → Case studies at end of reference files

---

## Anti-Patterns to Avoid

### 1. Example-First Writing
**Bad:** Starting with "When we analyzed GLUE, we found..."

**Good:** Starting with "When evaluating novel target safety..."

### 2. Ticker-Specific Rules
**Bad:**
> "For GLUE, check NEK7's relationship to GSPT1"

**Good:**
> "For any novel target, identify structural homologs and assess their toxicity profiles"

### 3. Missing Quantification
**Bad:**
> "If there's a structural homolog risk, be more careful about safety"

**Good:**
> "Structural homolog to toxic protein, selectivity uncertain → -10-15% PoS adjustment"

### 4. Burying Frameworks in Examples
**Bad:** Framework explanation interleaved with specific case details

**Good:** Clean framework first, then "see Case Study 1 for example application"

---

## Iteration Workflow

When a new email thread, analysis, or post-mortem arrives:

```
1. READ the material

2. ASK: "What analytical move happened here?"
   - What question was being answered?
   - What data/logic was used?
   - What conclusion was reached?

3. ABSTRACT to a rule
   - Remove ticker names
   - Remove specific numbers (unless they're benchmarks)
   - Write as imperative instruction

4. LOCATE where it belongs
   - New rule? → Add to Analytical Rules
   - New framework? → Add section to SKILL.md or create reference file
   - Extends existing framework? → Update existing reference file
   - Just a good example? → Add as case study

5. VERIFY abstraction quality
   - Run quality checks above
   - Ensure case study is at END, not embedded

6. UPDATE pattern tracking
   - Log source conversation
   - Mark implementation status
```

---

## Key Principles

1. **Frameworks first, examples last** - The structure should be: Question → Methodology → Interpretation → [Case study at end]
2. **Rules are ticker-agnostic** - If it mentions a specific company, it's not abstract enough
3. **Quantify the impact** - Every framework should connect to a PoS adjustment, commercial estimate, or valuation input
4. **One framework, one question** - Each framework should answer a single analytical question
5. **Case studies prove, not explain** - Examples show that the framework works, not how it was invented

---

## Work Evaluation Protocol

**CRITICAL: Every submitted piece of work serves TWO purposes:**
1. **Coaching identification** - Where is this person falling short? What can they improve?
2. **Pattern extraction** - What new analytical techniques did they use that we haven't codified?

**Both must be explicitly addressed for every case study or work submission.**

### Evaluation Template

When reviewing any analyst work, complete this template:

```
WORK EVALUATION: [TICKER] by [ANALYST]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PART 1: COACHING IDENTIFICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

What they did well:
1. [Specific strength with example]
2. [Specific strength with example]
3. [Specific strength with example]

Where they fell short:
1. [Gap] - [Specific example] - [Why it matters]
2. [Gap] - [Specific example] - [Why it matters]
3. [Gap] - [Specific example] - [Why it matters]

Coaching script:
> "[Exact words to deliver feedback]"

Action items for analyst:
□ [Specific thing to do differently next time]
□ [Specific thing to do differently next time]

Update team-roster.md: Yes/No
- If yes, add to Progress Tracking table

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PART 2: PATTERN EXTRACTION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

New patterns identified (not already in framework):
1. [Pattern name] - [Description] - [Generalizable rule]
2. [Pattern name] - [Description] - [Generalizable rule]

Existing patterns applied well (reinforces framework):
1. [Pattern] from [file] - [How they applied it]
2. [Pattern] from [file] - [How they applied it]

Existing patterns missed (should have applied):
1. [Pattern] from [file] - [Should have used for X]
2. [Pattern] from [file] - [Should have used for X]

Files to update:
□ [File] - Add [pattern/rule]
□ [File] - Add [pattern/rule]
□ PATTERN_TRACKING.md - Add case study
□ team-roster.md - Update analyst profile

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Coaching Identification Checklist

For EVERY submission, check these dimensions:

**Stated View (5PTer requirement):**
□ Did they state a PoS / position / recommendation?
□ Is it a number, not "TBD" or "more work needed"?
□ Did they say what would change their view?

**Provenance (Rules 40-45):**
□ Are specific numbers sourced?
□ Any claims stated without citation?
□ Any "I recall" or unsourced assertions?

**Contrary Evidence (ZH pattern):**
□ Did they engage with bear case?
□ Did they address competitor failures/read-throughs?
□ Did they dismiss evidence without engaging?

**Clinical-Commercial Handoff:**
□ If clinical: Did they define what bar matters for commercial?
□ If commercial: Did they define clinical bar for scenarios?
□ Did they connect their work to the other side?

**Implied PoS / Valuation Link:**
□ Did they compare their view to market implied?
□ Can you act on this (buy/sell/size) or just inform?

**Role-Appropriate Scope:**
□ Did they stay in their lane?
□ Did they provide enough context for other roles?
□ Did they flag what they need from others?

### Pattern Extraction Checklist

For EVERY submission, ask:

**New Analytical Techniques:**
□ Did they do something clever we haven't codified?
□ Did they use a comparison/analog we haven't documented?
□ Did they surface a data source we don't have listed?

**New Frameworks:**
□ Did they structure analysis in a way we should replicate?
□ Did they create a useful table/template?
□ Did they ask a question we should always ask?

**New Rules:**
□ Did they flag a pitfall we haven't documented?
□ Did they identify a red flag pattern?
□ Did they note a common mistake to avoid?

**Therapeutic Area Specifics:**
□ Did they surface TA-specific benchmarks?
□ Did they identify relevant historical trials?
□ Should we create/update a TA reference file?

**Cross-Trial Insights:**
□ Did they make a useful cross-trial comparison?
□ Did they identify relevant analogs?
□ Did they note design differences that matter?

### Examples of Each

**Coaching Identification Examples:**

| Analyst | Work | Gap Identified | Coaching Delivered |
|---------|------|----------------|-------------------|
| ZH | AVTX pitch | Didn't address bermekimab/MAS825 | "Write the bear thesis first" |
| Ben | AVTX commercial | No clinical bar for scenarios | "Define what HiSCR delta separates $1.5bn from $750mn" |
| LA | AVTX mechanism | No stated view | "After all this work, where do you come out?" |
| WS | ACAD pitch | No implied PoS comparison | "What's market implying? Is 30% above or below?" |

**Pattern Extraction Examples:**

| Work | New Pattern Identified | Codified In |
|------|------------------------|-------------|
| AVTX (LA) | Bermekimab correction + IL-1α alarmin rationale | ta-hidradenitis-suppurativa.md |
| AVTX (Ben) | Molecule ownership history as diligence signal | (to add) |
| AVTX (Ben) | SSE vs DSE biosimilar dynamics | (to add) |
| ACAD (WS) | RW vs parallel delta compression with SLNO analog | randomized-withdrawal-design.md |
| ACAD (WS) | SD differences between OL and DB phases | (to add) |
| ACAD (WS) | E-R plateau as negative signal for "dose higher" thesis | pk-pd-exposure-response.md |

### Minimum Output Requirements

For every work evaluation, you MUST produce:

1. **Coaching section** with:
   - At least 2 specific strengths (with examples)
   - At least 1 specific gap (with example and coaching script)
   - Update to team-roster.md Progress Tracking

2. **Pattern extraction section** with:
   - Explicit statement of new patterns found (or "None identified")
   - List of existing patterns applied well
   - List of existing patterns missed
   - Files to update (or "None")

3. **Summary table:**

| Dimension | Grade | Key Observation |
|-----------|-------|-----------------|
| Stated view | [A-F] | [One line] |
| Provenance | [A-F] | [One line] |
| Role execution | [A-F] | [One line] |
| Contrary evidence | [A-F] | [One line] |
| New patterns | [0-N] | [List or "None"] |

---

## Data Provenance Protocol

**CRITICAL: This section exists because of a Jan 2026 incident where fabricated trial data was stated with false confidence, sent to a PM, and later corrected by an analyst with actual citations.**

### Before Stating Any Trial Result

```
PROVENANCE CHECK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CLAIM: [What I'm about to state]
SOURCE: [Where this data comes from]

□ Peer-reviewed publication (citation: _______)
□ Conference abstract (meeting, year: _______)
□ Press release (company, date: _______)
□ Analyst report (firm, analyst: _______)
□ From uploaded document in this conversation
□ I DON'T HAVE A SOURCE → Flag as uncertain

If no source, STOP. Either:
- Search for actual data
- Say "I don't have [X] data - worth checking"
- Omit the claim entirely

NEVER state specific numbers without a traceable source.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Hallucination Risk Factors

**High risk of hallucination when:**
- Stating specific percentages (37% vs 37%, 24.5% delta, etc.)
- Claiming a trial "failed" or "succeeded"
- Characterizing data I haven't directly viewed in this conversation
- The data conveniently supports the thesis I'm building
- Critiquing someone else for "ignoring" evidence

**Mitigation:**
- Cite the source inline when stating numbers
- If uncertain, bracket with confidence level: "IIRC..." or "I believe, but should verify..."
- When critiquing, verify the contrary evidence exists BEFORE asserting it

### The AVTX Bermekimab Incident (Jan 2026)

**What happened:**
1. Analyst (ZH) pitched AVTX without mentioning bermekimab competitor data
2. Claude generated critique claiming bermekimab showed "37% vs 37%, 0% delta"
3. Critique sent to PM, characterizing this as "the elephant in the room"
4. Another analyst (LA) corrected with actual citation: Tanni et al showed 60% vs 10% (+50% delta)
5. The fabricated "contrary evidence" was worse than the gap it criticized

**Lessons codified:**
- Rule #40: Citation before assertion
- Rule #43: Check your own citations before criticizing others
- Rule #45: Hallucination red flags

**The irony test:** If you're criticizing someone for "not engaging with evidence," you better be damn sure that evidence exists as you characterize it. Inventing evidence to criticize someone is worse than their original omission.

### Confidence Calibration

| Phrasing | When to Use |
|----------|-------------|
| "[Drug] showed X% vs Y% (Source, Year)" | Have citation, directly viewed |
| "IIRC, [drug] showed ~X% response" | Recall without citation - flag uncertainty |
| "I don't have [drug] data - worth checking" | No data, no recall |
| "Based on [uploaded document], [drug] showed..." | Data from current conversation |
| NEVER: "[Drug] showed X% vs Y%" without source | Creates false confidence |

### When Critiquing Analyst Work

```
CRITIQUE PROVENANCE CHECK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CRITIQUE: "Analyst didn't address [X]"

Before asserting:
□ Do I have actual data for [X]?
□ Is my characterization of [X] accurate?
□ Did I verify [X] exists as I'm describing it?
□ Am I critiquing an omission or critiquing different interpretation?

If I don't have verified data for [X]:
→ Don't assert it as a gap
→ Say "worth checking [X] data if available"
→ Focus critique on what IS in the pitch
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
