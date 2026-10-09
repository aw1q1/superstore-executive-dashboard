# 📊 Retail Performance Executive Dashboard

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Business Intelligence](https://img.shields.io/badge/Domain-Business_Intelligence-blue?style=for-the-badge)
![Analytics](https://img.shields.io/badge/Level-Executive_Reporting-0F172A?style=for-the-badge)

An enterprise-grade, interactive executive dashboard built entirely in Microsoft Excel using advanced data modeling, dynamic UI/UX design systems, and automated narrative logic on the Global Superstore dataset (2016–2019).

---

## 🖥️ Dashboard Showcase

| Default State (Overview) | Filtered State (Interactivity Proof) |
| :---: | :---: |
| ![Dashboard Overview](assets/dashboard-overview.png) | ![Dashboard Filtered](assets/dashboard-filtered.png) |

---

## 🎯 Architectural Highlights & Philosophy

- **Modern Web-App UI/UX:** Styled using a structured 60-30-10 color hierarchy (Dark Slate `#0F172A`, Royal Blue `#2563EB`, and Emerald `#059669`), paired with a customized dark sidebar for interactive slicing.
- **Dynamic Executive Narrative (Smart Insights):** Unlike static text boxes, the insights engine leverages dynamic Excel string concatenation (`IF`, `TEXT`, and structured cell referencing) to recalculate executive summaries, top regions, and margin health alerts dynamically upon slicer selection.
- **Solving Scale Disparity:** Optimized vertical axis bounds (`$275K` maximum and `Thousands` display units) and adjusted series gap widths to legibly visualize high-revenue items alongside minor sub-categories without crowding.
- **Integrated Data Governance:** Built with an isolated calculation layer (`Pivot_Tables`) and a dedicated documentation sheet (`Docs`) detailing data architecture, formulas, and recommendations.

---

## 📁 Workbook Architecture

| Sheet Name | Layer Type | Purpose & Contents |
| :--- | :--- | :--- |
| **`Dashboard`** | Presentation | Primary executive interface containing KPIs, slicers, monthly seasonality trends, segment distribution, profitability bars, and dynamic automated narratives. |
| **`Docs`** | Documentation | Project metadata, metrics dictionary, technical architecture, and strategic business recommendations. |
| **`Pivot_Tables`** | Calculation Engine | Background calculation layer with 5 core PivotTables feeding the presentation interface. |
| **`Cleaned_Data`** | Transformed Layer | Validated dataset featuring calculated features (`Profit Margin %` and `Sales Category` tiers). |
| **`Orders`** | Raw Data Source | Primary transactional records containing 9,994 order lines across retail operations. |
| **`People` / `Returns`**| Reference Tables | Relational lookup tables mapping regional sales managers and order return statuses. |

---

## 📐 Key Metrics & Definitions

- **Total Sales (`$2,297,201`):** Gross revenue generated across all completed transactions (`SUM(Sales)`).
- **Total Profit (`$286,397`):** Net operating profit after accounting for costs, discounts, and overhead (`SUM(Profit)`).
- **Profit Margin (`12.5%`):** Aggregate operating margin benchmarked against an internal target of $\ge 12.0\%$ (`Total Profit / Total Sales`).
- **Top Region (`West`):** Identified via automated rank evaluation, delivering over `$725K` in volume at a healthy `14.9%` margin.

---

## 💡 Strategic Business Recommendations

1. **Stem Margin Bleed in Furniture:** Severe margin erosion identified in **Tables** (-$17.7K) and **Bookcases** (-$3.5K). Recommended capping discounts at 20% and reviewing vendor freight costs.
2. **Double Down on Technology:** The **Technology** segment anchors company-wide profitability, driven by **Copiers** and **Phones**. Inventory allocations should prioritize high-velocity tech items.
3. **Replicate West Region's Operating Playbook:** The **West** region operates at a strong `14.9%` margin, whereas the **Central** region lags at `7.9%`. Recommended conducting a regional pricing audit and restructuring Central's shipping fees.

---

## 🚀 How to Run the Workbook

1. Clone or download this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)aw1q1/superstore-executive-dashboard.git
