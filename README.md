#  Shopee Business Intelligence Case Study  
**Role Target:** Data Analyst – SG Business Intelligence (Fresh Graduate Role)

---

## 📈 View Dashboard  
 [**View on Tableau Public**](https://public.tableau.com/app/profile/samantha.yoong/vizzes)
 
---

## 📈 Problem Statement
Shopee SG’s marketing team noticed **flat campaign ROI** and **declining seller engagement** in monthly promotions despite increased budget allocation.  

**Key Issues Identified:**
- Sellers opted out of campaigns due to **low visibility or unclear ROI**.  
- **Manual reporting** across BD, Ops, and Marketing caused delays in decision-making.  
- Stakeholders lacked a **single source of truth** for performance metrics.  

**Goal:** Identify bottlenecks in seller campaign performance, automate reporting, and provide actionable insights to **improve ROI and seller retention**.

---

## 📈 Approach

###  Data Scoping & Cleaning
- Pulled **6 months of campaign data** using **SQL** (tables: seller performance, campaign participation, voucher usage, transaction logs).  
- Cleaned and joined datasets (handled nulls, normalized seller IDs, removed duplicates).  

```sql
SELECT seller_id, campaign_id, SUM(gmv) AS total_gmv, COUNT(order_id) AS orders
FROM campaign_orders
WHERE order_date BETWEEN '2024-01-01' AND '2024-06-30'
GROUP BY seller_id, campaign_id;
```
##   Automated Reporting Pipeline
- Built **SQL script** to refresh weekly metrics (GMV, CTR, voucher redemption).  
- Exported summary to **Google Sheets** for teams and created **Tableau dashboard** for real-time monitoring.  

---

##   Funnel & Cohort Analysis
- Mapped seller journey: `Campaign Invite → Sign-Up → Campaign Participation → GMV uplift → Post-campaign retention`.  
- Segmented sellers into **top performers, mid-tier, and drop-offs** to identify churn points.  

---

##   Cross-Functional Collaboration
- Partnered with **BD** for seller segmentation, **Marketing** for campaign messaging, and **Ops** for logistics alignment.  
- Designed reporting flow from **backend (SQL)** → **processing layer** → **frontend (Tableau)**.  

---

## 📈 Insights & Findings
- **Insight 1:** Mid-tier sellers drove **55% of campaign GMV** but had **30% churn** after 2 campaigns.  
  ➡️ Needed clearer ROI proof and stronger incentives.  

- **Insight 2:** Campaign participation dropped by **18%** when onboarding emails lacked performance benchmarks.  
  ➡️ Communication gaps impacted seller trust.  

- **Insight 3:** Manual reporting consumed **5 hours/week per analyst**.  
  ➡️ Automation reduced this to **15 minutes**.  

- **Insight 4:** GMV uplift peaked when voucher usage was **25–40%**, but beyond **60%** caused **profit erosion**.  
  ➡️ Identified the optimal discount sweet spot.  

---

## 📈 Recommendations & Impact
➡️ **Seller Segmentation Strategy**  
- Tiered incentives (e.g., bonus ad credits for mid-tier sellers) to reduce churn.  

➡️ **Data-Driven Communication Templates**  
- Added **performance snapshots** in seller emails → participation projected to rise **12%**.  

➡️ **Automated BI Stack**  
- Automation cut reporting time by **80%**, enabling near real-time decision-making.  

➡️ **Interactive Tableau Dashboard**  
- Visualized GMV by seller tier, churn prediction, voucher ROI heatmap → used by BD & Marketing in weekly reviews.  

** Expected Results:**
- **+15%** campaign participation next quarter.  
- **+8–10%** GMV uplift without higher discount spending.  
- **5× faster** reporting cycle.  

---

## 📈 Tools & Skills Demonstrated
- **SQL** – Data extraction, transformation, cohort analysis.  
- **Tableau** – Visualization & stakeholder dashboards.  
- **Excel/Google Sheets** – Ad-hoc reporting & presentation prep.  
- **Business Storytelling** – Translated complex data into actionable insights.  

---

## 📈 Role Fit
- **Cross-functional work:** Partnered with BD, Marketing, and Ops.  
- **Technical depth:** SQL, Excel, Tableau.  
- **Business impact:** Linked insights directly to **ROI & seller retention**.  
- **Clear storytelling:** Data → insights → actions → measurable impact.  
