# finance-portfolio

# Dennis John — FP&A & Financial Control Portfolio

Analyst-grade finance work: auditable models, validated forecasts, and
documented decisions. AI used as a review layer — not a shortcut.

**ESSEC Grande École MiM** · **CIMA Management Level** · **CFI certified FP&A Professional**

---

## What this portfolio demonstrates

- **Auditable modeling** — every number traces to centralized assumption
  sheets; no hardcodes, no orphan overrides.
- **Validated analysis** — forecasts and risk scores tested out-of-sample
  (AUC, lift, calibration), not just fitted.
- **Documented judgment** — every cleaning choice, threshold, and assumption
  logged with its rationale.
- **AI with an audit trail** — structured prompting, human review at each
  step, and a prompt log of what was used and what was rejected.

---

## Projects

### ✅ Financial Model Audit — SaaS P&L
**Status: Complete**

Audited a 37-month SaaS P&L model to controller standard. Found 9 hidden
constants across 260 cells, fixed tax and cash-flow logic, and rebuilt
every P&L column as a formula linked to a single assumption sheet.

**Result: 260 → 0 hardcoded cells. Model now re-forecasts from one input.**

`Excel` · `Claude` · `Named ranges` · `Audit log` · `Tolerance-based matching`
[→ Case study](./01-Constants-audit)

---

### 🚧 Customer Risk Analysis — B2B SaaS
**Status: In progress · Expected [Nov 2026]**

Three-construct risk engine (churn / payment default / spend reduction) built
on a multi-table star schema with WOE scorecards, out-of-sample validation,
and an executive dashboard. Designed for a real FP&A workflow: each risk
dimension answered by a separate model, with a documented prompt trail.

`Python` · `Power Query` · `Excel` · `Logistic regression` · `WOE scorecard`

---

### 🚧 Revenue Seasonality Analysis
**Status: In progress · Expected [Dec 2026]**


---

### 🚧 Three-Statement Model — SaaS (Duolingo)
**Status: Planned · Expected [Dec 2026]**

Driver-based 3-statement model + Forecast on a live SaaS company, with scenario
toggle, balance/cash tie-checks, and headcount proration. Built the way an
FP&A team builds: assumptions centralized, formulas end-to-end, audit-ready.

`Excel` · `Financial Modeling` · `Financial Forecasting` · `Scenario analysis` · `Tie-checks`

---

## About the approach

Every project in this portfolio follows the same discipline: **specify the
problem clearly, generate or source data honestly, validate out-of-sample,
and document every decision.** AI accelerates the build — it drafts code,
proposes structures, and critiques methodology — but it never makes the final
call on thresholds, variable selection, or the business narrative. Those
decisions are mine, logged, and defensible.

---

## Contact

📧 dennis.john@essec.edu
💼 [linkedin.com/in/dennisjhn](https://linkedin.com/in/dennisjhn)