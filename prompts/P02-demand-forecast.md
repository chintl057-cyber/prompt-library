# 📈 P02 Demand forecast and inventory prediction

Section: 01 — Demand Analysis

Workflow step: Step 2 of 3

Current version: v1.2
---

## 📌 Prompt Text (v1.2 — current)

```text
You are a retail demand forecasting analyst at a supermarket chain.

Using the provided sales trends and historical sales data, forecast demand for the next 7 days.

Provide:
- Forecasted demand for top 5 products (units)
- Expected increase or decrease (%) compared to current week
- 2 key factors influencing demand based on data trends
- 2 risks if the forecast is inaccurate

Context:
The goal is to support inventory planning and replenishment decisions using short-term demand predictions.

Constraints:
- Use ONLY the provided data
- Do NOT assume external factors (e.g. weather, promotions)
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Input data:
- Sales trends summary: [P01_OUTPUT]
- Historical sales data: [HISTORICAL_DATA]
```

---

## 🧩 Placeholders to fill

| Placeholder         | Source                  | Example                                      |
| ------------------- | ----------------------- | -------------------------------------------- |
| `[P01_OUTPUT]`      | Output from P01         | "Milk demand increasing, bread declining..." |
| `[HISTORICAL_DATA]` | Past 2–4 weeks POS data | "Milk: 500 → 550 → 600 units"                |

---

## 🏢 Intended Workflow or Task

* **Trigger:** Completion of P01 (Sales trend summary)
* **Actor:** Inventory planner / store manager
* **Timing:** Runs immediately after trend analysis
* **Next step:** P05 (Reorder recommendation) uses forecast output

```text
P01 output → [P02 RUNS] → Demand forecast generated  
→ Used for restocking decisions → Inventory planning executed
```

---

## ❗ Problem Being Solved

Demand forecasting in retail is often inconsistent and based on manual judgement.

* Managers rely on intuition rather than structured analysis
* Forecast accuracy varies across stores
* Poor predictions lead to stock imbalances

This results in:

* Lost sales due to stockouts
* Increased holding costs due to overstocking
* Inefficient inventory allocation

**Pain points addressed:**

* Inconsistent demand prediction
* Manual and time-consuming forecasting
* Lack of standardised forecasting approach

---

## ⚡ Automation Potential

**Level:** Medium–High

| Dimension               | Assessment                                  |
| ----------------------- | ------------------------------------------- |
| Repetitiveness          | High — performed weekly across stores       |
| Data availability       | Medium–High — depends on historical records |
| Human judgment needed   | Medium — forecasts require validation       |
| Integration possibility | High — integrates with inventory systems    |
| Estimated time saving   | ~60–70% reduction                           |

**Human-in-the-loop role:**
Managers validate forecasts before applying inventory decisions.

---

## ⚠️ Risks and Limitations

| Risk                                       | Level  | Mitigation                          |
| ------------------------------------------ | ------ | ----------------------------------- |
| Inaccurate predictions due to limited data | High   | Human validation before decisions   |
| Ignoring external demand drivers           | Medium | Add external data inputs if needed  |
| Over-reliance on AI forecasts              | Medium | Use as decision support only        |
| Poor input data quality                    | High   | Validate historical data before use |

**Overall risk rating:** MEDIUM–HIGH — requires human oversight for accuracy.

---

## 🔄 Version History

### v1.0 — Initial draft

Prompt: Predict next week sales.
Output: Vague predictions without structure
Observed effect: Not usable for business decisions
Lesson learned: Need structured outputs and clear constraints

---

### v1.1 — Added forecasting structure

Change: Added product focus and percentage change
Output: More relevant but inconsistent format
Observed effect: Difficult to compare outputs
Lesson learned: Need standardised format

---

### v1.2 — Structured + constrained forecast ✅ Current

Change: Added:

* explicit outputs (units, %, risks)
* bullet format
* word limit
* grounding constraint

Output: Clear, consistent, and actionable forecasts
Observed effect: Reliable for inventory planning
Lesson learned: Structured prompts improve forecast reliability

---

## 🔗 Related Prompts
* Previous in chain: P01 — Sales trend summary
* Next in chain: P03 — Seasonality detection / P05 — Reorder recommendation
* Parent section: 01 — Demand Analysis
---
