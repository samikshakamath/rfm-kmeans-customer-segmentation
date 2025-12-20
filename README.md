# Behavioral Segmentation of Retail Customers Using RFM, PCA & K-Means Clustering

 - **Author**: Samiksha Kamath 
- **Project Date**: 3/3/2025


This repository presents a **data-driven customer segmentation study** based on transactional data from a national convenience store chain.  
The project applies **unsupervised learning, RFM analysis, and dimensionality reduction** to identify distinct customer segments and translate them into **actionable marketing strategies**.

Rather than treating customers as a homogeneous base, the analysis focuses on **behavioural differentiation**, enabling targeted retention, loyalty, and revenue optimisation initiatives.

---

## Business Objective

The primary objective of this project is to:

- Segment customers based on **spending behaviour, visit frequency, and product preferences**
- Identify **high-value** and **at-risk (churning)** segments
- Support **targeted marketing, pricing optimisation, and personalised engagement**

The analysis is designed for **strategic decision support**, not real-time prediction.

---

## Dataset Overview

- **Domain:** Retail / convenience store transactions  
- **Time horizon:** 6 months  
- **Customers:** ~3,000  
- **Data sources:**
  - Customer summary table
  - Category-level spend table (20 product categories)
  - Basket-level transactions
  - Line-item purchase data

Each table was integrated to construct a **holistic behavioural view** of each customer.

---

## Data Cleaning and Preparation

Extensive preprocessing was performed to ensure analytical validity:

### Key Cleaning Steps
- Removal of duplicate records (114 line-item duplicates)
- Conversion of currency fields (e.g. `"£"`) to numeric format
- Handling of negative quantities and spend values (refunds / corrections)
- Conversion of purchase timestamps to datetime format
- Verification of missing values (no nulls across core tables)

These steps ensured consistency across transactional, basket-level, and customer-level views.

---

## Feature Engineering

A rich set of behavioural features was engineered, including:

### Spending and Volume
- Total spend
- Total quantity purchased
- Spend per unique visit
- Average basket value

### Frequency and Regularity
- Visit frequency ratio
- Average items per visit
- Temporal purchase patterns

### Category-Level Behaviour
- Spend across essential, non-essential, and occasional categories
- Purchase diversity across product groups

### RFM Metrics
- **Recency:** Days since last visit
- **Frequency:** Number of visits
- **Monetary:** Total spend

Log transformation was applied to right-skewed spend variables, followed by **standardisation** to ensure balanced feature contribution.

---

## Dimensionality Reduction

### Principal Component Analysis (PCA)

PCA was applied to reduce dimensionality while preserving behavioural structure:

- **PC1:** 52.03% variance explained
- **PC2:** 30.65% variance explained
- **Total (PC1 + PC2):** 82.87%

The first two components captured overall spending intensity, visit frequency, and purchase volume, enabling efficient clustering without significant information loss :contentReference[oaicite:1]{index=1}.

---

## Segmentation Methodology

### Clustering Algorithm
- **K-Means clustering**

### Model Selection
- Elbow Method
- Silhouette Score

An optimal cluster count of **k = 5** was selected, balancing interpretability and cluster separation  
(Silhouette score ≈ 0.317).

Cluster centroids were reverse-transformed (PCA, scaling, log) to enable **business-readable profiles**.

---

## Customer Segments Identified

### Segment 1: High Value Consumers
- Highest spend and frequency
- Broad category engagement
- Strong presence in both essential and discretionary items
- Primary revenue drivers

### Segment 2: Occasional Shoppers
- Infrequent visits
- Moderate, irregular spending
- Convenience- and impulse-driven behaviour

### Segment 3: Churning Customers
- Previously high value
- Sharp decline in visit frequency
- High spend per visit but low engagement
- High risk of revenue loss

### Segment 4: Frequent Buyers
- High visit frequency
- Low spend per visit
- Budget-conscious, essentials-focused

### Segment 5: Loyal Consumers
- Stable, predictable behaviour
- Moderate frequency and spend
- Balanced category engagement

RFM analysis validated and refined these segments.

---

## Key Insights

- Revenue is highly concentrated among **High Value Consumers**
- **Churning Customers** still exhibit high spend per visit, indicating recoverable value
- Frequent Buyers provide stability but lower margins
- Occasional Shoppers are unreliable for consistent revenue

This segmentation highlights where **retention efforts yield the highest ROI**.

---

## Marketing Strategy Recommendations

### Focus Segments
- **High Value Consumers**
- **Churning Customers**

#### High Value Consumers
- Threshold-based free delivery
- Premium membership / VIP programs
- Cross-selling and upselling
- Early access to seasonal and exclusive products

#### Churning Customers
- Urgency-driven comeback offers
- Targeted category discounts
- Omnichannel retargeting (email, SMS, ads)
- Subscribe-and-save programs for essentials

These strategies align directly with observed behavioural patterns.

---

## Tools and Techniques

- **Python**: Data processing and analysis
- **Pandas / NumPy**: Feature engineering
- **Scikit-learn**: PCA and K-Means clustering
- **Matplotlib / Seaborn**: Visual exploration
- **Jupyter Notebook**: Analytical workflow

---

