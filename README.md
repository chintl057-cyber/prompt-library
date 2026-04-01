# 📦 Prompt Library — Retail Inventory Replenishment & Stock Management

Assessment 1 | Generative AI for Business

Student: Thi Lan Chi, NGUYEN

Business Field: Retail Operations — Inventory Replenishment & Stock Management

Model tested on: GPT-4o 
Last updated: 1 April 2026

---

# 📌 What This Library Does

This prompt library supports workflow automation for retail inventory replenishment and stock management.

It contains 10 documented, tested, and iterated prompts designed to help supermarket/store managers make faster, data-driven inventory decisions.

The prompts focus on solving key operational challenges such as:

* Stockouts (lost sales)
* Overstocking (waste and storage cost)
* Manual reporting inefficiencies
* Poor demand forecasting

Each prompt entry follows a consistent structure:

* Exact prompt text (with placeholders)
* Workflow task it supports
* Business problem it solves
* Automation potential
* Risks and mitigation strategies
* Version history and test results

---

# 📂 Folder Structure

```
prompt-library/

├── README.md ← You are here (library index)

├── 01-demand-analysis/
│   ├── P01-sales-trend-summary.md
│   ├── P02-demand-forecast.md
│   ├── P03-seasonality-detection.md

├── 02-inventory-management/
│   ├── P04-low-stock-alert.md
│   ├── P05-reorder-recommendation.md

├── 03-risk-monitoring/
│   ├── P06-overstock-detection.md
│   ├── P07-expiry-risk-analysis.md
│   ├── P08-supply-delay-impact.md

├── 04-reporting/
│   ├── P09-weekly-inventory-report.md
│   ├── P10-store-performance-comparison.md
```

💡 *Folders are organised based on business workflow stages: demand → stock → risk → reporting*

---

# 📊 Library Summary Table

| ID  | Prompt Name                  | Workflow             | Automation Level | Risk Level | Status         |
| --- | ---------------------------- | -------------------- | ---------------- | ---------- | -------------- |
| P01 | Sales trend summary          | Demand analysis      | High             | Low        | ✅ Tested       |
| P02 | Demand forecast              | Demand analysis      | Medium           | Medium     | ✅ Tested       |
| P03 | Seasonality detection        | Demand analysis      | Medium           | Medium     | ✅ Tested       |
| P04 | Low stock alert              | Inventory management | High             | Low        | ✅ Tested       |
| P05 | Reorder recommendation       | Inventory management | High             | Medium     | ✅ Tested       |
| P06 | Overstock detection          | Risk monitoring      | High             | Medium     | ✅ Tested       |
| P07 | Expiry risk analysis         | Risk monitoring      | Medium           | High       | ✅ Tested       |
| P08 | Supply delay impact          | Risk monitoring      | Medium           | High       | ✅ Tested       |
| P09 | Weekly inventory report      | Reporting            | High             | Low        | 🔄 In progress |
| P10 | Store performance comparison | Reporting            | Medium           | Medium     | 🔄 In progress |

**Automation levels:** Very High / High / Medium / Low
**Risk levels:** High (needs human review) / Medium / Low

---

# 🔗 Prompt Chaining Map

Some prompts are designed to work together in sequence.

### 📦 INVENTORY DECISION CHAIN

P01 (Sales trend summary)
→ P02 (Demand forecast)
→ P05 (Reorder recommendation)

### ⚠️ RISK MONITORING CHAIN

P06 (Overstock detection)
→ P07 (Expiry risk analysis)
→ P08 (Supply delay impact)

### 📊 REPORTING CHAIN

P01 + P04 + P06 outputs
→ P09 (Weekly inventory report)
→ P10 (Store performance comparison)

---

# ⚙️ Prompting Strategies Used

| Strategy                                        | Prompts       | Why chosen                                    |
| ----------------------------------------------- | ------------- | --------------------------------------------- |
| RACE framework (Role–Action–Context–Evaluation) | P01, P02, P05 | Ensures consistent and structured outputs     |
| Grounding constraint ("use only provided data") | P04, P06, P07 | Prevents hallucination in inventory decisions |
| Structured output (bullet points / tables)      | All           | Makes outputs usable for managers             |
| Word/format limits                              | All           | Reduces need for editing                      |
| Self-check / validation step                    | P05, P08      | Improves reliability for decision-making      |

---

# 🔁 Iteration Evidence

All prompt versions are stored in this repository.

**Commit history = version log**
Each commit documents:

* What changed
* Why it changed
* What improved

| Prompt | Versions    | Key improvement                                       |
| ------ | ----------- | ----------------------------------------------------- |
| P01    | v1.0 → v1.2 | Added role + structured output → clearer insights     |
| P05    | v1.0 → v1.2 | Added constraints → more accurate reorder suggestions |
| P06    | v1.0 → v1.1 | Added data grounding → reduced hallucination          |
| P07    | v1.0 → v1.2 | Added risk thresholds → more actionable outputs       |

---

# 🎯 Business Impact

This prompt library is designed to deliver measurable value:

* ⏱ Reduce manual reporting time by 60–80%
* 📉 Reduce stockouts → increase sales
* 📦 Reduce overstock → lower storage and waste costs
* 📊 Improve decision consistency across stores

---

# ⚠️ Risks & Governance

Key risks include:

* AI hallucination → mitigated with grounding constraints
* Incorrect forecasts → human validation required
* Over-reliance on AI → maintain human-in-the-loop

---

# 🚀 Summary

This project demonstrates how AI prompting can:

* Automate inventory workflows
* Improve operational efficiency
* Support better retail decision-making

It provides a scalable, practical solution suitable for real-world retail environments.
