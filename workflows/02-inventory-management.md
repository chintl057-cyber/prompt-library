# 📂 02 — Inventory Management Workflow

**Business function:** Operations — Inventory Control

**Trigger:** Inventory and sales data updated in ERP system

**Prompts in this section:** P04, P05

---

## Section Purpose

These prompts automate stock monitoring and reorder decision-making. Inventory management is a high-frequency operational task where delays or inaccuracies can lead to stockouts or overstocking. This prompt chain enables proactive stock control and reduces decision time from ~30 minutes to under 5 minutes per cycle.

---

## Chain Diagram

```
Inventory + sales data updated
        │
        ▼
   P04 · Low stock alert            (Daily — detects stockout risks)
        │
        ▼
   P05 · Reorder recommendation     (Triggered — generates reorder plan)
```

---

## Human-in-the-Loop Points

| Step       | Human action required                    |
| ---------- | ---------------------------------------- |
| P04 output | Inventory controller reviews alerts      |
| P05 output | Store manager approves reorder decisions |

---

## Prompts

| File                          | Prompt                 | Status          |
| ----------------------------- | ---------------------- | --------------- |
| P04-low-stock-alert.md        | Low stock alert        | ✅ Tested — v1.2 |
| P05-reorder-recommendation.md | Reorder recommendation | ✅ Tested — v1.2 |

