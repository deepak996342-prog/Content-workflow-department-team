# Content-Workflow-Department-Team

## 13-Department AI Content Creation System
### Niche: Personal Finance | AI & Finance | Business | Taxation | Financial Literacy | Corporate Law
### Target Audience: Gen Z (18–27)

---

## What This Is

A file-based AI workflow system that simulates a real 13-department content creation company. Each department runs sequentially — every team's output becomes the next team's input — producing a final CEO-ready report with a complete piece of viral Gen Z content.

---

## How to Use

### Option A — Full Auto (Recommended)
1. Open `system-prompt.md`
2. Paste it as the system prompt in your AI tool (Claude, GPT-4, etc.)
3. Send the trigger message: `Run full workflow`
4. The AI runs all 13 departments in sequence and outputs the complete CEO report

### Option B — Step-by-Step (Manual Control)
1. Open `departments/01-marketing-research/prompt.md`
2. Run it in your AI tool
3. Copy the output and paste it at the top of `departments/02-trend-analysis/prompt.md`
4. Continue through all 13 departments in order
5. Review and edit between each step as needed

### Option C — Mid-Point Restart
If you want to re-run from a specific department, paste all prior outputs as context into that department's `prompt.md` and continue from there.

---

## File Structure

| Path | Purpose |
|------|---------|
| `config.json` | Single source of truth — niche, audience, platform, tone |
| `system-prompt.md` | Master AI prompt — runs full 13-step pipeline in one session |
| `workflow-orchestration.md` | Visual pipeline map + data flow table |
| `departments/NN-*/role.md` | Each department's role, inputs, outputs, and quality standards |
| `departments/NN-*/prompt.md` | AI-ready prompt for each department |
| `departments/06-hook-specialist/genz-hook-guide.md` | Gen Z hook formulas, rules, and scoring |
| `departments/07-copy-team/genz-copy-guide.md` | Gen Z copy rules, vocab swaps, and CTA guide |
| `templates/ceo-report.md` | Final CEO approval report template (9 sections) |
| `templates/department-output.md` | Standard inter-department handoff format |
| `templates/workflow-run.md` | Session run log and checklist |
| `outputs/` | Save completed CEO reports here |

---

## The 13-Department Pipeline

```
01 Marketing Research  →  10 viral ideas discovered
02 Trend Analysis      →  Ideas ranked by virality, relatability, hook strength
03 Content Strategy    →  Top 3 ideas with angles + emotional triggers
04 Idea Shortlisting   →  1 winning idea selected
05 Script Writing      →  Full 5-part reel script (Hook→Build→Re-hook→Climax→CTA)
06 Hook Specialist     →  First 3 seconds optimized for Gen Z scroll-stopping
07 Copy Team           →  Full script refined to Gen Z voice
08 Packaging Team      →  Thumbnail + title + opening visual + text overlays
09 SEO Team            →  Hashtags + keywords + caption strategy
10 Publishing Team     →  Best posting times + cross-platform strategy + series plan
11 Performance Team    →  3-scenario engagement prediction
12 Feedback Team       →  Virality score + top 3 weaknesses + specific fixes
13 Operations Team     →  Final CEO approval report
```

---

## Gen Z Content Rules (Quick Reference)

- No corporate-speak. Ever. If it sounds like LinkedIn, rewrite it.
- Financial content must feel like advice from a cool older sibling, not a bank.
- Hook must stop the scroll in under 1.5 seconds.
- Short sentences. Punchy verbs. Slang only when it fits naturally.
- Dollar figures beat percentages. Specificity beats generality.
- The last line before the CTA must land like a gut punch.

---

## Output Naming Convention

```
outputs/YYYY-MM-DD-[idea-slug]-report.md
```

Example: `outputs/2026-05-06-zero-tax-on-12-lpa-report.md`

---

## Updating the Niche or Audience

Edit `config.json` only. All department prompts reference the config, so one change propagates through the entire system.
