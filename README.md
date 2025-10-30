Meta Ad Performance Analysis Dashboard 
<img width="1266" height="726" alt="Screenshot 2025-10-29 032527" src="https://github.com/user-attachments/assets/e610293c-7b7c-4ad9-b5fb-e3850574ba0f" />

Developed using Power BI & Excel

This project presents an **end-to-end analysis of Meta (Facebook & Instagram) ad campaigns**, providing deep insights into performance metrics, audience behavior, and optimization opportunities across multiple dimensions — **campaigns, platforms, demographics, time, and ad formats**.



Project Overview

The **Meta Ad Performance Dashboard** tracks the effectiveness of paid ad campaigns across the complete marketing funnel — **Awareness → Engagement → Conversion**.
It visualizes how well ads perform in terms of **reach, clicks, engagement, conversions, and ROI**, enabling data-driven decision-making for marketers and analysts.

**Objective:**
To help marketing teams monitor performance, identify leaks in the conversion funnel, and optimize ad spend for maximum ROI.



Tools & Technologies

* **Power BI:** Dashboard development, DAX measures, data modeling, and visual storytelling.
* **Microsoft Excel:** Initial data cleaning, validation, and structuring.
* **Data Modeling:** Star schema with one fact table and three dimension tables.


Data Model Structure

The data model follows a **Star Schema** design for efficient analytics and scalability:

| Table         | Type      | Description                                                             |
| ------------- | --------- | ----------------------------------------------------------------------- |
| **ad_events** | Fact      | Captures every user interaction (impression, click, comment, purchase). |
| **ads**       | Dimension | Ad-level metadata: platform, type, targeting, campaign linkage.         |
| **campaigns** | Dimension | Campaign details: duration, budget, objectives.                         |
| **users**     | Dimension | Demographics and interests of users engaging with ads.                  |

**Relationships:**
`ad_events → ads → campaigns` and `ad_events → users`
This structure supports cross-dimensional analysis (e.g., CTR by gender, ROAS by region, etc.).

---

Key KPIs Tracked

| KPI                           | Definition                                    | Formula                             |
| ----------------------------- | --------------------------------------------- | ----------------------------------- |
| **Impressions**               | Total times ads were shown                    | `COUNT(event_type = Impression)`    |
| **Clicks**                    | Number of times users clicked ads             | `COUNT(event_type = Click)`         |
| **Purchases**                 | Completed transactions after ad interaction   | `COUNT(event_type = Purchase)`      |
| **Engagements**               | Clicks + Shares + Comments                    | `SUM(Clicks + Shares + Comments)`   |
| **CTR (Click-Through Rate)**  | % of impressions that resulted in clicks      | `(Clicks ÷ Impressions) × 100`      |
| **Engagement Rate**           | % of impressions that resulted in engagements | `(Engagements ÷ Impressions) × 100` |
| **Conversion Rate**           | % of clicks that converted into purchases     | `(Purchases ÷ Clicks) × 100`        |
| **Purchase Rate**             | % of impressions resulting in purchases       | `(Purchases ÷ Impressions) × 100`   |
| **ROAS (Return on Ad Spend)** | Revenue per dollar spent                      | `(Total Revenue ÷ Total Budget)`    |

---

Dashboard Features

The Power BI dashboard contains **interactive visuals** that allow marketing teams to filter, explore, and interpret performance from multiple perspectives.

1. Funnel View**

* Tracks user journey: **Impressions → Clicks → Engagement → Purchase**.
* Helps detect major drop-off points in the funnel.

2. Gender & Age Analysis**

* **Donut Chart:** Engagement split by gender.
* **Bar Chart:** Performance across target age groups.
* **Insight:** Females (43%) and users aged **18–30** engage the most — ideal audience segment.

3. Geographic Insights**

* **Map Visualization:** Performance by country.
* High engagement: **India & Brazil**
* High-value markets: **Germany & UK**
* Recommendation: Run awareness ads in India/Brazil, premium conversion campaigns in UK/Germany.

