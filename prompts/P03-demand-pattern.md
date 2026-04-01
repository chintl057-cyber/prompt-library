# 📊 P03 Seasonality and demand pattern detection

Section: 01 — Demand Analysis

Workflow step: Step 3 of 3

Current version: v1.2

**Status:** ✅ Tested

---

## 📌 Prompt Text (v1.2 — current)

```text
You are a retail demand analysis specialist at a supermarket chain.

Analyse the following historical sales data across multiple weeks.

Identify:
- Any seasonal patterns (e.g. weekend spikes, monthly cycles)
- Recurring demand trends for key products
- Products with unstable or unpredictable demand
- 2 insights to improve inventory planning
- 2 risks if patterns are ignored

Context:
The goal is to detect demand patterns over time to improve forecasting and stock planning.

Constraints:
- Use ONLY the data provided
- Do NOT assume external factors (e.g. weather, promotions)
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Historical sales data:
[HISTORICAL_DATA]
```

---

## 🧩 Placeholders to fill

| Placeholder         | Source                       | Example                                         |
| ------------------- | ---------------------------- | ----------------------------------------------- |
| `[HISTORICAL_DATA]` | Multi-week POS sales records | "Week 1: Milk 500, Week 2: 550, Week 3: 600..." |

---

## 🏢 Intended Workflow or Task

* Trigger: Completion of P02 (Demand forecast)
* Actor: Inventory planner / analyst
* Timing: Runs after forecast to validate long-term patterns
* Next step: Insights used to refine forecasting and stocking strategy

```text
Historical data → [P03 RUNS] → Pattern insights identified  
→ Supports forecasting accuracy → Improves inventory planning
```

---

## ❗ Problem Being Solved

Retail demand is often influenced by recurring patterns (weekly, seasonal), but these are not always clearly identified.

* Managers rely on short-term data without understanding trends
* Seasonal demand spikes are missed
* Inventory planning becomes reactive instead of proactive

This leads to:

* Frequent stockouts during peak demand
* Overstock during low-demand periods
* Inefficient inventory allocation

**Pain points addressed:**

* Lack of visibility into demand patterns
* Reactive decision-making
* Poor long-term planning

---

## ⚡ Automation Potential

Level: Medium–High

| Dimension               | Assessment                                   |
| ----------------------- | -------------------------------------------- |
| Repetitiveness          | Medium — periodic analysis required          |
| Data availability       | High — historical data stored in POS systems |
| Human judgment needed   | Medium — patterns require validation         |
| Integration possibility | High — feeds into forecasting models         |
| Estimated time saving   | ~60–70% reduction                            |

Human-in-the-loop role:
Analysts validate detected patterns before applying strategic changes.

---

## ⚠️ Risks and Limitations

| Risk                               | Level  | Mitigation                                |
| ---------------------------------- | ------ | ----------------------------------------- |
| Misinterpretation of patterns      | Medium | Human validation of outputs               |
| Ignoring external factors          | High   | Combine with business context when needed |
| Poor data quality affects accuracy | High   | Ensure clean historical data              |
| Overgeneralisation of trends       | Medium | Limit conclusions to data provided        |

**Overall risk rating:** MEDIUM — suitable for decision support with oversight.

---

## 🔄 Version History

### v1.0 — Initial draft

Prompt: Analyse sales patterns.
Output: Vague insights with no actionable value
Observed effect: Not useful for planning
Lesson learned: Need specific outputs and structure

---

### v1.1 — Added pattern detection focus

Change: Added seasonal patterns and product trends
Output: More relevant but inconsistent
Observed effect: Difficult to standardise outputs
Lesson learned: Need constraints and formatting

---

### v1.2 — Structured + constrained output ✅ Current

Change: Added:

* explicit outputs (patterns, risks, insights)
* bullet format
* word limit
* grounding constraint

Output: Clear and consistent pattern insights
Observed effect: Improved planning reliability
Lesson learned: Structured prompts improve consistency and usefulness

---

## 🔗 Related Prompts

* Previous in chain: P02 — Demand forecast
* Next in chain: P05 — Reorder recommendation
* Parent section: 01 — Demand Analysis

---
