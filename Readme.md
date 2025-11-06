#  QuickBite Crisis Recovery Analysis

###  Data Analytics Project | Customer Retention | Operational Performance | Business Insights

**QuickBite** is a Bengaluru-based food-tech startup founded in 2020 that connects customers with nearby restaurants and cloud kitchens.  
In **June 2025**, QuickBite faced a major crisis due to a viral social media incident involving food safety violations and a week-long delivery outage during the monsoon season.  
The goal of this project is to **analyze the impact, identify recovery opportunities, and provide data-driven recommendations** to help QuickBite regain customer trust and market share.

---

##  Project Objectives

Imagining myself a Data Analyst , the following key areas are analyzed:

1. **Customer Segmentation** – Identified which customers can be recovered and which need new strategies.  
2. **Order Pattern Analysis** – Compared behavioral changes across pre-crisis, crisis, and post-crisis phases.  
3. **Delivery Performance** – Accessed delivery times, SLA compliance, and cancellation rates to uncover bottlenecks.  
4. **Restaurant Partnership Performance** – Evaluated restaurant recovery and predict long-term retention value.  
5. **Feedback & Sentiment Analysis** – Tracked customer satisfaction through ratings and sentiment trends.

---

## 📂 Datasets Used

| File Name | Description |
|------------|-------------|
| `fact_orders.csv` | Contains order-level information such as order IDs, timestamps, and payment types |
| `fact_order_items.csv` | Detailed items ordered per transaction |
| `fact_ratings.csv` | Customer feedback data (ratings and sentiment) |
| `fact_delivery_performance.csv` | Delivery partner performance metrics (actual_delivery_time_mins, expected_delivery_time_mins) |
| `dim_customer.csv` | Customer demographic and profile details |
| `dim_restaurant.csv` | Restaurant metadata including name, city, and cuisine type |
| `dim_delivery_partner_.csv` | Information about delivery partners |
| `dim_menu_item.csv` | Menu-level details for each restaurant |

---

##  Data Preparation & Cleaning

- Conducted **data profiling** and **quality checks** across all datasets.  
- Merged fact and dimension tables for unified analysis.  
- Handled missing values, inconsistent data types, and invalid entries.  
- Derived new metrics such as:
  - `recovery_pct` – % recovery in post-crisis vs pre-crisis orders
  - `sla_met` – service-level agreement compliance
  - `delivery_delay` – delay in minutes between expected and actual delivery
  - `customer_segment` – (Lost, New, Loyal) based on order frequency and recency
  - `phase` - based on the time when crisis occur

---

## Exploratory Data Analysis (EDA)

###  Customer Segmentation
- **Pre-crisis customers:** 70,358  
- **Crisis customers:** 7,141  
- **Post-crisis customers:** 22,524  
- **Lost customers:** 76.35%  
- **Loyal customers:** 1.13%  
- **New customers:** 22.52%  

**Recommendations:**
-  Reward loyal customers with loyalty bonuses.  
-  Run re-engagement campaigns for lost users.  
-  Offer welcome discounts for new users.  

---

###  Order Pattern Insights
- The **average order value (AOV)** remained stable (~₹340 per order).  
- **Customer-level spending** increased from ₹460 to ₹560 post-crisis — indicating only high-value users stayed active.  
- **Primary issue:** Drop in number of active customers and total orders, not the spend amount.  

---

###  Delivery Performance

| Phase | SLA Compliance | Avg Delay (mins) | Insights |
|-------|----------------|-----------------|-----------|
| Pre-crisis | 43.6% | Moderate | Acceptable for a scaling startup |
| Crisis | 11.8% | ~18 mins | Heavy monsoon + outage → collapse |
| Post-crisis | 12.4% | Slightly better | Needs major improvement |

**Key Takeaway:**  
SLA compliance is still 70% below pre-crisis levels — indicating urgent need for delivery infrastructure optimization.

---

###  Cancellation Trends

| Phase | Cancellation Rate |
|--------|-------------------|
| Pre-crisis | 1.7% |
| Crisis | 3.3% |
| Post-crisis | 3.6% |

Cancellations remained relatively low overall, suggesting that those who did order, mostly completed them.  
However, the slight increase post-crisis shows persistent confidence issues among customers.

---

###  Restaurant Performance

- Classified restaurants based on **recovery percentage** and **city-wise comparison**:
  - **Reactivated / New**
  - **Strong Recovery**
  - **Moderate Recovery**
  - **Declining / At Risk**

**Key Insight:**  
A large share of restaurants in major metros (like Bengaluru and Kolkata) showed moderate recovery, but smaller cities saw more “Declining / At Risk” cases — implying uneven recovery across geographies.

---

### Feedback & Sentiment

- Average rating and sentiment dropped sharply during the crisis phase.  
- Positive correlation between sentiment and SLA compliance.  
- Post-crisis recovery in sentiment was limited — indicating trust rebuilding is ongoing.

---

##  Tools & Libraries

- **Python**
  - pandas, numpy
  - matplotlib, seaborn
- **Jupyter Notebook**
- **Excel for dashboarding**

---

## Key Visualizations

- Customer segmentation distribution 
- City-wise restaurant recovery 
- Phase-wise SLA compliance 
- Cancellation rate trend 
- Average sentiment and rating trend 
- Top restaurants based on total revenue

---

## Business Recommendations

1. **Customer Retention:**
   - Implement loyalty programs and re-engagement campaigns.  
   - Personalized offers to win back inactive users.  

2. **Operational Improvements:**
   - Strengthen delivery partner network to improve SLA.  
   - Introduce real-time order tracking and refund transparency.  

3. **Restaurant Strategy:**
   - Prioritize strong recovery partners for visibility.  
   - Provide compliance and food safety training to at-risk partners.  

4. **Brand & Trust Rebuilding:**
   - Launch social media campaigns emphasizing new safety protocols.  
   - Highlight positive customer feedback in marketing efforts.  

---
