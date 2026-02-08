**RFM Analysis and Customer Segmentation on Olist E-Commerce Dataset**
---
**Description**

This Jupyter Notebook performs RFM (Recency, Frequency, Monetary) analysis and customer segmentation using the public Brazilian e-commerce dataset from Olist.
The main goal is to understand customer purchasing behavior through the three key RFM metrics, enabling data-driven marketing strategies such as loyalty programs, retention campaigns, win-back offers for at-risk customers, and targeted promotions for high-value segments.

**Key Steps in the Analysis:**

1.Data cleaning and merging of the three core datasets (orders, order items, and customers).
---
2.Calculation of RFM metrics:
---
  *Recency: Number of days since the customer's last purchase.*
  
  *Frequency: Total number of orders placed by each customer.*
  
  *Monetary: Total amount spent by each customer (product price + freight value).*

3.Customer segmentation using quantiles (e.g., 1–5 scoring) or simple business rules to classify customers into meaningful groups such as:
---
*Champions — recent, frequent, and high-spending customers*

*Loyal Customers / Potential Loyalists — consistent buyers with good potential*

*At Risk — previously valuable customers who have not purchased recently*

*New Customers, Promising, Lost / Hibernating, etc.*

4.Visualizations (Matplotlib & Seaborn) including RFM distributions, scatter plots, box plots per segment, and pie charts showing segment proportions.
   ---
5.Export of the final RFM table with segment labels to CSV (rfm_analysis_result.csv) for further use in BI tools, CRM systems, or additional modeling. 
  ---
This notebook is beginner-friendly for anyone learning e-commerce analytics and RFM analysis. The insights can directly support actionable recommendations such as personalized email/SMS campaigns, VIP rewards, re-engagement offers, and churn prevention.

Dataset
Sourced from the Brazilian E-Commerce Public Dataset by Olist on Kaggle:
---

*olist_orders_dataset.csv — order details (status, purchase timestamp, delivery dates)*

*olist_order_items_dataset.csv — items per order (price, freight value, product/seller info)*

*olist_customers_dataset.csv — unique customer information (customer ID, zip code prefix)*
