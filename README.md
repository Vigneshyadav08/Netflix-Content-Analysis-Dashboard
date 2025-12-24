# 🎬 Netflix Content Analytics Dashboard (Power BI)

## 📌 Overview
This project showcases a **Netflix-style interactive Power BI dashboard** designed to analyze movies and TV shows across genres, release years, countries, and content types.  
The objective is to transform raw content data into **business-ready insights** using KPIs, DAX, and visual storytelling.

---

## 🎯 Business Problem
Streaming platforms manage large and diverse content libraries.  
Business stakeholders require an interactive reporting solution to:

- Identify top-performing genres
- Understand content growth over time
- Compare Movies vs TV Shows
- Analyze country-wise content distribution
- Support data-driven content strategy decisions

This dashboard addresses these needs using **Power BI analytics**.

---

## 📊 Key KPIs
- Total Netflix Titles  
- Total Movies  
- Total TV Shows  
- Average Release Year  
- Top Genre (Dynamic)

---

## 🧠 Analytical Approach
- Cleaned and transformed raw data using **Power Query**
- Created calculated columns and measures using **DAX**
- Applied genre detection using text-based logic
- Designed interactive visuals with slicers, drill-through, and tooltips
- Enhanced storytelling using movie and genre posters

---

## 🛠 Tools & Technologies
- Power BI Desktop  
- DAX (CALCULATE, CONTAINSSTRING, SWITCH)  
- Power Query  
- Excel (Poster URL mapping)

---

## 📐 DAX Example
```DAX
Primary_Genre =
SWITCH(
    TRUE(),
    CONTAINSSTRING('Netflix'[listed_in], "Drama"), "Drama",
    CONTAINSSTRING('Netflix'[listed_in], "Comedy"), "Comedy",
    CONTAINSSTRING('Netflix'[listed_in], "Action"), "Action",
    CONTAINSSTRING('Netflix'[listed_in], "Horror"), "Horror",
    "Other"
)
