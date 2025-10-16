# 🚴‍♀️ Ecobici 2023 Data Challenge  

### 🌎 Project Overview  
**Ecobici** is the public bicycle-sharing system of **Buenos Aires, Argentina**, offering more than **4,000 bikes** and **471 stations** across the city.  
This project analyzes Ecobici’s 2023 operations to provide insights that can help the company achieve its goal of **increasing bike usage and station adoption by 18%** in 2024.  

Through a detailed analysis of millions of trips, this project explores **when**, **where**, and **how** residents use the bikes, uncovering opportunities for improvement in **operations**, **user experience**, and **data modeling**.  

> 📊 Full presentation of findings available here:  
> [🎥 **Ecobici 2023 - Pedaling Towards Success (PDF)**](Ecobici%202023%20Challenge.pdf)

---

### 🎯 Objective  
To identify data-driven strategies that enable Ecobici to reach its **18% adoption growth goal** by:  
- Understanding temporal and spatial usage patterns.  
- Improving bike availability and repair coverage.  
- Analyzing user retention and engagement trends.  
- Enhancing the overall user experience through data-informed product ideas.

---

### 🧾 Dataset  
Open dataset provided by the **City of Buenos Aires**:  
> [https://data.buenosaires.gob.ar/dataset/bicicletas-publicas](https://data.buenosaires.gob.ar/dataset/bicicletas-publicas)

#### Data Highlights  
- **2.6 million total rides** in 2023  
- **212,000 unique users**, representing all riders with at least one trip  
- **Average ride duration:** 23 minutes  
- **Average rides per week:** 50,400  
- **Average rides per user per year:** 12  

> ⚠️ *Note:* The dataset was cleaned to handle inconsistencies (e.g., missing data, invalid timestamps).  

---

### 🔍 Analytical Approach  

#### 1. **Temporal Analysis – When does Buenos Aires pedal?**
- Peak usage occurs in **March, October, and November** (warmer months).  
- **Weekdays dominate** usage — especially **Wednesdays (18%)**.  
- **Rush hours (4–7 PM)** account for **26%** of total rides.  

#### 2. **Spatial Analysis – Where does Buenos Aires pedal?**
- Nearly **10% of all rides** start at just **10 stations**, indicating network concentration.  
- **82% overlap** between top starting and ending stations — showing consistent high-traffic hubs.  
- Trending stations (with the largest MoM increase) show only **66% overlap**, revealing emerging demand areas.  

#### 3. **Operational Opportunities**
##### 🧰 Repair Points  
- **17 repair points** currently serve **471 stations** — averaging **27 stations per repair point**.  
- Some repair points cover up to **59 nearby stations**, creating service imbalance.  
- **Once** and **Parque Rivadavia** identified as ideal locations for **new repair hubs**, with **35K trip starts** and **84% higher demand** than the next most active area.

##### 🚲 Bike Redistribution  
- Estimated **4K bikes** across **8.5K parking spots** — meaning ~**50% of spots remain empty**.  
- Modeled a **20-minute peak-demand window** to evaluate bike sufficiency.  
- Recommended dynamic repositioning based on **origin–destination and peak-hour demand** patterns.  

#### 4. **User Behaviour and Retention**
- Dataset lacks **user IDs**, limiting lifecycle tracking.  
- Based on sample estimations:  
  - **Low retention:** Only **17%** of users continue riding after 6 months.  
  - **High churn:** Over **70%** are one-time users.  
- Proposed redesign of data model to include:  
  - `user_id` for activity tracking  
  - `bike_id` and `status` for usage and maintenance analytics  
  - Event logging for **activation, retention, and churn** metrics  

#### 5. **User Experience Opportunities**
Proposed data-driven product features to improve engagement and adoption:
- **Smart Station Filtering:** Suggest nearest stations with most available bikes.  
- **Bike Availability Alerts:** Notify users when favorite stations reach desired stock.  
- **Multimodal Integration:** Combine Ecobici rides with bus/subway schedules.  
- **Gamified Rewards:** Points, badges, and challenges to boost ride frequency.  
- **Fitness Integration:** Connect ride data with health apps.  
- **Guided Tours & Virtual Onboarding:** Enhance user engagement and onboarding.  

---

### 📈 Key Findings Summary  

| Dimension | Insight | Recommendation |
|------------|----------|----------------|
| **Temporal** | Usage peaks in warmer months and weekdays | Focus maintenance and redistribution during March–Nov and weekday evenings |
| **Spatial** | 10 stations handle ~10% of all rides | Expand capacity and add new stations in high-demand zones |
| **Operational** | Repair and redistribution coverage unbalanced | Add repair hubs in Once & Parque Rivadavia; dynamic rebalancing model |
| **User Retention** | Only 17% retention; 70% one-timers | Implement cohort tracking and user ID linking |
| **Experience** | Limited personalization | Introduce alerts, gamification, and multimodal features |

---

### 🧠 Conclusions  

To achieve an **18% increase in adoption**, Ecobici should act on **three pillars**:

1. **Bike Availability**  
   - Ensure stock during weekday afternoons and warmer months.  
   - Monitor redistribution efficiency during peak demand windows.

2. **User Experience**  
   - Incorporate new app features that increase engagement and satisfaction.  
   - Introduce personalized alerts, gamification, and integration with other transport modes.

3. **Data Model Enhancement**  
   - Include `user_id`, `bike_id`, and event tracking.  
   - Enable lifecycle, segmentation, and retention analysis for future growth.  

---

### 🛠️ Tech Stack  
- **Python (Jupyter Notebook)** – analysis and visualization  
- **pandas / numpy** – data manipulation  
- **matplotlib / seaborn / plotly** – data visualization  
- **geopandas / folium** – geospatial mapping  
- **Excel / CSV** – data import and preprocessing  

