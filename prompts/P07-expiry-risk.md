# ⏳ P07 Expiry risk analysis and waste prevention

**Section:** 03 — Risk Monitoring

**Workflow step:** Step 2 of 3

**Current version:** v1.1

**Status:** ✅ Tested

---

## 📌 Prompt Text (v1.1 — current)

```text
You are a retail inventory risk analyst at a supermarket chain.

Analyse inventory data including expiry dates and sales velocity.

Identify:
- Products at risk of expiring before being sold
- Estimated time to expiry vs expected sales rate
- Potential waste impact (units or value)
- 2 recommended actions to reduce waste
- 2 risks if expiry is not managed

Context:
The goal is to minimise product waste and financial loss due to expired inventory.

Constraints:
- Use ONLY the provided data
- Do NOT assume missing values
- Maximum 200 words
- Tone: professional and concise

Output format:
- Bullet points only
- No introduction or conclusion

Input data:
- Inventory with expiry dates: [EXPIRY_DATA]
- Sales velocity: [SALES_VELOCITY]
```

---

## 🧩 Placeholders to fill

| Placeholder        | Source           | Example                              |
| ------------------ | ---------------- | ------------------------------------ |
| `[EXPIRY_DATA]`    | Inventory system | "Milk: 100 units, expires in 3 days" |
| `[SALES_VELOCITY]` | POS data         | "Milk: 20/day"                       |

---

## 🏢 Intended Workflow or Task

* **Trigger:** Inventory update with expiry tracking
* **Actor:** Store manager / operations team
* **Timing:** Daily for perishable goods
* **Next step:** P08 (supply adjustment / mitigation actions)

```text
Inventory + expiry data → [P07 RUNS] → Expiry risks identified  
→ Actions taken → Waste reduced
```

---

## ❗ Problem Being Solved

Perishable inventory often expires before being sold due to poor monitoring.

* Staff lack visibility of expiry timelines
* High waste in fresh food categories
* Manual tracking is inefficient

This leads to:

* Financial losses
* Increased waste disposal costs
* Sustainability issues

**Pain points addressed:**

* Poor expiry visibility
* High waste levels
* Reactive management

---

## ⚡ Automation Potential

**Level:** High

| Dimension               | Assessment                 |
| ----------------------- | -------------------------- |
| Repetitiveness          | High — daily monitoring    |
| Data availability       | High — expiry + sales data |
| Human judgment needed   | Medium                     |
| Integration possibility | High                       |
| Estimated time saving   | ~70–80%                    |

**Human-in-the-loop role:**
Managers validate and act on recommendations.

---

## ⚠️ Risks and Limitations

| Risk                              | Level  | Mitigation                  |
| --------------------------------- | ------ | --------------------------- |
| Incorrect expiry data             | High   | Validate input data         |
| Misaligned sales velocity         | Medium | Use averaged data           |
| Overreaction (discount too early) | Medium | Combine with business rules |

**Overall risk rating:** MEDIUM — manageable with oversight.

---

## 🔄 Version History

### v1.0 — Initial draft

**Date:** [Date]
**Prompt:** Identify expiring products
**Output:** Basic list
**Observed effect:** Not actionable
**Lesson learned:** Need impact + recommendations

---

### v1.1 — Structured expiry risk analysis ✅ Current

**Date:** [Date]
**Change:** Added:

* impact estimation
* actionable recommendations
* structured output

**Output:** Clear and actionable insights
**Observed effect:** Improved waste reduction decisions
**Lesson learned:** Structured prompts improve operational value

---

## 🔗 Related Prompts

* **Previous:** P06 — Overstock detection
* **Next:** P08 — Supply adjustment
* **Parent section:** Risk Monitoring

---
