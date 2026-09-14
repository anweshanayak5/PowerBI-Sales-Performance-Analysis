# Sales Performance & Profitability Analysis | Power BI

## Project Overview

An interactive Power BI analysis of an **e-commerce transactional dataset**, developed to understand how sales performance translates into profitability across products, customers, payment modes and geographies.

The project was built with a **performance-improvement lens** rather than as a purely descriptive sales dashboard.

The central question was:

> **Where is the business generating revenue, and where is that revenue not translating into sufficient profitability?**

The analysis moves through four stages:

**Sales Performance → Profitability Analysis → Benchmarking → Improvement Opportunities**

This approach helps move a performance review from simply reporting historical numbers to identifying **which segments deserve further investigation and why**.

---

## Business Problem

E-commerce businesses generate large amounts of transactional data, but sales volume alone does not provide a complete picture of business performance.

A product may generate high revenue but still contribute relatively little profit. Conversely, a lower-revenue product may generate a much stronger margin.

Therefore, a sales-only analysis can lead to incomplete conclusions.

This project focuses on the gap between:

**Revenue generated**  
and  
**Profitability achieved**

The objective was to create a dashboard that could help answer:

- Which products and sub-categories drive revenue?
- Which segments contribute most to profit?
- Where does high sales coexist with weak profitability?
- Which customers and geographies contribute significantly to performance?
- Which segments fall below the overall profitability level?
- Where should management investigate further for potential improvement?

---

# Dataset

## E-commerce Transactional Data

The project uses an **e-commerce transactional dataset** containing order-level and product-level information.

The dataset was selected because an e-commerce transaction provides multiple dimensions of business performance within a single analytical environment.

A typical transaction connects:

**Customer → Order → Product → Sales → Quantity → Profit → Geography → Payment Mode**

This makes the dataset suitable for analysing both **commercial performance and profitability**.

### Data Structure

The analysis uses two primary tables:

### Orders

The Orders table contains order-level information such as:

- Order ID
- Order date
- Customer information
- Geographic information
- Payment mode

### Details

The Details table contains product/order-detail information such as:

- Order ID
- Product
- Category
- Sub-category
- Sales
- Quantity
- Profit

The two tables were connected using **Order ID** through a **one-to-many relationship**:

**One Order → Multiple Order Details**

Maintaining the two tables separately allows order-level and product-level attributes to be analysed without unnecessarily duplicating order information.

---

## Why This Dataset?

The dataset provides enough information to examine performance from several business perspectives rather than relying on a single dimension.

For example:

| Business Question | Relevant Data |
|---|---|
| How much are we selling? | Sales |
| How profitable are we? | Profit |
| How efficiently are we generating profit? | Profit Margin |
| What are we selling? | Category / Sub-category / Product |
| Who is buying? | Customer |
| Where are sales coming from? | Geography |
| How are customers paying? | Payment Mode |
| How frequently are transactions occurring? | Orders / Quantity |

This makes the dataset appropriate for demonstrating how **transactional data can be converted into management-oriented performance analysis**.

---

# Analytical Objective

The analysis was deliberately designed around a sequence of increasingly specific questions.

### 1. Establish the Performance Baseline

First, overall business performance was established using:

- Total Sales
- Total Profit
- Total Orders
- Total Quantity
- Overall Profit Margin
- Monthly performance

This provides the baseline against which individual segments can be evaluated.

### 2. Understand Revenue Drivers

The analysis then examines:

- Categories
- Sub-categories
- Products
- Customers
- Geographies

The objective is to understand **where revenue is being generated**.

### 3. Compare Revenue with Profitability

Revenue contribution was then viewed alongside profitability.

This is important because a high-sales segment is not necessarily a high-value segment.

The analysis therefore considers combinations such as:

**High Sales + High Margin**  
→ Strong performer

**High Sales + Low Margin**  
→ Potential improvement opportunity

**Low Sales + High Margin**  
→ Potentially attractive smaller segment

**Low Sales + Low Margin**  
→ Lower-priority segment for investigation

This provides a more balanced view than simply ranking products by sales.

---

# Why Profit Margin Was Used

Absolute profit is useful, but it can favour products or categories with higher sales volumes.

Profit margin provides a common basis for comparison:

**Profit Margin = Profit ÷ Sales × 100**

For example, a segment generating ₹50K in sales at a 4% margin is economically different from one generating ₹40K at a 15% margin.

Therefore, margin was used to assess **profitability efficiency**, while sales was retained to understand the scale of the opportunity.

---

# Why Benchmarking Was Used

The overall business profit margin of **8.44%** was used as an internal benchmark.

The benchmark was not treated as a universal target for every product.

Instead, it provides a consistent reference point to identify segments performing below the overall business level.

This creates a simple screening mechanism:

**Sub-category Margin < 8.44% → Flag for further investigation**

This was preferred over arbitrarily setting an external margin target because the available dataset does not provide industry-specific profitability benchmarks.

The internal benchmark therefore keeps the analysis **data-driven and grounded in the business's own performance**.

---

# Analytical Approach

The complete analytical flow was:

```text
E-commerce Transactions
          ↓
Data Modelling
          ↓
KPI Development
          ↓
Sales Analysis
          ↓
Profitability Analysis
          ↓
Product / Customer / Geographic Segmentation
          ↓
8.44% Internal Margin Benchmark
          ↓
Identify Below-Benchmark Segments
          ↓
Prioritise Areas for Further Investigation
