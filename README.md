# Amazon India — Category Intelligence Report

![Excel](https://img.shields.io/badge/Excel-Data%20Cleaning%20%26%20Feature%20Engineering-217346?style=flat&logo=microsoftexcel&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat&logo=powerbi&logoColor=black)
![Data Source](https://img.shields.io/badge/Data%20Source-Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-1D9E75?style=flat)

An end-to-end data analytics project analyzing Amazon India's product catalog using the Amazon Sales Dataset. The project follows a complete business intelligence workflow: data cleaning and feature engineering in Excel Power Query, pivot table analysis, and a 3-page interactive Power BI dashboard.

---

## Dashboard Preview

### Page 1: Executive Overview
![Executive Overview](visuals/Executive%20Overview.png)

### Page 2: Pricing & Discount Analysis
![Pricing & Discount Analysis](visuals/Pricing%20%26%20Discount%20Analysis.png)

### Page 3: Risk & Opportunity Analysis
![Risk & Opportunity Analysis](visuals/Risk%20%26%20Opportunity%20Analysis.png)

---

## Business Scenario

Amazon India runs aggressive quarterly discount campaigns across its product catalog, but heading into the next promotional planning cycle, the Category Management team raised concerns about whether these discounts were actually working. The Senior Category Manager needed a data-backed answer to whether discount depth improves customer ratings and engagement, which products carry high visibility but poor quality, and which categories deserve campaign investment.

As the Data Analyst on the Category Intelligence team, the task was to analyze the full product catalog and surface findings to guide the next discount and promotional strategy.

**Role:** Data Analyst
**Tools:** Microsoft Excel, Power BI, DAX
**Dataset:** Amazon Sales Dataset (Kaggle), 1,464 products across 9 categories

---

## Key Findings

| Area | Finding |
|---|---|
| Discount Effectiveness | Low-discount products average a 4.17 rating versus 4.07 for high-discount products — a consistent inverse pattern across the catalog, directly challenging the assumption that deeper discounts drive satisfaction. |
| Premium Pricing | Products priced above ₹10,000 achieve the highest average rating (4.20) while requiring the lowest average discount (32.40%), proving high discounts are not necessary for satisfaction. |
| Category Exceptions | Electronics and Computers & Accessories sustain strong ratings (4.2–4.3) even at 45–55% discount depth, making them structurally different from the rest of the catalog and the safest categories for aggressive promotions. |
| Quality Risk | 145 products (9.9% of the catalog) are flagged "At Risk" with ratings below 3.8, concentrated in Home & Kitchen (60), Electronics (55), and Computers & Accessories (30). |
| Value Opportunities | Home Improvement, Computers & Accessories, and Electronics lead on Value Index, representing the strongest candidates for Deal of the Day campaign investment. |

---

## Recommendations

1. **Discount strategy:** Adopt category-specific discounting instead of a blanket strategy. Reserve deep discounts (45%+) for categories proven to tolerate them, such as Electronics and Computers & Accessories.
2. **Campaign prioritization:** Prioritize Electronics and Computers & Accessories for the next Deal of the Day rotation — they combine the highest discount tolerance with strong ratings and dominate the Top 10 Value Products table.
3. **Quality intervention:** Launch targeted quality reviews in Home & Kitchen and Electronics, which carry the highest absolute number of at-risk products (60 and 55).
4. **Premium pricing:** Reduce discount dependency on products above ₹10,000. This segment already achieves the highest ratings at the lowest discount depth — shift toward value-based positioning to protect margin.
5. **Investment focus:** Treat Home Improvement, Computers & Accessories, and Electronics as the core value-driving categories for future investment, based on consistent leadership across the value index and discount health analyses.

---

## Project Workflow

1. Downloaded Amazon Sales Dataset from Kaggle (1,465 rows, 16 columns)
2. Defined business scenario, stakeholders, and 4 core business problems
3. Defined 5 KPIs with formulas: Discount Depth, Customer Satisfaction Score, Engagement Volume, Value-for-Money Index, Category Satisfaction Benchmark
4. Cleaned and transformed the dataset using Excel Power Query — removed currency symbols and commas from price columns, removed 1 corrupt rating row, converted rating and engagement columns to correct numeric types
5. Split the hierarchical category column into `category_lvl1` and `category_lvl2`
6. Engineered 6 new calculated columns: `discount_depth`, `discount_flag`, `weighted_rating`, `value_index`, `low_rating_flag`, `price_bucket`, plus `price_bucket_order` for chart sorting
7. Ran 5 pivot table analyses in Excel to validate initial hypotheses around discount bands, price distribution, and category satisfaction
8. Built a 3-page interactive Power BI dashboard with DAX measures, category/discount/price slicers, and conditional formatting
9. Documented findings and recommendations in a business-facing insights report

---

## DAX Measures

Key measures built in Power BI:

- Total Products, Average Rating, Average Discount %, At Risk Product Count
- % At Risk Products
- Weighted Average Rating
- Average Discount Depth
- High Value Products Count
- At Risk Count by Category

Full measures available in the `.pbix` file.

---

## Dashboard Pages

**Page 1: Executive Overview**
KPI cards for total products, average rating, average discount %, and at-risk product count. Product distribution by category donut chart, category satisfaction bar chart (sorted by weighted rating), and product count by price bucket. Category and discount flag slicers.

**Page 2: Pricing & Discount Analysis**
Discount depth vs product rating scatter plot, average rating by discount level (Low/Medium/High) bar chart, price band performance combo chart with discount trend line, and category discount health bubble chart (rating vs discount depth, sized by engagement). Category and price bucket slicers.

**Page 3: Risk & Opportunity Analysis**
Value index by category bar chart, at-risk products by category bar chart, popularity-quality trap scatter plot, and top 10 value products table with conditional formatting. Category and risk flag slicers.

---

## Project Structure

```
amazon-category-intelligence/
│
├── README.md
│
├── data/
│   ├── raw data/                         # Original Kaggle CSV file
│   └── clean_data/                       # Excel Power Query cleaned file
│
├── excel/
│   └── amazon_analysis.xlsx              # Pivot tables and quick analysis
│
├── powerbi/
│   └── amazon_dashboard.pbix             # Full Power BI dashboard file
│
├── visuals/
│   ├── Executive Overview.png
│   ├── Pricing & Discount Analysis.png
│   └── Risk & Opportunity Analysis.png
│
└── documentation/
    ├── Business_Problems.docx            # Business scenario, role, and core problems
    └── Insights and Recommendation.docx  # Key findings and recommendations
```

> Note: create a `visuals/` folder in the repo root and add your 3 dashboard page screenshots there (named to match the paths above) so the Dashboard Preview images render correctly.

---

## Skills Demonstrated

Data cleaning and transformation, feature engineering, pivot table analysis, KPI development, DAX calculations, Power BI dashboard design, business analysis, data storytelling.

---

## How to Open

**Excel files:** Open with Microsoft Excel 2016 or later.

**Power BI file:** Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free) → File → Open → select `amazon_dashboard.pbix`

**Data Source:** Kaggle — Amazon Sales Dataset · Tools: Microsoft Excel, Power BI Desktop

---

## About

**Sandipa**

[GitHub](#https://github.com/sandipakun) · [LinkedIn](#)
