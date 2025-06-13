# R-Food Delivery & Ride Hailing-Forecasting Demand-Marketplace Optimization 
Forecasted demand and optimized investment strategy for GrabFood Vietnam using regression and time series modeling. Identified high-performing merchant categories and proposed actionable reallocations to improve booking efficiency and GMV growth.

# 📦 Grab Vietnam – Demand Forecasting & Investment Optimization

This project analyzes marketplace performance data for GrabFood Vietnam, aiming to identify booking drivers, evaluate investment efficiency across merchant categories, and forecast demand for strategic planning. The analysis supports the Marketplace Strategy team with insights to optimize ROI, especially during volatile weeks.
![image](https://github.com/user-attachments/assets/36868f07-576d-49cf-b15a-bb089cdfe9f5)

---

## 🎯 Project Goals

- Understand booking trends and week-over-week fluctuations
- Evaluate ROI by merchant category (A1–A4)
- Forecast GMV and spending for the next 6 weeks
- Recommend tactical actions to improve performance and efficiency

---

## 📊 Data Overview

![image](https://github.com/user-attachments/assets/0fa61c20-0b04-49a2-a36d-7ee07f7b963c)

- **Source**: Internal Grab Vietnam weekly performance data
- **Duration**: 6 weeks
- **Key Metrics**:
  
![image](https://github.com/user-attachments/assets/73795a9c-7fb2-468a-a297-aa225e287c28)
  - Booking orders
  - GMV (Gross Merchandise Value)
  - Spend per merchant category
  - Active merchant count, CPBO, fulfillment rate

## Data after cleaning
![image](https://github.com/user-attachments/assets/5f6b6eb0-e40b-4e24-be29-98f07a52d8cd)

---

## 🧠 Approach
Analysis Structure in R Studio
![image](https://github.com/user-attachments/assets/32fa771a-f010-42eb-ab64-ae366f99c4a4)

## Overview of GMV contribution and budget allocation
![image](https://github.com/user-attachments/assets/43ea3710-ccd4-46a6-882b-5cba0fab7b1b)
![image](https://github.com/user-attachments/assets/c6c980f9-8c8f-4436-82ce-35437cba69b4)

### 1. Exploratory Analysis
- Weekly summaries using pivot tables
- Spend and GMV breakdown by category
- Fulfillment trends and CPBO distribution
  
![image](https://github.com/user-attachments/assets/be5dfe43-2a58-4ba7-b53b-f1be51b663e0)

- Observation & Summary on percentage of change of each metric and how it drive the performace by category and by the last 3 weeks
- Targeted segment
- 
![image](https://github.com/user-attachments/assets/105ded44-5b39-46e7-8d6e-be7fa25401ad)

![image](https://github.com/user-attachments/assets/cdc3baf7-d20c-43e6-87c7-7b2013b1e2c3)

-Logic tree to identify growth levers for Grabfood :

![image](https://github.com/user-attachments/assets/056af489-2bf0-4b1f-8e0e-15f430a07283)


### 2. Correlation & Regression
- Built a correlation matrix to identify significant variables and also to check multicollinear of each variables
- Applied multiple linear regression to estimate the impact of spend and category mix on bookings 
![image](https://github.com/user-attachments/assets/e948f5fc-7f71-4bd6-b001-238276383f21)

- Validation. Fine-tunethe  regression model with a categorical variable
  
![image](https://github.com/user-attachments/assets/a6c8136f-fa58-402f-925d-69057f54bc9c)

![image](https://github.com/user-attachments/assets/58390267-ca06-43e5-a147-b75605b75ae9)

![image](https://github.com/user-attachments/assets/f792ed71-f145-46f2-8450-426a841bb4d2)

- Key finding: **Spend allocation matters more than spend volume**
  
- Category A3 is the most significant positive driver of booking orders, with an estimated uplift of +461,500 bookings compared to baseline (A1).
- Category A2 and A4 show strong negative impacts on bookings, reducing performance by -136,400 and -454,700 bookings respectively
- Total Spend itself is not statistically significant, suggesting that where we allocate budget (category selection) matters more than simply increasing spend
- The model explains 99.9% of booking variance, indicating a very strong and reliable fit for strategic forecasting
- Actionable Strategy: Reallocate investment toward Category A3 to drive maximum booking growth, while optimizing or limiting spending on Categories A2 and A4



### 3. Forecasting
- Compared ARIMA and regression-based approaches

![image](https://github.com/user-attachments/assets/436a9c34-79ce-4b41-a790-b166f4a595e7)

- >> Multi Regression Model can explain 99.6% (R-Square), better than the AIRMA

- Generated 6-week forecasts for GMV and spend
  - Key metrics change adjustment + budget reallocation plan structure:
  ![image](https://github.com/user-attachments/assets/de815ae1-cebd-4aa6-802f-78ce1df07df7)

  ![image](https://github.com/user-attachments/assets/0ec8b36b-d602-4a47-be33-8be7be0e36c5)

- Ran scenario-based simulations to test reallocation impact
  - Baseline Scenario (Without budget reallocation):
  ![image](https://github.com/user-attachments/assets/5f3c065b-641b-4d35-8f68-7a98d1724fb3)

  - Optimized Reallocation Scenario (With budget reallocation):
  ![image](https://github.com/user-attachments/assets/fd7ae8d6-7c28-407d-a449-9711f2f396bd)

---

## 🔍 Key Insights

| Metric | Insight |
|--------|---------|
| 📈 **Category A3** | Drives the highest incremental bookings (+461K) |
| 📉 **Category A2 & A4** | Negative impact on overall bookings |
| 💸 **Total Spend** | Not statistically significant on its own |
| 🔄 **Spend Allocation** | Major lever to influence booking efficiency |

---

## 📌 Strategic Recommendations

**Reallocate spend toward Category A3**  
→ Focus on merchants with high fulfillment rates and strong AOV  
→ Pause inefficient campaigns in A2/A4  

**Merchant Activation Strategy**  
→ Target dormant or underperforming merchants  
→ Use customized promotions and bundles to lift order value  

**Improve Operational Metrics**  
→ Launch training and benchmarks for fulfillment improvement  
→ Partner with top 10% merchants for exclusive incentives

---

## 📦 Extra Growth Analytics Frameworks:

- Growth tree:
![image](https://github.com/user-attachments/assets/2bbc83eb-9c5c-4237-a474-bca545bd8347)

- Ansoff Matrix & BCG Matrix to find our position & prioritization in the market:
![image](https://github.com/user-attachments/assets/9a942854-4154-4733-b2c2-de443f459050)

- E-commerce Optimization Strategy:
![image](https://github.com/user-attachments/assets/1ab91d2a-08cd-411c-a9d4-abead9388ad2)

- Optimization Framework for online sales channels:
![image](https://github.com/user-attachments/assets/f2ee274b-c8ab-4dfb-bd35-5806fe7da6b1)

- Data Analytics Execution Loops:
![image](https://github.com/user-attachments/assets/d6a1aac3-bf97-4eff-83df-773900c9fe71)

----

