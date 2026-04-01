P02. Demand forecast and inventory prediction

Section: Demand Analysis
Workflow step: Step 2 of 3
Current version: v1.2
Status: Tested

---

📌 Prompt Text (v1.2 — current)

You are a retail demand forecasting analyst.

Using the provided sales trends and historical sales data, forecast demand for the next 7 days.

Provide:

* Forecasted demand for top 5 products
* Expected increase or decrease (%) compared to current week
* 2 key factors influencing demand (seasonality, trend changes)
* 2 risks if forecast is inaccurate

Use ONLY the provided data and trends. Do not assume external factors.

Input data:

* Sales trends summary: [P01_OUTPUT]
* Historical sales data: [HISTORICAL_DATA]

Output format:

* Bullet points
* Maximum 200 words
* Use clear business language

---

Placeholders to fill

| Placeholder       | Source                                 | Example                               |
| ----------------- | -------------------------------------- | ------------------------------------- |
| [P01_OUTPUT]      | Output from P01 (sales trends summary) | "Milk increasing, bread declining..." |
| [HISTORICAL_DATA] | Past 2–4 weeks sales data              | "Milk: 500 → 550 → 600 units..."      |

---

## Intended Workflow or Task

* **Trigger:** Completion of P01 (sales trend summary)
* **Integration:** Used by the inventory system for planning restocking
* **Timing:** Runs after weekly trend analysis
* **Next step:** P05 (Reorder recommendation) uses forecast output

P01 output → [P02 RUNS] → Demand forecast generated
→ Used for restocking decisions

---

Problem Being Solved

Demand forecasting is often done manually or using basic assumptions.

* Inaccurate forecasts lead to **stockouts or overstocking**
* Managers rely on intuition instead of data
* Inconsistent forecasting across stores

This results in:

* Lost revenue (out-of-stock items)
* Increased costs (excess inventory)

---

⚡ Automation Potential

Level: Medium–High

| Dimension               | Assessment                          |
| ----------------------- | ----------------------------------- |
| Repetitiveness          | High — forecasting done weekly      |
| Data availability       | Medium — depends on data quality    |
| Human judgment needed   | Medium — forecasts need validation  |
| Integration possibility | High — feeds into inventory systems |
| Estimated time saving   | ~60–70% reduction                   |

**Human-in-the-loop role:**
Managers validate forecasts before applying inventory decisions.

---

⚠️ Risks and Limitations

| Risk                                           | Level  | Mitigation                               |
| ---------------------------------------------- | ------ | ---------------------------------------- |
| Inaccurate predictions                         | High   | Human validation before action           |
| Missing external factors (weather, promotions) | Medium | Add constraints or additional inputs     |
| Over-reliance on AI                            | Medium | Use as decision support, not replacement |
| Poor input data quality                        | High   | Validate historical data                 |

**Overall risk rating: MEDIUM–HIGH** — requires human oversight.

---

🔁 Version History

### v1.0 — Initial draft

Prompt: “Predict next week sales.”
Output: Vague predictions with no structure
Observed effect: Not usable for decision-making
Lesson learned: Need structure and constraints

---

### v1.1 — Added forecasting structure

Change: Added product focus and percentage change
Output: More useful but inconsistent
Observed effect: Difficult to compare across runs
Lesson learned: Need format standardisation

---

### v1.2 — Structured + grounded forecast ✅ Current

Change: Added:

* clear outputs (top products, % change, risks)
* constraint to use only provided data
* structured format

Output: Consistent and actionable forecasts
Observed effect:Reliable for inventory planning
**Lesson learned:** Structured + grounded prompts improve forecast usability

---

