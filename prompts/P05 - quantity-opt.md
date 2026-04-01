# 🛒 P05 Reorder recommendation and quantity optimisation

Section: 02 — Inventory Management

Workflow step: Step 2 of 2

Current version:v1.2

Status: ✅ Tested

---

## 📌 Prompt Text (v1.2 — current)

```text 
You are a retail inventory planning specialist at a supermarket chain.

Using the demand forecast and current inventory data, recommend optimal reorder quantities.

Provide:
- Products that require reorder
- Recommended reorder quantity for each product (units)
- Justification based on demand forecast and stock levels
- Suggested reorder priority (High / Medium / Low)
- 2 risks if reorder decisions are incorrect

Context:
The goal is to optimise stock levels to avoid stockouts and overstocking while maintaining operational efficiency.

Constraints:
- Use ONLY the provided data
- Do NOT assume missing values
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Input data:
- Demand forecast: [P02_OUTPUT]
- Current stock levels: [STOCK_DATA]
- Sales velocity: [SALES_VELOCITY]
```

---

## 🧩 Placeholders to fill

| Placeholder        | Source                            | Example                            |
| ------------------ | --------------------------------- | ---------------------------------- |
| `[P02_OUTPUT]`     | Output from P02 (Demand forecast) | "Milk forecast: 700 units (+15%)"  |
| `[STOCK_DATA]`     | Inventory system (ERP)            | "Milk: 100 units, Bread: 50 units" |
| `[SALES_VELOCITY]` | POS data (daily avg sales)        | "Milk: 20/day"                     |

---

## 🏢 Intended Workflow or Task

* Trigger: Completion of P04 (Low stock alert) + P02 (Demand forecast)
* Actor: Inventory planner / store manager
* Timing: Runs before placing supplier orders
* Next step: Output used to generate purchase orders

```text
P02 forecast + P04 alerts → [P05 RUNS] → Reorder plan generated  
→ Manager reviews → Purchase order placed
```

---

## ❗ Problem Being Solved

Reorder decisions are often made manually using incomplete information.

* Managers rely on experience rather than data
* Inconsistent reorder quantities across stores
* Risk of under-ordering or over-ordering

This leads to:

* Stockouts → lost sales
* Overstock → increased holding costs and waste
* Inefficient inventory turnover

**Pain points addressed:**

* Lack of data-driven reorder decisions
* Inconsistent inventory planning
* Time-consuming manual calculations

---

## ⚡ Automation Potential

Level: High

| Dimension               | Assessment                                       |
| ----------------------- | ------------------------------------------------ |
| Repetitiveness          | High — performed regularly across all stores     |
| Data availability       | High — forecast and inventory data available     |
| Human judgment needed   | Medium — final approval required                 |
| Integration possibility | Very high — connects to ERP and ordering systems |
| Estimated time saving   | ~70–80% reduction                                |

Human-in-the-loop role:
Managers review and approve reorder recommendations before placing orders.

---

## ⚠️ Risks and Limitations

| Risk                                                    | Level  | Mitigation                             |
| ------------------------------------------------------- | ------ | -------------------------------------- |
| Incorrect forecast leads to poor reorder decisions      | High   | Validate forecast outputs before use   |
| Overstock due to overestimation                         | Medium | Apply safety stock limits              |
| Stockouts due to underestimation                        | High   | Include buffer stock rules             |
| Ignoring supplier constraints (lead time, availability) | Medium | Integrate supplier data where possible |

Overall risk rating:** MEDIUM–HIGH — critical decisions require human validation.

---

## 🔄 Version History

### v1.0 — Initial draft

Prompt: Suggest reorder quantities.
Output: Basic suggestions with no justification
Observed effect: Not reliable for decision-making
Lesson learned: Need structured reasoning and priorities

---

### v1.1 — Added justification and priorities

Change: Included reorder reasoning and priority levels
Output: More useful but inconsistent format
Observed effect: Difficult to standardise across stores
Lesson learned: Need constraints and structured output

---

### v1.2 — Structured + optimised decision output ✅ Current

Change: Added:

* clear outputs (quantity, priority, risks)
* grounding constraints
* structured format

Output: Clear, actionable, and consistent reorder recommendations
Observed effect: Improved decision speed and consistency
Lesson learned: Structured prompts improve decision reliability and business value

---

## 🔗 Related Prompts

* Previous in chain: P04 — Low stock alert / P02 — Demand forecast
* Next in chain: P06 — Overstock detection
* Parent section: 02 — Inventory Management

---
