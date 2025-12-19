# Behavioral Segmentation of Retail Customers Using RFM, PCA & K-Means Clustering

 - **Author**: Samiksha Kamath 
- **Project Date**: 3/3/2025


## Objective

This project conducts a data-driven segmentation analysis on a national convenience store's customer base. Using **RFM metrics**, **Principal Component Analysis (PCA)**, and **K-Means clustering**, the goal is to identify actionable customer segments to enhance marketing personalization, retention, and revenue optimization.

---

## Key Analytical Techniques

- **RFM Analysis** – Classifying customers based on Recency, Frequency, and Monetary value  
- **Feature Engineering** – Extracting behavioral indicators like category affinity, spend trends, and basket dynamics  
- **PCA** – Reducing dimensionality while preserving 82.87% of total variance  
- **K-Means Clustering** – Segmenting customers into five meaningful clusters  
- **Silhouette Analysis** – Determining optimal cluster quality (k=5 selected, score: 0.317)

---

## Segmentation Insights

| Segment             | % Base | Characteristics                                       |
|---------------------|--------|--------------------------------------------------------|
| High-Value          | 29.6%  | High frequency and diverse category engagement         |
| Frequent Buyer      | 24.8%  | Regular, low-to-moderate spenders                      |
| Loyal Customer      | 22.2%  | Balanced, dependable with strong brand affinity        |
| Occasional Spender  | 14.9%  | Infrequent, selective buyers with low purchase volume  |
| Churning Customer   | 8.4%   | High past value but sharply declining activity         |

---

## Methodology Overview

1. **Data Cleaning**: Removed duplicates, handled invalid entries, and standardized formats  
2. **Feature Transformation**: Applied log transforms and StandardScaler to normalize skewed data  
3. **Dimensionality Reduction**: PCA selected to retain interpretability and reduce overfitting risk  
4. **Clustering**: K-Means applied to PCA components with silhouette validation  
5. **Customer Profiling**: Reverse-transformed clusters to build real-world pen profiles

---

## Strategic Recommendations

- **Retain High-Value Customers** via premium memberships, cross-selling, and exclusive access
- **Re-engage Churning Customers** using urgency-based offers and personalized retargeting
- **Upsell Frequent Buyers** with threshold-based rewards and curated product bundles
- **Personalize Marketing** through segment-specific messaging and campaign design
- **Future Work**: Integrate CLV prediction, churn modeling, and seasonal behavior analysis

---

## Tools & Libraries Used

- Python (Pandas, NumPy, scikit-learn, Matplotlib, Seaborn)  
- Jupyter Notebook  
- Data: Customer transactions, category spends, baskets, and line items

This project demonstrates the power of combining business acumen with analytical modeling for precise and effective customer segmentation.

