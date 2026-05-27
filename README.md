# GoodCabs Performance Analysis 🚖📊

---

# Overview

GoodCabs is a rapidly growing cab service company operating across tier-2 cities in India. The company focuses on empowering local drivers while providing affordable and reliable transportation services.

As the company expanded, management wanted to analyze:

- Trip growth across cities
- Revenue generation patterns
- Passenger retention behavior
- Repeat customer trends
- Target achievement performance
- Passenger and driver satisfaction

This project was developed to convert raw operational data into meaningful business insights using SQL, Power BI, and data analytics techniques. The system helps management make data-driven decisions for improving operational efficiency, customer retention, and overall business growth.

---

# Business Problem

GoodCabs had multiple operational challenges:

- Some cities were performing significantly better than others
- Passenger repeat rates varied across locations
- Several monthly business targets were not being achieved
- Revenue growth patterns were inconsistent
- Management lacked a centralized analytical reporting system

To solve these problems, a complete analytical system was designed using:

- Database Management System (DBMS)
- SQL Views
- Stored Procedures
- Database Functions
- Power BI Dashboards

The objective was not only to analyze data but also to create actionable business intelligence.

---

# Project Objectives

The main objectives of this project were:

✅ Analyze city-wise trip performance  
✅ Measure revenue generation trends  
✅ Evaluate target achievement status  
✅ Study repeat passenger behavior  
✅ Understand customer satisfaction trends  
✅ Identify high-performing and underperforming cities  
✅ Build interactive dashboards for decision-making  
✅ Create reusable SQL procedures and functions for automation  

---

# Why This Project Matters

Cab service businesses depend heavily on:

- Customer retention
- Operational efficiency
- Dynamic demand management
- Service quality
- Driver performance
- Pricing optimization

A small improvement in repeat customers or trip conversion can significantly improve long-term profitability.

This project helps management identify:

- Which cities require operational improvement
- Which cities generate maximum revenue
- How passenger loyalty affects business growth
- What strategies can improve customer retention

---

# Dataset Overview

The database consists of 8 interconnected tables designed using relational database principles.

| Table Name | Purpose |
|---|---|
| `fact_trips` | Stores detailed trip-level data |
| `dim_repeat_trip_distribution` | Stores repeat trip frequency data |
| `fact_passenger_summary` | Monthly passenger summary |
| `dim_date` | Date and calendar information |
| `dim_city` | City information |
| `city_target_passenger_rating` | Passenger rating targets |
| `monthly_target_new_passengers` | Monthly passenger targets |
| `monthly_target_trips` | Monthly trip targets |

---

# Database Design Logic

The database was designed using a **star-schema inspired structure** to support analytical queries efficiently.

### Why Fact and Dimension Tables Were Used

## Fact Tables
Fact tables store measurable business events such as:

- Trips
- Revenue
- Passenger counts

These tables help perform aggregations and KPI analysis.

## Dimension Tables
Dimension tables provide descriptive context such as:

- City names
- Dates
- Passenger categories

This structure improves:

- Query efficiency
- Data consistency
- Analytical flexibility

---

# Record Statistics

| Table | Number of Records |
|---|---|
| fact_trips | 425,903 |
| dim_repeat_trip_distribution | 540 |
| fact_passenger_summary | 60 |
| dim_date | 182 |
| dim_city | 10 |

---

# Project Workflow

## 1️⃣ Data Collection

The project started with understanding the available datasets and identifying important business metrics.

---

## 2️⃣ Data Cleaning & Preparation

The data was cleaned to:

- Remove inconsistencies
- Standardize formats
- Ensure referential integrity
- Prepare tables for analytical queries

### Why This Step Was Important

Poor-quality data leads to incorrect business insights.

Cleaning ensures:
- Accurate reporting
- Reliable KPIs
- Better dashboard performance

---

## 3️⃣ SQL Analysis

SQL was used extensively to perform business analysis.

### Why SQL Was Chosen

SQL is highly efficient for:

- Aggregations
- Joins
- Filtering
- Window functions
- Business reporting

The project used:

- Views
- Stored Procedures
- Database Functions
- CTE logic
- Window Functions

