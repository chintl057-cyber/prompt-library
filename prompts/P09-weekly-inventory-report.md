# 📊 P09 Weekly inventory performance report

**Section:** 04 — Reporting

**Workflow step:** Step 1 of 2

**Current version:** v1.2

**Status:** ✅ Tested
---

## 📌 Prompt Text (v1.2 — current)

```text
You are a retail operations analyst.

Generate a weekly inventory report based on all provided data.

Include:
- Key demand trends
- Stock issues (low stock, overstock, expiry)
- Actions taken
- Overall performance summary
- 2 strategic recommendations

Constraints:
- Max 250 words
- Clear business language
- Bullet points

Input:
[P01–P08 outputs]
```

---

## 🧩 Placeholders

| Placeholder         | Source               |
| ------------------- | -------------------- |
| `[P01–P08 outputs]` | All previous prompts |

---

## 🏢 Workflow

```text
All prompts → [P09 RUNS] → Weekly report  
→ Sent to management
```

---

## ❗ Problem

Reporting is manual, slow, and inconsistent.

---

## ⚡ Automation Potential

Very High (~80%)

---

## ⚠️ Risks

| Risk             | Mitigation   |
| ---------------- | ------------ |
| Missing insights | Human review |

---

## 🔄 Version History

### v1.0 
**Prompt:** Generate a weekly inventory report.  
**Output:**  
Produced a generic summary of inventory data without clear structure or prioritisation. Key insights were mixed together and difficult to scan.  
**Observed effect:**  
- Report lacked clear sections (trends, risks, actions)  
- Difficult for managers to quickly extract key insights  
- Required manual editing before presentation  

---

### v1.1 — Added structured reporting sections  
**Change:**  
- Introduced structured sections:
  - demand trends  
  - stock issues  
  - actions taken  
- Improved clarity of outputs  

**Output:**  
More organised report with clearer separation of insights.  

**Observed effect:**  
- Easier to read but still inconsistent in length and detail  
- Some outputs were too long or included unnecessary information  

**Lesson learned:**  
Need constraints on length and clearer prioritisation of key insights.

---

### v1.2 — Refined and management-ready report ✅ Current  
**Change:**  
- Added **word limit (250 words)**  
- Required **strategic recommendations**  
- Enforced **bullet-point format**  
- Improved instruction for **business-focused language**  

**Output:**  
Concise, structured, and management-ready weekly report highlighting key trends, risks, and actions.  

**Observed effect:**  
- Significantly improved readability and usability  
- Managers could quickly understand performance and make decisions  
- Reduced need for manual editing  

**Lesson learned:**  
Combining **structure + constraints + business-focused outputs** produces reports suitable for executive decision-making.
---

