# Biotech Skills Workflow

How to use and update the biotech skills framework with Claude Desktop and GitHub.

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                    SOURCE OF TRUTH: GitHub                       │
│         github.com/issender-byte/biotech-skills                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                 LOCAL WORKING COPY                               │
│   C:\Users\IlanSender\OneDrive - Braidwell\Desktop\biotech-skills│
│                                                                  │
│   Claude Desktop connects via MCP servers:                       │
│   • biotech-skills-files (read/write files)                     │
│   • biotech-skills-git (status, diff, add, commit)              │
└─────────────────────────────────────────────────────────────────┘
```

---

## Daily Workflow

### 1. Investment Case Analysis Session (Claude Desktop)

Start a new conversation and analyze the case:

```
You: "Analyze this ACME thesis: [paste content]"

Claude: [Uses skills to analyze, routes through reverend-bayes → john-snow → graham → keynes]
```

### 2. Pattern Extraction (Claude Desktop)

When new patterns emerge during analysis:

```
You: "Add the pattern we identified about [X] to the appropriate skill file"

Claude: [Reads current file] → [Updates with new pattern] → [Shows you the change]
```

### 3. Commit Changes (Claude Desktop)

After updating skill files:

```
You: "Commit the changes with message 'Add [pattern] from [TICKER] analysis'"

Claude: [git add] → [git commit] → "Committed with hash abc123"
```

### 4. Push to GitHub (Manual Step)

Double-click the batch file on your Desktop:

```
📄 push-biotech-skills.bat
```

Or run in terminal:
```
cd "C:\Users\IlanSender\OneDrive - Braidwell\Desktop\biotech-skills"
git push origin main
```

---

## Available Commands in Claude Desktop

### File Operations (biotech-skills-files MCP)

| Command | Example |
|---------|---------|
| List files | "List all files in the skills directory" |
| Read file | "Read the reverend-bayes SKILL.md" |
| Write file | "Update PATTERN_TRACKING.md with..." |
| Edit file | "Add this pattern to analytical-rules.md" |

### Git Operations (biotech-skills-git MCP)

| Command | Example |
|---------|---------|
| Status | "What's the git status?" |
| Diff | "Show me what changed" |
| Stage | "Stage the modified files" |
| Commit | "Commit with message 'Add X pattern'" |
| Log | "Show recent commits" |
| Branch | "What branch am I on?" |

**Note:** `git push` is not available via MCP. Use the batch file or terminal.

---

## Session Protocols

### Starting a New Session

Claude Desktop should:
1. Read `PATTERN_TRACKING.md` first (per existing protocol)
2. Verify file count matches expected
3. Route analysis requests through appropriate skills

### Ending a Session with Updates

Before ending:
1. Verify all pattern updates are in files
2. Update `PATTERN_TRACKING.md` with:
   - Source Conversation Index entry
   - Pattern Catalog entry (correct skill section)
3. Commit all changes
4. Push to GitHub (batch file or terminal)

---

## File Structure

```
biotech-skills/
├── WORKFLOW.md                    ← This file
├── .gitignore
├── push-biotech-skills.bat        ← On Desktop, not in repo
│
├── biotech-coordinator/
│   ├── SKILL.md                   ← Orchestration rules
│   └── references/
│       ├── PATTERN_TRACKING.md    ← Master pattern index
│       ├── PERSISTENCE.md         ← Recovery protocols
│       ├── 5pter-template.md      ← Output format
│       ├── skill-iteration-guide.md
│       ├── team-roster.md
│       └── ...
│
├── reverend-bayes/                ← Clinical/statistical
│   ├── SKILL.md
│   └── references/
│
├── john-snow/                     ← Commercial
│   ├── SKILL.md
│   └── references/
│
├── graham/                        ← Valuation
│   ├── SKILL.md
│   └── references/
│
├── keynes/                        ← Position/sentiment
│   ├── SKILL.md
│   └── references/
│
└── simons/                        ← Portfolio/risk
    ├── SKILL.md
    └── references/
```

---

## Troubleshooting

### MCP servers not connecting

1. Check Claude Desktop Settings → Developer → Local MCP servers
2. Both servers should show "running"
3. If not, restart Claude Desktop

### Config file location

```
C:\Users\IlanSender\AppData\Roaming\Claude\claude_desktop_config.json
```

### MCP logs

```
C:\Users\IlanSender\AppData\Roaming\Claude\logs\mcp.log
C:\Users\IlanSender\AppData\Roaming\Claude\logs\mcp-server-biotech-skills-files.log
C:\Users\IlanSender\AppData\Roaming\Claude\logs\mcp-server-biotech-skills-git.log
```

### Push fails

If `push-biotech-skills.bat` fails:
1. Check you have internet connection
2. Verify GitHub credentials are cached: `git config credential.helper`
3. Try pushing manually: `git push origin main`

---

## Quick Reference

| Task | Where | Command |
|------|-------|---------|
| Analyze case | Claude Desktop | "Analyze [ticker]" |
| Read skill | Claude Desktop | "Read [skill] SKILL.md" |
| Update skill | Claude Desktop | "Update [file] with [content]" |
| View changes | Claude Desktop | "Show git diff" |
| Commit | Claude Desktop | "Commit with message '[msg]'" |
| Push | Desktop/Terminal | Double-click `push-biotech-skills.bat` |
| Pull latest | Terminal | `git pull origin main` |

---

*Last updated: 2026-01-27*
