**Customer Segmentation and Customer Lifetime Value (LTV) Prediction using RFM Analysis and Machine Learning**

**Project Overview**

This project focuses on analyzing customer purchasing behaviour using the **UCI Online Retail dataset**. The objective is to segment customers based on their buying patterns using **RFM Analysis** and **K-Means Clustering**, and then predict **Customer Lifetime Value (LTV)** using Machine Learning regression models.
The project demonstrates a complete end-to-end data analytics workflow, including data cleaning, feature engineering, exploratory data analysis, customer segmentation, and predictive modelling.


**Objectives**

- Clean and preprocess real-world e-commerce transaction data.
- Generate customer-level RFM (Recency, Frequency, Monetary) metrics.
- Perform Exploratory Data Analysis (EDA).
- Identify customer segments using K-Means Clustering.
- Interpret customer groups for business decision-making.
- Predict Customer Lifetime Value (LTV) using Machine Learning.
- Compare the performance of different regression models.


**Dataset**

Dataset: UCI Online Retail Dataset

The dataset contains transactional data of a UK-based online retail company, including:

- Invoice Number
- Stock Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country


**Technologies Used**

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Microsoft Excel


**Project Workflow**

```
Raw Online Retail Dataset
            │
            ▼
      Data Cleaning
            │
            ▼
   Revenue Calculation
            │
            ▼
      RFM Analysis
            │
            ▼
 Exploratory Data Analysis
(Histograms & Boxplots)
            │
            ▼
 Log Transformation
            │
            ▼
 StandardScaler
            │
            ▼
 Elbow Method
            │
            ▼
 K-Means Clustering
            │
            ▼
 Customer Segmentation
            │
            ▼
 Customer Lifetime Value Prediction
            │
            ▼
 Model Comparison
```


**Data Preprocessing**

The following preprocessing steps were performed:

- Removed missing Customer IDs
- Removed cancelled invoices
- Removed transactions with zero or negative quantities
- Removed transactions with zero or negative prices
- Removed duplicate records
- Converted Invoice Date to datetime format
- Created Revenue feature

---

**RFM Analysis**

Customer behaviour was summarized using:

- Recency (R): Days since the customer's last purchase.
- Frequency (F): Number of unique purchases made.
- Monetary (M): Total amount spent by the customer.

These three metrics formed the basis for customer segmentation.

---

**Exploratory Data Analysis**

EDA was performed using:

- Histograms
- Boxplots

The analysis identified:

- Right-skewed distributions
- Presence of outliers
- Need for preprocessing before clustering


**Data Transformation**

To improve clustering performance:

- Log Transformation (`np.log1p()`) was applied to reduce skewness.
- StandardScaler was used to standardize the RFM variables.


**Customer Segmentation**
Customer segmentation was performed using K-Means Clustering.
The optimal number of clusters was determined using the Elbow Method.
Four customer segments were identified:

- VIP Customers
- Loyal Customers
- Regular Customers
- At-Risk Customers


**Customer Lifetime Value (LTV) Prediction**

Three regression models were implemented:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

**Features Used**

- Recency
- Frequency
- Customer Segment

**Target Variable**

- Monetary Value (used as a proxy for Customer Lifetime Value)


**Model Evaluation**

Models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

**Model Comparison**

	Model            	MAE	          RMSE	         R2 Score
0	Linear Regression	1480.510421	  8209.916171	    0.34127
1	Decision Tree	    1985.318037	  12026.407768	 -0.41352
2	Random Forest	    1817.141503	  10571.481667	 -0.09220


Best Performing Model: Linear Regression

---

**Key Findings**

- Successfully cleaned and transformed the retail transaction data.
- Generated RFM metrics for 4,338 unique customers.
- Identified four meaningful customer segments using K-Means clustering.
- Customer segmentation provides actionable insights for personalized marketing.
- Linear Regression achieved the best performance for LTV prediction among the evaluated models.


**Business Applications**

- Customer Segmentation
- Personalized Marketing
- Customer Retention Strategies
- Loyalty Program Design
- Customer Lifetime Value Prediction
- Data-Driven Business Decision Making

**Future Scope**

- Use additional customer behavioural features to improve prediction accuracy.
- Apply advanced ensemble learning methods such as XGBoost or LightGBM.
- Develop an interactive dashboard using Power BI or Streamlit.
- Deploy the model as a web application for real-time customer analytics.

**Author**
Project Title: Customer Segmentation and Customer Lifetime Value (LTV) Prediction using RFM Analysis and Machine Learning

Developed as part of the Summer Internship Project (2026).