4. Time & Seasonality**

* **Area Chart:** Hourly engagement peaks during **afternoon and evening** (15–20 hrs).
* **Calendar Heat Map:** Highlights campaign spikes on 19–21 & 25–27 (indicative of promos).
* Suggestion: Allocate budget to high-performing time slots.

5. Ad Format Performance**

| Ad Type      | Impressions | CTR   | Conversion Rate | Engagement Rate |
| ------------ | ----------- | ----- | --------------- | --------------- |
| **Video**    | 46K         | 11.9% | 5.2%            | 13.7%           |
| **Stories**  | 72K         | 11.8% | 5.2%            | 13.6%           |
| **Image**    | 51K         | 11.7% | 4.9%            | 13.5%           |
| **Carousel** | 48K         | 11.7% | 5.1%            | 13.4%           |

**Video** and **Story Ads** outperform others — ideal for future budget prioritization.

---

Key Insights & Findings

1. **High CTR (11.76%) and Engagement Rate (13.56%)** — strong creative and targeting performance.
2. **Low Purchase Rate (0.61%)** — funnel leakage from engagement to conversion.
3. **Audience:** Young females (18–30) dominate interactions.
4. **Best Ad Formats:** Video and Story ads.
5. **Optimal Timing:** Afternoon & evening.
6. **Geography Insight:**

   * **Volume:** India, Brazil
   * **Value:** Germany, UK

Recommendations

1. **Optimize landing pages** to reduce funnel drop-offs.
2. **Improve retargeting strategies** to convert high engagers.
3. **Personalize offers** for young female audiences.
4. **Shift more ad spend** toward **Video & Story formats**.
5. **Schedule ads** during high-performing time windows (15:00–20:00 hrs).
6. **Segment strategies** by geography for high-volume vs. high-value markets.

Business Objective

To enable data-backed decisions for marketing teams by:

* Tracking campaign performance across KPIs.
* Identifying effective audience segments.
* Evaluating platform (Facebook vs Instagram) efficiency.
* Optimizing ad spend to maximize ROI.

Visualization Summary

| Chart        | Visualization Type | Purpose                            |
| ------------ | ------------------ | ---------------------------------- |
| Gender       | Donut Chart        | Understand engagement by gender    |
| Age Group    | Bar Chart          | Identify most active audience      |
| Country      | Map                | Analyze performance by geography   |
| Calendar     | Heat Map           | Detect seasonality & promotions    |
| Weekly Trend | Stacked Column     | Compare weekly ad type performance |
| Hourly Trend | Area Chart         | Find optimal posting times         |
| Ad Type      | Matrix             | Compare platforms and ad formats   |

Dataset Summary

| Table         | Description                  | Example Fields                                |
| ------------- | ---------------------------- | --------------------------------------------- |
| **ad_events** | Interaction-level data       | `event_type`, `timestamp`, `user_id`, `ad_id` |
| **ads**       | Ad creative & targeting info | `ad_type`, `platform`, `target_age_group`     |
| **campaigns** | Budget & duration            | `total_budget`, `start_date`, `end_date`      |
| **users**     | Audience demographics        | `gender`, `age`, `country`, `interests`       |

Data Model Flow

```
users ─┐
        │
ad_events ─── ads ─── campaigns
        │
        └── demographics & engagement linkage
```

Conclusion

The **Meta Ad Performance Dashboard** demonstrates how **data analytics can uncover actionable marketing insights** by connecting campaign data with audience behavior.
Through detailed KPI tracking and visual storytelling, it empowers marketers to make smarter decisions about **budget allocation, ad creative, and targeting strategy**.

Developer Info

**Developed by:** Rakshit Naik
**College:** NIT Hamirpur (Electrical Engineering)
**Interests:** Data Analysis | UI/UX Design 
