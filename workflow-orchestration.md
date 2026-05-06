# Workflow Orchestration Map

## 13-Department Sequential Pipeline

```
USER TRIGGER: "Run full workflow"
          │
          ▼
┌──────────────────────────────────────┐
│  DEPT 01 — Marketing Research Team  │
│  Output: 10 viral content ideas     │
└──────────────────┬───────────────────┘
                   │ 10 ideas
                   ▼
┌──────────────────────────────────────┐
│  DEPT 02 — Trend Analysis Team      │
│  Output: Ranked table + top 3       │
└──────────────────┬───────────────────┘
                   │ top 3 ranked ideas
                   ▼
┌──────────────────────────────────────┐
│  DEPT 03 — Content Strategy Team    │
│  Output: 3 strategy briefs          │
└──────────────────┬───────────────────┘
                   │ 3 briefs
                   ▼
┌──────────────────────────────────────┐
│  DEPT 04 — Idea Shortlisting Team   │
│  Output: 1 approved idea + angle    │
└──────────────────┬───────────────────┘
                   │ approved idea + angle
                   ▼
┌──────────────────────────────────────┐
│  DEPT 05 — Script Writing Team      │
│  Output: Full 5-part reel script    │
└──────────────────┬───────────────────┘
                   │ full script
                   ▼
┌──────────────────────────────────────┐
│  DEPT 06 — Hook Specialist          │
│  Output: Optimized 3-second hook    │
└──────────────────┬───────────────────┘
                   │ final hook + script
                   ▼
┌──────────────────────────────────────┐
│  DEPT 07 — Copy Team                │
│  Output: Gen Z-refined full script  │
└──────────────────┬───────────────────┘
                   │ refined script
                   ▼
┌──────────────────────────────────────┐
│  DEPT 08 — Packaging Team           │
│  Output: Thumbnail + visual brief   │
└──────────────────┬───────────────────┘
                   │ packaging brief
                   ▼
┌──────────────────────────────────────┐
│  DEPT 09 — SEO Team                 │
│  Output: Hashtags + keywords        │
└──────────────────┬───────────────────┘
                   │ SEO package
                   ▼
┌──────────────────────────────────────┐
│  DEPT 10 — Publishing Team          │
│  Output: Posting playbook           │
└──────────────────┬───────────────────┘
                   │ all outputs 01–10
                   ▼
┌──────────────────────────────────────┐
│  DEPT 11 — Performance Team         │
│  Output: 3-scenario prediction      │
└──────────────────┬───────────────────┘
                   │ all outputs 01–11
                   ▼
┌──────────────────────────────────────┐
│  DEPT 12 — Feedback Team            │
│  Output: Virality score + fixes     │
└──────────────────┬───────────────────┘
                   │ all outputs 01–12
                   ▼
┌──────────────────────────────────────┐
│  DEPT 13 — Operations Team          │
│  Output: CEO Final Report           │
└──────────────────┬───────────────────┘
                   │
                   ▼
            CEO APPROVAL
```

---

## Data Flow Table

| Dept | Name | Receives From | Key Input | Passes To | Key Output |
|------|------|--------------|-----------|-----------|-----------|
| 01 | Marketing Research | User trigger | Niche + audience config | 02 | 10 viral ideas |
| 02 | Trend Analysis | 01 | 10 ideas | 03 | Ranked table + top 3 |
| 03 | Content Strategy | 02 | Top 3 ranked ideas | 04 | 3 strategy briefs |
| 04 | Idea Shortlisting | 03 | 3 briefs | 05, 08 | 1 approved idea + angle |
| 05 | Script Writing | 04 | Approved idea + angle | 06 | Full 5-part script |
| 06 | Hook Specialist | 05 | Full script (Hook section) | 07 | Optimized final hook |
| 07 | Copy Team | 05 + 06 | Script + final hook | 08, 09 | Gen Z-refined script |
| 08 | Packaging | 04 + 07 | Angle + refined script | 09, 13 | Packaging brief |
| 09 | SEO | 04 + 07 + 08 | Idea + script + caption | 10, 13 | SEO package |
| 10 | Publishing | 04 + 09 | Idea + SEO package | 11, 13 | Publishing playbook |
| 11 | Performance | 01–10 | All prior outputs | 12, 13 | Performance predictions |
| 12 | Feedback | 01–11 | All prior outputs | 13 | Feedback report + score |
| 13 | Operations | 01–12 | All prior outputs | CEO | Final CEO report |

---

## Inter-Department Handoff Protocol

Each department output begins with:

```
═══════════════════════════════════════════════
DEPARTMENT [NN] — [DEPARTMENT NAME]
Status: COMPLETE
Passing output to: Dept [NN+1]
═══════════════════════════════════════════════
```

And ends with:

```
───────────────────────────────────────────────
DEPT [NN] OUTPUT COMPLETE
Key deliverable: [one-line summary]
→ HANDOFF TO DEPT [NN+1]
───────────────────────────────────────────────
```

---

## Running Modes

| Mode | How | Best For |
|------|-----|---------|
| **A — Full Auto** | Paste `system-prompt.md` as AI system prompt. Send "Run full workflow." | Fastest, single-session output |
| **B — Step-by-Step** | Run each `departments/NN-*/prompt.md` individually. Paste prior output at top. | Review and edit between steps |
| **C — Mid-Point Restart** | Paste Depts 01–N outputs into Dept N+1's prompt as context. | Fix specific department outputs |

---

## Niche Reference

All departments should operate within these niche categories:

| Category | Examples |
|----------|---------|
| Personal Finance | Saving, budgeting, debt, emergency funds |
| AI with Finance | AI tools for investing, budgeting apps, robo-advisors |
| AI for Business & Finance | AI for accounting, invoicing, financial analysis |
| Taxation | Tax hacks, deductions, corporate vs. personal tax |
| Business | Starting a business, LLPs, side hustles, profit structures |
| Business Politics | Policy changes affecting small business and startups |
| Financial Literacy | Concepts school never taught — compound interest, credit, net worth |
| Corporate Laws | Legal structures, shareholder rights, corporate loopholes |

---

## Gen Z Platform Behavior Notes

| Platform | Gen Z Behavior | Content Implication |
|----------|---------------|---------------------|
| Instagram Reels | Saves > Likes | Create "save-worthy" content — actionable, reference-able |
| TikTok | Comments drive algorithm | End with a question that demands a reply |
| YouTube Shorts | Watch time % is king | Re-hook at 30 seconds is critical to prevent drop-off |
| LinkedIn | Shares from Gen Z professionals | Adopt slightly more professional tone, same raw truth |
