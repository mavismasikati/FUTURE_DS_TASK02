# 📊 Customer Retention & RFM Segmentation Analysis
**An End-to-End Power BI Business Intelligence Solution**

---

## 📖 Project Overview
This project addresses a critical business challenge: a **74% customer churn rate**. Using **RFM (Recency, Frequency, Monetary) analysis**, I segmented **18.4K customers** to identify high-value "Champions" and develop targeted win-back strategies for "At Risk" segments.  

The interactive dashboards provide actionable insights for marketing, retention, and revenue optimization.

---

## 🛠️ Technical Implementation
- **Data Modeling:** Star Schema for optimized performance and cross-filtering.  
- **DAX Measures:** Custom calculations for RFM scoring, **Churn Rate %**, **Retention %**, and Active Customer trends.  
- **Data Visualization:** 4-page interactive dashboard covering **Demographics, RFM Segmentation, Customer Details, and Marketing Actions**.  

---

## 📈 Key Dashboard Insights
- **Customer Demographics:** 60% of total sales ($19.6M) come from customers aged **55-74**, highlighting the value of age-targeted marketing.  
- **RFM Segmentation:** Categorized 18K+ customers into **11 segments** (e.g., Champions, Loyalists, About to Sleep, At Risk).  
- **Churn Analysis:** Acquisition is strong (3.2K New Customers) but retention is weak, resulting in a **74% churn rate**.  

---


## 🧮 Key DAX Measures

**Churn Rate %**
```DAX
Churn Rate % =
VAR TotalCustomers =
    DISTINCTCOUNT(Customers[CustomerID])
VAR ChurnedCustomers =
    CALCULATE(
        DISTINCTCOUNT(Customers[CustomerID]),
        Customers[Status] = "Churned"
    )
RETURN
DIVIDE(ChurnedCustomers, TotalCustomers, 0)

## 📝 Conclusion
This project demonstrates how **data-driven insights** can improve customer retention and reduce churn. By analyzing key metrics, identifying high-risk customers, and understanding customer segments, businesses can **make informed decisions** to maximize revenue and loyalty.  
The dashboard provides a clear, interactive way to monitor performance over time and take actionable steps for growth.

## 📬 Contact
Interested in **leveraging your customer data to reduce churn and improve retention**? Connect with me on **GitHub** or **LinkedIn** to discuss insights and strategies.
