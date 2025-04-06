# Customer Segmentation using Clustering Techniques

This project transforms a **transactional dataset** into a **customer-centric analytical model** using clustering and segmentation techniques. The goal is to uncover meaningful insights into customer behavior to aid strategic decision-making in marketing and operations.


## Objective

To group customers based on behavioral patterns like spending, recency, and frequency using **unsupervised machine learning**, enabling businesses to create personalized experiences.


##  Dataset Overview

- **Type:** E-commerce transactional data  
- **Features:**  
  `CustomerID`, `InvoiceDate`, `Quantity`, `Price`, `Country`, etc.  
- **Derived Metrics:**  
  `TotalSpent`, `Recency`, `Frequency`, `Monetary`, `Trend Slope`


## Project Pipeline

### 1. Data Preprocessing
- Cleaned nulls, duplicates
- Created customer-level features (RFM, trend)
- Handled outliers using **Isolation Forest**
- Converted dataset from transaction-based to **customer-centric**

### 2. Feature Scaling & PCA
- Standardized features using **StandardScaler**
- Applied **PCA** for dimensionality reduction
- Selected `n_components = 6` capturing ~90% of variance

### 3. Clustering & Evaluation
- Applied **KMeans clustering**
- Determined optimal `k = 3` using:
  - Elbow Method (WCSS)
  - Silhouette Score
- Labeled clusters and analyzed distribution

### 4. Customer Segmentation
- Segmented customers into:
  - High Value Loyalists
  - Occasional Buyers
  - At-Risk Customers
- Visualized segments and behavior

## Technologies Used

- Python 3.x  
- Libraries:  
  `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `yellowbrick`, `scipy`

## Key Results

- **3 customer segments** identified:
  - Segment 1: High Recency, High Spending — Loyal  
  - Segment 2: Moderate Frequency, Low Spend — Occasional  
  - Segment 3: Infrequent, Low RFM — Churn Risk  
- Ready for actionable strategies:
  - Loyalty programs
  - Re-targeting ads
  - Promotions and offers

## Future Improvements

- Add demographics and web behavior data
- Try **DBSCAN / Agglomerative Clustering**
- Build a **dashboard (Streamlit / Power BI)** for business users


