# Customer Segmentation & Offer Recommendation System (Banking Analytics)

This project implements an end-to-end customer analytics pipeline for retail banking.
It uses K-Means clustering to segment customers based on financial behavior and applies
rule-based logic to recommend personalized banking offers.

---

## Problem Statement

Banks deal with customers having different income levels, spending patterns, and risk profiles.
Using a single generic strategy leads to poor engagement and revenue loss.

This project solves that by:
- Segmenting customers based on behavioral data
- Profiling each segment for business understanding
- Recommending targeted offers using explainable rules

---

## Project Workflow

### Step 1: Data Understanding & Feature Engineering
Input features:
- Customer ID
- Age
- Monthly Income
- Average Account Balance
- Number of Transactions per Month
- Credit Card Usage
- Loan Status
- Days Since Last Transaction

Engineered features:
- Activity Score
- Spend Intensity
- Credit Usage Ratio
- Dormancy Flag

Purpose: Convert raw banking data into meaningful behavior signals.

---

### Step 2: Data Preprocessing
- Missing value handling
- Outlier removal using IQR method
- Feature normalization using StandardScaler
- Categorical encoding

Purpose: Prepare data for machine learning.

---

### Step 3: Customer Segmentation
- Algorithm: K-Means Clustering
- Optimal clusters identified using Elbow Method
- Final number of clusters: 5

Output: Each customer is assigned a segment label.

---

### Step 4: Segment Profiling
For each segment, the following are calculated:
- Average account balance
- Average income
- Spending behavior
- Credit usage
- Dormancy indicators

Purpose: Convert ML clusters into human-readable customer profiles.

---

### Step 5: Rule-Based Offer Recommendation
Each segment is mapped to a business action using predefined rules.

Segments and actions:
- High-Value Active Customers → Premium credit card & RM support
- Salary Earners with Low Spend → Cashback & spend-based offers
- Dormant Customers → Reactivation campaigns
- High Spend but Credit Risk → Credit limit monitoring
- Young / Student Customers → Entry-level cards & savings plans

Purpose: Make segmentation actionable.

---

### Step 6: Visualization & Insights
- Segment distribution analysis
- Segment-wise revenue potential (proxy)
- Business-friendly plots using matplotlib

---

## Final Output
Each customer record contains:
- Customer ID
- Segment Label
- Segment Description
- Recommended Offer

---

## Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/raghavpatidarr/customer-segmentation-banking.git
