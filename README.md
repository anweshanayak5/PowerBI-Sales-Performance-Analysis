# Sales Performance & Profitability Analysis | Power BI

## Project Overview

This project analyses an **e-commerce transactional dataset** using Microsoft Power BI to understand how sales translate into profitability across products, customers, payment modes and geographies.

Rather than treating the dashboard as a collection of sales charts, the analysis follows a **performance-improvement approach**:

**Sales → Profitability → Benchmarking → Problem Identification → Improvement Opportunity**

The objective was to move beyond answering *"How much did we sell?"* and instead answer:

> **"Where are we generating revenue without generating sufficient profit, and where should management investigate further?"**

The dashboard combines data modelling, DAX-based KPI development, segmentation and profitability benchmarking to identify commercially relevant performance gaps.

---

# 1. Business Context

E-commerce businesses typically generate large volumes of transactional data covering orders, products, customers, locations and payment methods.

However, high sales do not necessarily indicate strong business performance.

A product can generate significant revenue while contributing little or even negative profit because of factors such as:

- Low pricing relative to cost
- Product-level margin differences
- Discounting
- Product mix
- Order economics
- Customer or category-level differences

Therefore, analysing **sales alone** can lead to incomplete conclusions.

This project was designed around that problem.

Instead of stopping at revenue reporting, the analysis connects **sales performance with profitability** to identify segments that may require managerial attention.

---

# 2. Dataset

The analysis uses a **transaction-level e-commerce dataset** containing information related to customer orders and individual order details.

The dataset was structured around two key tables:

### Orders Table

The Orders table contains information associated with the overall order, such as:

- Order ID
- Order date
- Customer information
- Geographic information
- Payment mode
- Other order-level attributes

### Details Table

The Details table contains information at the individual order/product level, including:

- Order ID
- Product/category information
- Sales value
- Quantity
- Profit
- Product/sub-category information

The two tables were connected using **Order ID**, creating a one-to-many relationship:

**One Order → Multiple Order Details**

This structure was retained instead of combining everything into one flat table because separating order-level and transaction-level information makes the model more structured and reduces unnecessary duplication.

It also allows the dashboard to analyse performance from multiple perspectives — order, product, customer and geography — while maintaining a consistent relationship between the data.

---

# 3. Why an E-commerce Dataset?

An e-commerce dataset is particularly useful for performance analysis because it captures multiple dimensions of business performance within the same transaction.

A single order can provide information about:

**Who bought → What they bought → When they bought → Where they bought → How they paid → How much revenue was generated → How much profit was generated**

This makes the dataset suitable for analysing not only sales volume but also **commercial performance and profitability drivers**.

The dataset therefore provides an opportunity to simulate a real business problem:

> A company has substantial transaction data, but needs to convert that data into actionable performance insights.

---

# 4. Business Objective

The dashboard was developed to answer six core business questions:

### Sales Performance
- How are sales performing over time?
- Which categories and sub-categories contribute most to revenue?

### Profitability
- Which products generate strong revenue but weak profitability?
- Which sub-categories generate margins above or below the overall business level?

### Customer Performance
- Which customers contribute significantly to sales?
- Is revenue concentrated among a small number of customers?

### Geographic Performance
- Which locations contribute significantly to sales and profitability?
- Are there geographic differences in business performance?

### Payment Behaviour
- Which payment modes are most frequently used?

### Performance Improvement
- Which high-revenue segments may require profitability improvement?

The final question is particularly important because it shifts the dashboard from **descriptive reporting** toward **decision support**.

---

# 5. Why These Metrics?

The dashboard does not rely on revenue alone.

Five primary KPIs were selected to provide a balanced view of business performance:

| KPI | Value | Why it matters |
|---|---:|---|
| Total Sales | ₹437.77K | Measures revenue generated |
| Total Profit | ₹36.96K | Shows the financial contribution after costs |
| Total Orders | 500 | Indicates transaction volume |
| Total Quantity | 5,615 | Shows product volume sold |
| Profit Margin | 8.44% | Measures profitability relative to sales |

### Why include both Sales and Profit?

Sales answer:

> **"How much did we generate?"**

Profit answers:

> **"How much value did we actually retain?"**

Using both prevents high-revenue but low-profit segments from being automatically interpreted as strong performers.

### Why Profit Margin?

Absolute profit can favour products with larger sales volumes.

Profit margin provides a more comparable measure:

**Profit Margin = Profit ÷ Sales × 100**

This allows products with different revenue levels to be compared on profitability efficiency.

---

# 6. Analytical Approach

The analysis follows a structured performance-improvement framework:

### Step 1 — Establish the Business Baseline

The Executive Overview establishes the overall performance baseline using:

- Sales
- Profit
- Orders
- Quantity
- Profit margin
- Monthly trends

This provides the context required before analysing individual segments.

---

### Step 2 — Identify Revenue Contributors

The next step analyses:

- Categories
- Sub-categories
- Products
- Customers
- Geography

The purpose is to identify **where revenue is coming from**.

However, revenue contribution alone is not treated as the final measure of performance.

---

### Step 3 — Connect Revenue with Profitability

The analysis then compares sales with profit margins.

This helps identify situations such as:

**High Sales + High Margin → Strong performer**

**High Sales + Low Margin → Potential improvement opportunity**

**Low Sales + High Margin → Potentially attractive niche**

**Low Sales + Low Margin → Lower-priority segment**

This approach is more useful than ranking products only by sales because it considers both **scale and economic efficiency**.

---

# 7. Why Benchmarking Was Used

A key part of the analysis is the use of the **overall profit margin of 8.44% as a benchmark**.

