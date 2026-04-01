# 📦 P04 Low stock alert and replenishment trigger

Section: 02 — Inventory Management

Workflow step: Step 1 of 2

Current version: v1.2

Status: ✅ Tested

---

## 📌 Prompt Text (v1.2 — current)

```text 
You are a retail inventory monitoring specialist at a supermarket chain.

Analyse the current inventory levels and sales velocity data.

Identify:
- Products that are at risk of stockout within the next 3–5 days
- Products with critically low stock levels (below threshold)
- 2 potential business impacts if no action is taken
- 2 recommended actions for immediate response

Context:
The goal is to detect low-stock risks early and trigger replenishment actions to avoid lost sales.

Constraints:
- Use ONLY the data provided
- Do NOT assume missing values
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Input data:
- Current stock levels: [STOCK_DATA]
- Sales velocity (daily sales): [SALES_VELOCITY]
```

---

## 🧩 Placeholders to fill

| Placeholder        | Source                     | Example                           |
| ------------------ | -------------------------- | --------------------------------- |
| `[STOCK_DATA]`     | Inventory system (ERP)     | "Milk: 50 units, Bread: 20 units" |
| `[SALES_VELOCITY]` | POS sales data (daily avg) | "Milk: 15/day, Bread: 10/day"     |

---

## 🏢 Intended Workflow or Task

* Trigger: Daily inventory update from ERP system
* Actor: Store manager / inventory controller
* Timing: Runs daily (or real-time for high-demand items)
* Next step: P05 (Reorder recommendation) triggered for flagged items

```text 
Inventory + sales data → [P04 RUNS] → Low-stock risks identified  
→ Alerts generated → Reorder process triggered
```

---

## ❗ Problem Being Solved

Low stock detection is often reactive rather than proactive.

* Managers identify stockouts only after shelves are empty
* Manual monitoring is inconsistent and time-consuming
* High-demand items frequently run out

This leads to:

* Lost sales and reduced customer satisfaction
* Missed replenishment opportunities
* Inefficient store operations

**Pain points addressed:**

* Reactive stock management
* Lack of early warning system
* Manual monitoring inefficiency

---

## ⚡ Automation Potential

**Level: High

| Dimension               | Assessment                                  |
| ----------------------- | ------------------------------------------- |
| Repetitiveness          | Very high — monitoring happens daily        |
| Data availability       | High — stock + sales data readily available |
| Human judgment needed   | Low — rule-based detection                  |
| Integration possibility | High — connects to ERP and alert systems    |
| Estimated time saving   | ~80–90% reduction                           |

Human-in-the-loop role:
Managers review flagged items and approve reorder actions if necessary.

---

## ⚠️ Risks and Limitations

| Risk                                        | Level  | Mitigation                       |
| ------------------------------------------- | ------ | -------------------------------- |
| Incorrect stock data leads to false alerts  | High   | Ensure real-time data validation |
| Misinterpretation of sales velocity         | Medium | Use averaged or smoothed data    |
| Over-alerting (too many flagged items)      | Medium | Set threshold limits             |
| Ignoring external factors (delivery delays) | Medium | Combine with supply data         |

**Overall risk rating:** MEDIUM — suitable for automation with monitoring.

---

## 🔄 Version History

### v1.0 — Initial draft

Prompt: Identify low stock items.
Output: Basic list with no context or urgency
Observed effect: Not actionable for decision-making
Lesson learned: Need thresholds and business context

---

### v1.1 — Added risk detection

Change: Included stockout risk and business impact
Output: More useful but inconsistent format
Observed effect: Difficult to standardise alerts
Lesson learned: Need structured output and constraints

---

### v1.2 — Structured + actionable alerts ✅ Current

Change: Added:

* clear outputs (risk, impact, actions)
* constraints and format
* time-based risk (3–5 days)

Output: Clear and actionable low-stock alerts
Observed effect: Faster response and improved stock management
Lesson learned: Structured prompts improve operational usability

---

## 🔗 Related Prompts

* Previous in chain: P03 — Seasonality detection
* Next in chain: P05 — Reorder recommendation
* Parent section: 02 — Inventory Management

---