---

# Business Questions & Analytical Logic

## 1️⃣ City Fare & Trip Contribution Analysis

### Objective
Analyze:
- Total trips
- Average fare per km
- Average fare per trip
- City contribution percentage

### Why This Analysis Was Done

This helps identify:

- High-demand cities
- Revenue efficiency
- Operational performance
- Pricing effectiveness

A city with high trip volume but low revenue may indicate:
- Low fare pricing
- Short-distance trips
- Heavy discounts

This analysis helps management focus on profitable cities instead of only high-volume cities.

---

## 2️⃣ Monthly Target Performance Analysis

### Objective
Compare:
- Actual trips
- Target trips
- Percentage difference

### Why This Analysis Was Done

Business targets are critical KPIs.

This analysis helps management:
- Evaluate operational efficiency
- Measure city-wise performance
- Identify underperforming regions
- Improve forecasting

Cities failing targets may require:
- Better driver allocation
- Marketing campaigns
- Demand optimization strategies

---

## 3️⃣ Repeat Passenger Distribution Analysis

### Objective
Analyze repeat passengers based on trip frequency.

Example:
- 2 trips
- 3 trips
- 4 trips
- Up to 10 trips

### Why This Analysis Was Done

Repeat customers are one of the strongest indicators of customer satisfaction.

This analysis helps understand:
- Passenger loyalty
- Customer retention patterns
- Ride usage frequency

It also supports:
- Loyalty program planning
- Personalized promotions
- Driver quality evaluation

---

## 4️⃣ New Passenger Ranking Analysis

### Objective
Identify:
- Top 3 cities
- Bottom 3 cities
based on new passengers.

### Why This Analysis Was Done

New passenger growth reflects:
- Market penetration
- Marketing effectiveness
- Brand visibility

Low-performing cities may require:
- Local promotions
- Referral programs
- Better operational support

---

## 5️⃣ Revenue Contribution Analysis

### Objective
Identify the highest revenue-generating month for each city.

### Why This Analysis Was Done

This helps management understand:
- Seasonal demand patterns
- Revenue spikes
- Business opportunities

Example:
Holiday seasons can significantly increase trip demand.

Management can use these insights for:
- Surge planning
- Marketing timing
- Resource allocation

---

# Stored Procedures

The project includes reusable stored procedures for automation and advanced analysis.

---

## City Performance Procedure

### Purpose
Generate:
- Monthly repeat passenger rate
- City-wide repeat rate

### Why It Was Created

This procedure helps management quickly evaluate customer retention performance for any city without rewriting queries.

---

## Repeat Rate vs Passenger Rating Procedure

### Purpose
Analyze the relationship between:
- Passenger ratings
- Driver ratings
- Repeat passenger rates

### Why This Analysis Matters

Higher satisfaction usually leads to:
- Better customer loyalty
- Increased repeat usage
- Higher revenue stability

This analysis helps identify whether service quality directly affects retention.

---

## Revenue Analysis Procedure

### Purpose
Generate monthly revenue reports for selected cities.

### Why This Was Important

This allows:
- Revenue trend analysis
- Seasonal comparison
- City-wise financial evaluation

---

# Database Functions

## Percentage Difference Function

### Purpose
Calculate the percentage difference between:
- Actual new passengers
- Target new passengers

### Why This Function Was Built

This helps evaluate:
- Marketing effectiveness
- Customer acquisition performance
- Growth efficiency

---

## Revenue Contribution Function

### Purpose
Calculate:
- City revenue
- Total company revenue
- Percentage contribution

### Why This Analysis Matters

This helps identify:
- Most profitable cities
- Revenue dependency
- Strategic business priorities

---

# Power BI Dashboard

## 1️⃣ Repeat Rate Dashboard

<img src="images/Repeat Rate.png" width="900">

### Dashboard Features

- Repeat passenger analysis
- Passenger rating comparison
- Driver rating comparison
- Monthly repeat rate tracking
- Repeat trip category contribution
- Interactive city & month filters

### Major Insights

