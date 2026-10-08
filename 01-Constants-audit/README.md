# Financial Model Audit — SaaS P&L

**Found 9 hidden assumptions across 218 cells, fixed 3 formula errors, and rebuilt the model so every number traces back to one centralized assumption sheet.**

---

## What This Is

A 37-month SaaS P&L model that had accumulated the usual mess: hardcoded numbers buried in formulas, assumptions declared but not used, manual overrides nobody remembered, and a cash flow calculation that didn't reconcile.

I ran a structured audit to find every hidden constant, corrected the errors, and rebuilt the model so that changing **one assumption** — say, COGS from 32% to 35% — flows correctly through the entire P&L and cash balance.

---

## Why It Matters

Most models look fine until someone asks: *"What happens to our runway if COGS goes up 3 points?"*

If the answer requires hunting through 218 cells to find what breaks, the model isn't a model — it's a spreadsheet. This project is about closing that gap.

---

## What I Found

| Finding | Impact |
|---|---|
| **9 hardcoded constants** across 260 cells (50% of the P&L) | Model couldn't be re-forecast without manual edits |
| **6 of 9 constants were missing** from the assumptions sheet entirely | No single source of truth |
| **Tax applied inconsistently** — only 7 of 37 rows matched the stated 25% rate | 5,455 error in total tax |
| **4 unexplained manual opex adjustments** left in the model | 310 overstated opex |
| **Cash flow omitted the depreciation add-back** | Understated cash by 1,500/month, 55,500 cumulative |

---

## What I Fixed

- Centralized all assumptions into a single sheet with named ranges
- Rebuilt every P&L column as a formula linked to those assumptions
- Corrected the tax, opex, net income, and cash flow logic
- Documented every change with before/after values in an audit log

**Result:**Hardcoded P&L cells went from **260 to 0**.

---

## Skills Demonstrated

**Model audit** — Constants detection, reverse-engineering formulas from static values, tolerance-based matching, identifying outliers

**Excel best practice** — Named ranges, assumption centralization, audit trails, change logging

**AI-assisted workflow** — Structured prompting with human review and validation at each step

---

## Files

| File | What's Inside |
|---|---|
| `Model Audit v0/` | The pre-audit model — assumptions and 37-month P&L |
| `Model Audit v1` | Final Model including audit table, change log, and pre-fix snapshot |
| `Prompt/` | The exact prompts used to run the audit |

---

## Tools

Excel · Claude (Opus 5.5) · CSV

*All data is synthetic. No client or proprietary information is included.*

---

**[Your Name]** · [LinkedIn] · [GitHub] · [Email]
