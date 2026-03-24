# FUTURE_DS_TASK02
Analyzed 18.4K customers with Power BI and RFM segmentation, revealing a 74% churn rate and high-value segments. Built interactive dashboards with DAX measures, providing actionable insights for retention, revenue growth, and targeted marketing strategies.

# 📊 Customer Retention & RFM Segmentation Analysis
**An End-to-End Power BI Business Intelligence Solution**

---

## 📖 Project Overview
This project addresses a critical business challenge: a **74% customer churn rate**. By implementing **RFM (Recency, Frequency, Monetary) analysis**, I segmented a database of **18.4K customers** to identify high-value "Champions" and develop targeted win-back strategies for "At Risk" segments. The dashboards provide actionable insights for marketing and business strategy.

---

## 🛠️ Technical Implementation
- **Data Modeling:** Designed a **Star Schema** to optimize report performance and cross-filtering.  
- **DAX Measures:** Developed custom measures for **RFM scoring, Churn Rate %, Retention %, and Active Customer trends**.  
- **Data Visualization:** Created a **4-page interactive Power BI dashboard** focusing on Demographics, RFM Segmentation, and Prescriptive Marketing Actions.

---

## 📈 Key Dashboard Insights
- **Customer Demographics:** Customers aged **55-74** contribute **60% of total sales ($19.6M)**, highlighting the value of age-targeted marketing.  
- **RFM Analysis:** Categorized 18K+ customers into **11 distinct segments** (e.g., Champions, Loyalists, About to Sleep, At Risk).  
- **The “Churn Signal”:** Acquisition is strong (3.2K New Customers) but retention is weak, resulting in a **74% churn rate**.

---

## 💡 Business Recommendations
**Champions (VIP Treatment):**  
- Loyalty program with early access to new products to protect the highest revenue stream.  

**At Risk (Win-Back):**  
- Automated re-engagement email campaigns with personalized discounts for customers who haven't purchased in 90+ days.  

**New Customers (Onboarding):**  
- A "Welcome Series" to encourage a second purchase within 30 days, increasing conversion to the "Promising" segment.  

**About to Sleep:**  
- Reminder emails or SMS campaigns with urgency messaging to retain customers before they churn.

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

Retention Rate % =
VAR TotalCustomers =
    DISTINCTCOUNT(Customers[CustomerID])
VAR ActiveCustomers =
    CALCULATE(
        DISTINCTCOUNT(Customers[CustomerID]),
        Customers[Status] = "Active"
    )
RETURN
DIVIDE(ActiveCustomers, TotalCustomers, 0)


