# Department Output Handoff Template

## Purpose

Every department output must begin and end with these standard blocks. This ensures clean parsing when running departments individually (Mode B) and makes it easy to extract each department's key deliverable.

---

## Header Block (start of every department output)

```
═══════════════════════════════════════════════
DEPARTMENT [NN] — [DEPARTMENT NAME]
Status: IN PROGRESS
Timestamp: [YYYY-MM-DD HH:MM]
Input received from: Dept [NN-1] — [Dept Name]
Passing output to: Dept [NN+1] — [Dept Name]
═══════════════════════════════════════════════
```

---

## Output Body

[Department completes its full output here, following its prompt.md structure]

---

## Footer Block (end of every department output)

```
───────────────────────────────────────────────
DEPT [NN] OUTPUT COMPLETE
Status: COMPLETE
Key deliverable: [One-line summary of the main output]
→ HANDOFF TO DEPT [NN+1] — [DEPARTMENT NAME]
───────────────────────────────────────────────
```

---

## Full Example (Department 02)

```
═══════════════════════════════════════════════
DEPARTMENT 02 — TREND ANALYSIS TEAM
Status: IN PROGRESS
Timestamp: 2026-05-06 19:30
Input received from: Dept 01 — Marketing Research Team
Passing output to: Dept 03 — Content Strategy Team
═══════════════════════════════════════════════

[Full ranked table of 10 ideas with scores]
[Top 3 highlighted with rationale]

───────────────────────────────────────────────
DEPT 02 OUTPUT COMPLETE
Status: COMPLETE
Key deliverable: All 10 ideas ranked; Top 3 identified for Content Strategy
→ HANDOFF TO DEPT 03 — CONTENT STRATEGY TEAM
───────────────────────────────────────────────
```

---

## Department Quick Reference

| Dept | Name | Receives From | Passes To |
|------|------|--------------|-----------|
| 01 | Marketing Research | User | 02 |
| 02 | Trend Analysis | 01 | 03 |
| 03 | Content Strategy | 02 | 04 |
| 04 | Idea Shortlisting | 03 | 05, 08 |
| 05 | Script Writing | 04 | 06 |
| 06 | Hook Specialist | 05 | 07 |
| 07 | Copy Team | 05, 06 | 08, 09 |
| 08 | Packaging | 04, 07 | 09, 13 |
| 09 | SEO | 04, 07, 08 | 10, 13 |
| 10 | Publishing | 04, 09 | 11, 13 |
| 11 | Performance | 01–10 | 12, 13 |
| 12 | Feedback | 01–11 | 13 |
| 13 | Operations | 01–12 | CEO |
