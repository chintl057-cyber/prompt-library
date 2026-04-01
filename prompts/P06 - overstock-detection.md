# 📦 P06 Overstock detection and excess inventory risk analysis

**Section:** 03 — Risk Monitoring

**Workflow step:** Step 1 of 3

**Current version:** v1.2

**Status:** ✅ Tested

---

## 📌 Prompt Text (v1.2 — current)

```text 
You are a retail inventory risk analyst at a supermarket chain.

Analyse the current inventory levels and demand forecast.

Identify:
- Products with excess stock relative to demand
- Products at risk of becoming overstocked within the next 7–14 days
- Estimated impact (e.g. storage cost, waste risk)
- 2 recommended actions to reduce excess inventory
- 2 risks if overstock is not addressed

Context:
The goal is to minimise excess inventory, reduce holding costs, and prevent waste.

Constraints:
- Use ONLY the provided data
- Do NOT assume missing values
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Input data:
- Current stock levels: [STOCK_DATA]
- Demand forecast: [P02_OUTPUT]
```

---

## 🧩 Placeholders to fill

| Placeholder    | Source                            | Example                             |
| -------------- | --------------------------------- | ----------------------------------- |
| `[STOCK_DATA]` | Inventory system (ERP)            | "Milk: 500 units, Bread: 200 units" |
| `[P02_OUTPUT]` | Output from P02 (Demand forecast) | "Milk forecast: 300 units/week"     |

---

## 🏢 Intended Workflow or Task

* **Trigger:** After demand forecast and inventory updates
* **Actor:** Inventory manager / operations analyst
* **Timing:** Runs weekly or during inventory review cycles
* **Next step:** P07 (Expiry risk analysis) and P08 (supply adjustments)

```text
Inventory + forecast data → [P06 RUNS] → Overstock risks identified  
→ Actions recommended → Waste and cost reduced
```

---

## ❗ Problem Being Solved

Overstocking is a common issue in retail due to inaccurate forecasting or over-ordering.

* Excess stock increases storage and holding costs
* Perishable goods may expire before being sold
* Capital is tied up in unsold inventory

This leads to:

* Financial loss from waste
* Reduced inventory turnover efficiency
* Inefficient use of storage space

**Pain points addressed:**

* Lack of visibility into excess inventory
* Poor stock balance between demand and supply
* High operational costs due to overstock

---

## ⚡ Automation Potential

**Level:** High

| Dimension               | Assessment                                   |
| ----------------------- | -------------------------------------------- |
| Repetitiveness          | High — regular monitoring required           |
| Data availability       | High — stock + forecast data available       |
| Human judgment needed   | Medium — action decisions require validation |
| Integration possibility | High — integrates with inventory systems     |
| Estimated time saving   | ~70–80% reduction                            |

**Human-in-the-loop role:**
Managers review flagged overstock items and decide corrective actions.

---

## ⚠️ Risks and Limitations

| Risk                                              | Level  | Mitigation                                |
| ------------------------------------------------- | ------ | ----------------------------------------- |
| Incorrect classification of overstock             | Medium | Validate using historical demand patterns |
| Ignoring promotional opportunities to clear stock | Medium | Combine with marketing strategies         |
| Poor forecast accuracy affects analysis           | High   | Validate P02 outputs before use           |
| Data inaccuracies in inventory system             | High   | Ensure real-time data validation          |

**Overall risk rating:** MEDIUM — manageable with proper validation.

---

## 🔄 Version History

### v1.0 — Initial draft  
**Prompt:** Identify overstock items.  
**Output:** Basic list of overstocked products with no context or recommendations  
**Observed effect:** Not actionable for business use  
**Lesson learned:** Need to include business impact and recommended actions  

---

### v1.1 — Structured + actionable risk analysis ✅ Current  
**Change:** Added:
- clear outputs (impact, actions, risks)  
- structured bullet format  
- grounding constraint (use only provided data)  

**Output:** Clear and actionable overstock insights with business relevance  
**Observed effect:** Improved usability for inventory decision-making  
**Lesson learned:** Adding structure and constraints significantly improves output quality  

## 🔗 Related Prompts

* **Previous in chain:** P05 — Reorder recommendation
* **Next in chain:** P07 — Expiry risk analysis
* **Parent section:** 03 — Risk Monitoring

---
