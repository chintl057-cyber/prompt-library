# 📂 03 — Risk Monitoring Workflow

**Business function:** Retail Operations — Risk & Loss Prevention

**Trigger:** Inventory and forecast data available

**Prompts in this section:** P06, P07, P08

---

## Section Purpose

These prompts identify and mitigate key inventory risks, including overstocking, product expiry, and imbalance between supply and demand. In retail, unmanaged risks lead to financial loss, waste, and inefficiency. This workflow enables proactive risk detection and reduces operational losses.

---

## Chain Diagram

```
Inventory + forecast data available
        │
        ▼
   P06 · Overstock detection        (Weekly — identifies excess stock)
        │
        ▼
   P07 · Expiry risk analysis       (Daily — detects perishable risks)
        │
        ▼
   P08 · Mitigation planning        (Triggered — recommends actions)
```

---

## Human-in-the-Loop Points

| Step       | Human action required                          |
| ---------- | ---------------------------------------------- |
| P06 output | Inventory manager validates overstock risks    |
| P07 output | Store manager confirms expiry actions          |
| P08 output | Operations manager approves mitigation actions |

---

## Prompts

| File                        | Prompt               | Status          |
| --------------------------- | -------------------- | --------------- |
| P06-overstock-detection.md  | Overstock detection  | ✅ Tested — v1.1 |
| P07-expiry-risk-analysis.md | Expiry risk analysis | ✅ Tested — v1.1 |
| P08-supply-delay-impact.md  | Mitigation planning  | ✅ Tested — v1.1 |

