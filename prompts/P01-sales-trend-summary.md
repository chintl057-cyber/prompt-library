📊 P01. Sales trend summary and insights

Section: 01 — Demand Analysis

Workflow step: Step 1 of 3

Current version: v1.2

Status: ✅ Tested

---

 📌 Prompt Text (v1.2 — current)

```
You are a retail inventory analyst at a supermarket chain.

Analyse the following weekly sales data.

Provide:
- Top 3 best-selling products (by sales volume)
- Top 3 declining products (largest decrease vs previous period)
- Any notable patterns (seasonal trends, demand shifts)
- 2 key insights for inventory planning
- 2 risks if current trends continue

Context:
The goal is to support inventory planning decisions using recent sales performance.

Constraints:
- Use ONLY the data provided
- Do NOT assume or generate missing data
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Sales data:
[SALES_DATA]
```

---

**Placeholders to fill:**

| Placeholder    | Source                  | Example                                               |
| -------------- | ----------------------- | ----------------------------------------------------- |
| `[SALES_DATA]` | Weekly POS sales report | "Milk: 500 (+10%), Bread: 300 (-5%), Eggs: 450 (+2%)" |

---

## 🏢 Intended Workflow or Task

* Trigger: Weekly sales data generated from POS system
* Actor: Store manager / inventory planner reviews output
* Timing: Runs at end of each week before inventory planning
* Next step: P02 (Demand forecast) uses this output

```
Sales data generated → [P01 RUNS] → Trend insights produced  
→ Used for demand forecasting → Inventory decisions made
```

---

## ❗ Problem Being Solved

Store managers manually analyse sales reports to identify trends and patterns.

This process:

* Takes approximately 1–2 hours per week per store
* Produces inconsistent insights depending on manager experience
* Delays inventory planning decisions

At scale across multiple stores, this leads to **inefficient operations and missed sales opportunities**.

**Pain points addressed:**

* Manual data analysis is time-consuming
* Inconsistent interpretation of trends
* Delayed decision-making

---

## ⚡ Automation Potential

Level: High

| Dimension               | Assessment                                    |
| ----------------------- | --------------------------------------------- |
| Repetitiveness          | High — performed weekly across all stores     |
| Data availability       | High — Sales data always available        |
| Human judgment needed   | Medium — validation required before decisions |
| Integration possibility | High — integrates with inventory systems      |
| Estimated time saving   | ~70–80% — from 1–2 hours to minutes           |

Human-in-the-loop role:
Human review AI-generated insights before applying inventory decisions.

---

## ⚠️ Risks and Limitations

| Risk                                           | Level  | Mitigation                                          |
| ---------------------------------------------- | ------ | --------------------------------------------------- |
| Model identifies trends not supported by data  | Medium | Add grounding constraint (“use only provided data”) |
| Poor input data quality affects output         | High   | Validate data before use                        |
| Oversimplified insights miss important context | Medium | Combine with human review                           |
| Over-reliance on AI recommendations            | Medium | Use as decision support, not replacement            |

Overall risk rating: MEDIUM — suitable for decision support with human validation.

---

## 🔄 Version History

### v1.0 — Initial draft

Prompt: Upload this dataset. Summarise sales data.
Output: Generic summary with little business value
Observed effect:Managers still needed to manually analyse data
Lesson learned:Need structured outputs and clear objectives

---

### v1.1 — Added role and structure

Change: Added analyst role and required outputs (top products, trends)
Output: More relevant but inconsistent format
Observed effect: Difficult to compare outputs across weeks
Lesson learned: Need consistent formatting constraints

---

### v1.2 — Structured + constrained output ✅ Current

Change: Added:

* bullet point output
* word limit
* explicit required outputs
* grounding constraint

Output: Clear, consistent, and actionable insights
Observed effect: Reliable outputs for weekly reporting and planning
Lesson learned: Structured prompts with constraints improve consistency and usability

---

## 🔗 Related Prompts

* Previous in chain: None (starting point)
* Next in chain P02 — demand - forecast
* **Parent section:** 01 — Demand Analysis

---

