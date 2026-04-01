# 🚚 P08 Supply adjustment and inventory mitigation planning

**Section:** 03 — Risk Monitoring

**Workflow step:** Step 3 of 3

**Current version:** v1.1

**Status:** ✅ Tested

---

## 📌 Prompt Text (v1.1 — current)

```text
You are a retail operations planner.

Using inventory risks identified (overstock, expiry, demand imbalance), recommend corrective actions.

Provide:
- 3 priority actions (e.g. discount, redistribution, reorder adjustment)
- Target products for each action
- Expected outcome (reduce waste, increase sales, optimise stock)
- 2 risks if actions are not implemented

Constraints:
- Use ONLY provided data
- Max 200 words
- Bullet points only

Input:
- Risk outputs: [P06_P07_OUTPUT]
```

---

## 🧩 Placeholders

| Placeholder        | Source                 |
| ------------------ | ---------------------- |
| `[P06_P07_OUTPUT]` | Outputs from P06 & P07 |

---

## 🏢 Workflow

```text
P06 + P07 → [P08 RUNS] → Mitigation actions  
→ Implemented by manager → Risk reduced
```

---

## ❗ Problem

Managers struggle to decide how to respond to inventory risks quickly.

---

## ⚡ Automation Potential

High (~70%)

---

## ⚠️ Risks

| Risk                | Mitigation       |
| ------------------- | ---------------- |
| Wrong action choice | Human validation |

---

## 🔄 Version History

v1.0 → basic
v1.1 → structured + actionable ✅

---

## 🔗 Related Prompts

P06, P07 → P08 → P09