The purpose of the benchmark is not to claim that every product should achieve exactly 8.44%.

Instead, it provides a simple internal reference point:

> **How does each sub-category perform relative to the business's overall profitability?**

This allows the analysis to flag segments that generate meaningful revenue but operate below the overall margin.

For example:

- Electronic Games — **₹39.17K sales, -1.64% margin**
- Phones — **₹46.12K sales, 4.00% margin**
- Chairs — **₹34.22K sales, 4.75% margin**
- Saree — **₹59.09K sales, 6.87% margin**

All four fall below the overall **8.44% benchmark**.

This makes them potential areas for further investigation.

---

# 8. Why This Approach Instead of Only Sales Ranking?

A simple sales ranking would identify the products generating the highest revenue.

However, this can create a misleading conclusion.

For example:

**Product A**
- Sales: ₹60K
- Profit margin: 3%

**Product B**
- Sales: ₹45K
- Profit margin: 15%

A sales-only dashboard would rank Product A higher.

A profitability-oriented analysis highlights that Product B may be generating revenue more efficiently.

Therefore, the project deliberately combines:

**Revenue Scale + Profitability Efficiency**

rather than relying on a single metric.

---

# 9. Why This Is a Diagnostic Analysis

The dashboard is intentionally **diagnostic rather than predictive**.

The objective was not to forecast future sales or build a machine-learning model.

Instead, the first question is:

> **Where is the current performance problem?**

Only after identifying the problem would a business typically move toward:

- Root-cause analysis
- Pricing analysis
- Cost analysis
- Discount analysis
- Inventory analysis
- Customer-level investigation
- Forecasting
- Prescriptive recommendations

Therefore, predictive modelling was not prioritised at this stage.

The dashboard acts as the **first layer of a performance-improvement process**.

---

# 10. How the Analysis Supports Process Improvement

The value of the dashboard is not simply that it visualises existing data.

It changes the way the performance review can be conducted.

### Traditional approach

**Sales report → Manual review → Identify numbers → Discuss problems**

This can make it difficult to determine which segments deserve attention first.

### Dashboard-driven approach

**Data → KPI baseline → Segment analysis → Benchmarking → Flag performance gaps → Investigate root causes**

This creates a more structured process.

For example, instead of reviewing hundreds of products manually, management can first identify:

> **Which high-revenue sub-categories are below the overall profitability benchmark?**

Those segments can then become the focus of deeper investigation.

---

# 11. Example of a Performance-Improvement Opportunity

Consider **Electronic Games**.

The segment generated:

- **₹39.17K in sales**
- **-1.64% profit margin**

A sales-only dashboard might classify the segment as successful because it generates substantial revenue.

The profitability analysis tells a different story.

The segment is generating revenue but operating below the overall business profitability benchmark.

This does **not** automatically mean the product should be discontinued.

Instead, it creates a specific diagnostic question:

> **Why is this segment generating revenue without generating sufficient profit?**

Possible areas for further investigation could include:

- Product-level costs
- Pricing
- Discounts
- Product mix
- Order economics
- Customer segments
- Geographic differences

Thus, the dashboard does not pretend to identify the root cause from insufficient data. It **narrows the problem to where deeper analysis should begin**.

---

# 12. Key Insights

### Overall Performance

The business generated:

- **₹437.77K in sales**
- **₹36.96K in profit**
- **500 orders**
- **5,615 units**
- **8.44% overall profit margin**

The 8.44% margin serves as the internal benchmark for subsequent analysis.

### High-Revenue but Lower-Margin Segments

Several segments generate significant sales while remaining below the overall profitability benchmark:

- Electronic Games — ₹39.17K sales, -1.64% margin
- Phones — ₹46.12K sales, 4.00% margin
- Chairs — ₹34.22K sales, 4.75% margin
- Saree — ₹59.09K sales, 6.87% margin

These segments represent potential areas for performance investigation.

### Higher-Margin Segments

Other segments demonstrate stronger profitability:

- Printers — ₹59.25K sales, 14.52% margin
- Accessories — 15.43% margin

These segments can provide useful internal comparisons when investigating what may be driving stronger profitability.

---

# 13. Dashboard Structure

## Page 1 — Executive Overview

The first page provides the business baseline.

It focuses on:

- Total sales
- Total profit
- Total orders
- Total quantity
- Overall margin
- Monthly performance
- Category-level performance

### Purpose

To answer:

> **"What is the overall health of the business?"**

---

## Page 2 — Product & Customer Insights

This page moves from overall performance to the underlying contributors.

It analyses:

- Product/sub-category performance
- Customer contribution
- Payment-mode usage
- Sales and profitability relationships

### Purpose

To answer:

> **"Which products and customers are driving the observed performance?"**

---

## Page 3 — Performance Improvement

The final page applies the profitability benchmark.

Sub-categories are compared against the **8.44% overall profit-margin benchmark** to highlight weaker-performing segments.

### Purpose

To answer:

> **"Where should management investigate for potential profitability improvement?"**

This makes the third page the transition from **reporting to action-oriented analysis**.

---

# 14. Performance-Improvement Logic

The dashboard can be summarised through the following decision framework:

```text
E-commerce Transactions
          ↓
Data Modelling
          ↓
KPI Development
          ↓
Sales & Profitability Analysis
          ↓
Product / Customer / Geographic Segmentation
          ↓
8.44% Profitability Benchmark
          ↓
Identify Below-Benchmark Segments
          ↓
Prioritise Areas for Root-Cause Investigation
          ↓
Potential Pricing / Cost / Mix / Process Improvements
