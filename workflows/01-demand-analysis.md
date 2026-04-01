# 📂 01 — Demand Analysis Workflow

**Business function:** Operations 

**Trigger:** Weekly sales data generated from POS system

**Prompts in this section:** P01, P02, P03

---

## Section Purpose

These prompts automate the analysis of sales data to identify trends, forecast demand, and detect patterns. In retail environments with high product turnover, demand analysis is a repetitive and time-sensitive task. This prompt chain reduces manual analysis time from ~1–2 hours per store to under 10 minutes, while improving consistency and decision accuracy.

---

## Chain Diagram

```
Weekly sales data generated
        │
        ▼
   P01 · Sales trend summary        (Weekly — identifies key trends)
        │
        ▼
   P02 · Demand forecast            (Weekly — predicts next 7 days demand)
        │
        ▼
   P03 · Seasonality detection      (Periodic — identifies recurring patterns)
```

---

## Human-in-the-Loop Points

| Step       | Human action required                          |
| ---------- | ---------------------------------------------- |
| P01 output | Store manager reviews insights                 |
| P02 output | Inventory planner validates forecast           |
| P03 output | Analyst confirms patterns before strategic use |

---

## Prompts

| File                         | Prompt                | Status          |
| ---------------------------- | --------------------- | --------------- |
| P01-sales-trend-summary.md   | Sales trend summary   | ✅ Tested — v1.2 |
| P02-demand-forecast.md       | Demand forecast       | ✅ Tested — v1.2 |
| P03-seasonality-detection.md | Seasonality detection | ✅ Tested — v1.2 |

