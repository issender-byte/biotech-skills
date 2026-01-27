# Persistence Protocol

How to prevent data loss across sessions when working with biotech skills framework.

---

## The Problem

Files in `/mnt/skills/user/` persist across sessions, BUT:
1. Sessions can be compacted mid-work
2. Files created but not saved before compaction are lost
3. Memory edits have character limits
4. Conversation history isn't always accessible

## The Solution: Triple-Redundancy

Every pattern extraction must update THREE places:

```
┌─────────────────────────────────────────────────────────────┐
│                    PERSISTENCE TRIANGLE                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│                    PATTERN_TRACKING.md                      │
│                    (Source of Truth)                        │
│                          ▲                                  │
│                         / \                                 │
│                        /   \                                │
│                       /     \                               │
│                      /       \                              │
│           SKILL.md ◄─────────► Reference Files              │
│           (Rules)              (Deep Content)               │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Mandatory Checklist: After Every Pattern Extraction

```
PATTERN PERSISTENCE CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. PATTERN_TRACKING.md UPDATED:
   □ Added to Source Conversation Index
   □ Added to Pattern Catalog (correct skill section)
   □ Marked implementation status
   □ Version history updated

2. SKILL.md UPDATED (if new rule):
   □ Rule added to Analytical Rules section
   □ Reference file added to Reference Files table
   □ Dependency tree updated in biotech-coordinator

3. REFERENCE FILE CREATED/UPDATED:
   □ File created in correct /mnt/skills/user/[skill]/references/
   □ Framework structure (Question → Methodology → Interpretation)
   □ Case study at end
   □ Checklist included

4. MEMORY UPDATED (if major addition):
   □ New ticker added to memory
   □ Key pattern summarized if room

5. VERIFICATION:
   □ Run: find /mnt/skills/user -name "*.md" ! -path "*/autonomous-integration/*" | wc -l
   □ Expected count: _____ (update after each session)
   □ File exists and has content

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Session Start Protocol

**EVERY new conversation in this project should:**

1. **Read PATTERN_TRACKING.md first** (per memory)
2. **Check file count:** `find /mnt/skills/user -name "*.md" ! -path "*/autonomous-integration/*" | wc -l`
3. **If count is wrong:** Alert user, check this file for recovery protocol

---

## Session End Protocol

**BEFORE ending any session with new patterns:**

1. Verify files exist: `ls /mnt/skills/user/*/references/`
2. Verify PATTERN_TRACKING.md updated
3. If time permits, run full audit

---

## Recovery Protocol

**If files are missing after a session:**

1. Check memory for expected file count
2. Search conversation history: `conversation_search` with ticker name
3. Recreate from conversation history
4. Update PATTERN_TRACKING.md to mark as recovered

---

## File Counts (Update After Each Session)

| Directory | Expected Files | Last Verified |
|-----------|----------------|---------------|
| biotech-coordinator/references/ | 7 | — |
| reverend-bayes/references/ | 17 | — |
| john-snow/references/ | 7 | — |
| graham/references/ | 4 | — |
| keynes/references/ | 6 | — |
| simons/references/ | 5 | — |
| **TOTAL REFS** | **46** | — |

**TOTAL FILES (6 SKILL.md + 46 refs):** 52+

---

## Case Study Index

| # | Ticker | Status | Primary Reference File |
|---|--------|--------|------------------------|
| 1 | CRVS | ✓ | immuno-inflammation.md |
| 2 | CGON | ✓ | cross-trial-comparison.md |
| 3 | ALMS | ✓ | short-thesis-validation.md |
| 4 | TERN/ELVN | ✓ | endpoint-manipulation.md |
| 5 | APGE | ✓ | pk-pd-exposure-response.md |
| 6 | RVMD | ✓ | m-and-a-playbook.md |
| 7 | OCUL | ✓ | street-expects-integration.md |
| 8 | ZEUS/GLUE | ✓ | cv-inflammation.md |
| 9 | Fintepla | ✓ | pk-pd-exposure-response.md |
| 10 | NUVB/NUVL | ✓ | oncology.md |
| 11 | GOSS | ✓ | pah-pulmonary.md |
| 12 | PGEN | ✓ | bolus-product-commercial.md |
| 13 | IRON | PARTIAL | short-thesis-validation.md |
| 14 | IMVT | PARTIAL | — |
| 15 | SLNO | ✓ | intraquarter-commercial-tracking.md |
| 16 | GKOS | ✓ | product-transition-pricing.md |
| 17 | Fintepla | ✓ | pk-pd-exposure-response.md |
| 18 | KPTI | ✓ | ta-hematology-mf.md |
| 19 | CNST | ✓ | ta-hematology-mf.md |
| 20 | AVTX | ✓ | ta-hidradenitis-suppurativa.md |

---

## Why This Matters

Each case study represents hours of analytical work. The patterns extracted are:
- Generalizable across tickers
- Derived from real institutional debates
- Quantified with specific adjustments

**Losing them means re-doing the work. This protocol prevents that.**

---

## Self-Validation Script

Run this to verify system integrity:

```bash
echo "=== BIOTECH SKILLS INTEGRITY CHECK ===" 
echo ""

# Count files
total=$(find /mnt/skills/user -name "*.md" ! -path "*/autonomous-integration/*" | wc -l)
echo "Total files: $total"
echo ""

# List by directory
for skill in biotech-coordinator reverend-bayes john-snow graham keynes simons; do
  count=$(find /mnt/skills/user/$skill -name "*.md" 2>/dev/null | wc -l)
  echo "  $skill: $count files"
done
echo ""

# Check key files exist
echo "Key files:"
for f in PATTERN_TRACKING.md PERSISTENCE.md skill-iteration-guide.md 5pter-template.md; do
  if [ -f "/mnt/skills/user/biotech-coordinator/references/$f" ]; then
    echo "  ✓ $f"
  else
    echo "  ✗ $f MISSING"
  fi
done
```
