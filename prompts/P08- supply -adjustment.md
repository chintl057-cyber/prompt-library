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

### v1.0 — Initial draft  
**Prompt:** Suggest actions to address inventory risks.  

**Output:**  
Generated general recommendations such as “reduce stock” or “increase sales” without specifying products, priorities, or expected outcomes.  

**Observed effect:**  
- Output was too vague and not actionable  
- No clear link between identified risks and recommended actions  
- Managers still needed to manually interpret and decide next steps  

---

### v1.1 — Structured and actionable mitigation plan ✅ Current  

**Change:**  
- Added requirement for **3 priority actions**  
- Included **target products for each action**  
- Added **expected outcomes (e.g. reduce waste, increase sales)**  
- Introduced **risk awareness if actions are not taken**  
- Enforced **bullet-point structured output**  

**Output:**  
Clear, actionable mitigation plan linking inventory risks to specific operational actions and expected results.  

**Observed effect:**  
- Managers could directly apply recommendations without further interpretation  
- Faster decision-making (reduced planning time significantly)  
- Improved alignment between risk detection (P06, P07) and action  

**Lesson learned:**  
Action-oriented prompts with **explicit structure and business outcomes** significantly improve usability and operational impact.

---

## 🔗 Related Prompts

P06, P07 → P08 → P09
