# 🏡 Austin Housing Market Insights – Power BI Dashboard

This project provides a comprehensive analysis of Austin, Texas’s residential property market using Power BI. It includes robust data modeling, optimization through normalization, and rich visualizations to help users explore property trends, school accessibility, and key housing features.

---

### 📑 Contents:
- **Power BI Dashboard**
- **Project Resources:** Data Model, Data File, Background Theme

## 📊 Project Overview

- **Tool Used**: Power BI  
- **Focus Area**: Data modeling, DAX optimization, interactive dashboards, feature impact analysis

---

## 🛠️ Data Preparation & Modeling

1. **Data Cleaning & Preprocessing**
   - Imported the Excel dataset and created a cleaned reference table.
   - Disabled load for unused tables to optimize performance.

2. **Fact & Dimension Tables**
   - Built a central fact table `housing_fact`.
   - Created 5 dimension tables: `features`, `house`, `school`, `location`, `description`.
   - Assigned surrogate keys to all dim tables (except `location` and `description`).

3. **Relationships & Cardinality**
   - Defined relationships:
     - `location` ↔ `housing_fact`: 1:1
     - `description` → `housing_fact`: Many:1
     - All others: Many:1 (from Fact to Dim)

4. **Snowflake Schema**
   - Further normalized the `description` table into `word_summary_pqe`, creating a snowflake schema for detailed keyword-level insights.

5. **Optimization**
   - Normalization reduced overall file size by **~40%**, improving report performance and manageability.

---

## 📍 Dashboard Pages & Features

### 1. **Summary View**
A high-level snapshot of the current property market in Austin:
- KPIs: Property count, Median Home Price, Median Living Area, Median Lot Size
- Visuals:
  - Properties by Home Type
  - Median vs Avg Home Price by Type
  - Properties by Zipcode
  - Feature Distribution (%)
  - Build Year Breakdown
 
![Summary View]([https://github.com/yasharora57/DA2_Advanced_Project-Austin-Property-Market-Insights-Dashboard-using-PowerBI/blob/ae1cbed25dd467c5124986b600243971beaae230/Project%20Resources/Report%20Views/View%201_Summary.png])


### 2. **Location View**
An interactive geospatial map:
- Filter and explore property locations
- Hover to view key metrics and property details

![Location View]([https://github.com/yasharora57/DA2_Advanced_Project-Austin-Property-Market-Insights-Dashboard-using-PowerBI/blob/ae1cbed25dd467c5124986b600243971beaae230/Project%20Resources/Report%20Views/View%202_Location.png])

### 3. **School View**
Analyze property suitability based on nearby schools:
- KPIs: Avg School Rating, Avg School Size, Student–Teacher Ratio
- Interactive map filtered by:
  - School Rating
  - School Size
  - Students per Teacher
- Pie charts for property distribution by school rating

![School View]([https://github.com/yasharora57/DA2_Advanced_Project-Austin-Property-Market-Insights-Dashboard-using-PowerBI/blob/ae1cbed25dd467c5124986b600243971beaae230/Project%20Resources/Report%20Views/View%203_Schools.png])

### 4. **Features View**
Understand which features drive housing value:
- Key Influencers chart: What impacts home prices
- Median Home Price by:
  - No. of Bedrooms, Bathrooms, Garages, Appliances, etc.
- Text Analytics: Common listing words by price segment

![Features View]([https://github.com/yasharora57/DA2_Advanced_Project-Austin-Property-Market-Insights-Dashboard-using-PowerBI/blob/ae1cbed25dd467c5124986b600243971beaae230/Project%20Resources/Report%20Views/View%204_Features.png])

---

## 📦 Key Outcomes

- Created a **normalized star and snowflake schema** to improve query efficiency.
- **40% reduction in dataset size** by removing redundancy.
- Delivered a **clean, interactive Power BI experience** for both buyers and analysts.
- Incorporated **AI-driven insights** via Key Influencers to explain price variations.

---