- Surat and Lucknow showed strong repeat passenger behavior
- April and May had the highest repeat rates
- Most passengers repeated exactly 2 trips
- Jaipur had the highest number of trips
- Mysore achieved the highest passenger rating

---

## 2️⃣ Revenue & Target Dashboard

<img src="images/Targets & Revenue.png" width="900">

### Dashboard Features

- Trips vs Fare analysis
- Actual vs Target comparison
- Revenue trend analysis
- KPI tracking
- Passenger target monitoring

### Major Insights

- February generated the highest revenue
- Jaipur generated the highest overall revenue
- Mysore experienced strong seasonal revenue growth
- January and June failed to meet trip targets

---

# Key Business Insights

## 📌 Passenger Retention Is Critical

Repeat passengers significantly contribute to stable revenue.

Cities with higher repeat rates likely provide:
- Better service quality
- Better customer experience
- Reliable driver behavior

---

## 📌 Revenue ≠ High Trips

Some cities generate high revenue despite lower trip volume.

This indicates:
- Better pricing efficiency
- Longer-distance trips
- Higher-value customers

---

## 📌 Seasonal Trends Matter

Holiday periods showed higher revenue growth.

This suggests:
- Demand forecasting is important
- Seasonal promotions can improve profitability

---

## 📌 Underperforming Cities Need Attention

Cities missing targets may require:
- Better marketing
- Improved operations
- More driver availability

---

# Recommendations

## 1️⃣ Launch Loyalty Programs

### Why
Increasing repeat passengers improves long-term profitability.

### Suggested Solutions
- Reward points
- Membership plans
- Cashback offers
- Subscription benefits

---

## 2️⃣ Optimize Pricing Strategies

### Why
Different cities have different demand patterns.

### Suggested Solutions
- Dynamic pricing
- City-specific pricing models
- Seasonal pricing adjustments

---

## 3️⃣ Improve Customer Experience

### Why
Passenger satisfaction directly impacts repeat rates.

### Suggested Solutions
- Faster ride allocation
- Better customer support
- Driver quality monitoring

---

## 4️⃣ Focus on Underperforming Cities

### Why
Certain cities may have untapped growth potential.

### Suggested Solutions
- Localized marketing campaigns
- Driver expansion
- Service quality improvements

---

# Tools & Technologies Used

| Tool | Purpose |
|---|---|
| MySQL | Database design & analysis |
| Power BI | Dashboard development |
| Excel | Initial data cleaning |
| SQL | Business querying & reporting |

---

# Repository Structure

```bash
Good-Cabs-Performance-Analysis/
│
├── BI.pbix
├── challenge.sql
├── Report.pdf
├── README.md
│
├── images/
│   ├── Repeat Rate.png
│   └── Targets & Revenue.png
```

---

# How to Run This Project

## Step 1 — Clone Repository

```bash
git clone https://github.com/ShreyanshDangi/Good-Cabs-Performance-Analysis.git
```

## Step 2 — Import Database

Run the SQL scripts in MySQL.

---

## Step 3 — Open Power BI File

Open:

```bash
BI.pbix
```

using Power BI Desktop.

---

## Step 4 — Explore Dashboards

Use filters and visuals to interact with business insights.

---

# Learning Outcomes

This project strengthened skills in:

- SQL Query Optimization
- Database Design
- Window Functions
- Business Analytics
- Power BI Dashboarding
- KPI Analysis
- Data Storytelling
- Analytical Thinking

---

# Future Improvements

Possible future enhancements:

- Demand forecasting using Machine Learning
- Customer churn prediction
- Driver performance analytics
- Real-time dashboards
- AI-based pricing recommendations

---

# Conclusion

This project demonstrates how structured data analytics can transform raw operational data into actionable business intelligence.

Using SQL, database engineering, and Power BI visualization, the project successfully analyzes:

- Revenue performance
- Customer retention
- Operational efficiency
- City-wise business growth

The insights generated can help GoodCabs make strategic decisions that improve profitability, customer satisfaction, and long-term business growth.

---

# Author

## 👨‍💻 Shreyansh Dangi

If you found this project useful, consider giving it a ⭐ on GitHub.
