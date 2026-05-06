# Olympics Performance & Medal Analysis (1896–2016)

An interactive Power BI dashboard project focused on analyzing historical Olympic Games data from 1896 to 2016. This project transforms raw Olympic athlete data into meaningful visual insights related to participation, medals, countries, sports, and athlete demographics.

---

#  Project Overview

The Olympic Games have evolved significantly over the years in terms of participation, competitiveness, and inclusivity. The aim of this project is to analyze historical Olympic data and identify important trends and patterns using data visualization techniques.

This dashboard helps users explore:
- Athlete participation trends
- Medal distribution across sports and countries
- Gender participation growth
- Athlete characteristics such as age, height, and weight
- Seasonal Olympic participation

---

# Problem Statement

To analyze Olympic Games data and create an interactive dashboard that provides insights into athlete participation, medal performance, country dominance, and demographic trends from 1896 to 2016.

---

# Tools & Technologies Used

- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- CSV Dataset
- Data Visualization Techniques

---

# Dataset Information

Dataset Source:
Kaggle – 120 Years of Olympic History: Athletes and Results

Dataset includes:
- Athlete details
- Country information
- Sports and events
- Medal records
- Olympic years and seasons

---

# ETL Process

The ETL process was performed inside Power BI using Power Query.

### Data Cleaning Steps
- Removed null values
- Removed duplicate records
- Corrected data types
- Standardized gender values
- Replaced missing medals with "No Medal"

---

#  Dashboard Features

## 1. KPI Cards
Displays:
- Total Athletes
- Total Medals
- Gold Medals
- Total Countries
- Average Age
- Average Height
- Average Weight

---

## 2. Participation Trend Analysis
A line chart showing athlete participation growth over time.

### Key Insight:
Olympic participation increased rapidly after 1950.

---

## 3. Top Sports by Medals
Stacked bar chart comparing Gold, Silver, and Bronze medals across sports.

### Key Insight:
Athletics and Swimming have the highest medal counts.

---

## 4. Top Countries by Medals
Bar chart representing countries with highest Olympic success.

### Key Insight:
United States dominates Olympic medal counts.

---

## 5. Gender Participation Analysis
Stacked column chart showing male and female participation trends.

### Key Insight:
Female participation has increased steadily over time.

---

## 6. Age vs Weight Analysis
Scatter plot representing athlete age and weight distribution.

### Key Insight:
Most athletes fall in the 20–30 age group.

---

## 7. Participation by Season
Donut chart comparing Summer and Winter Olympics participation.

### Key Insight:
Summer Olympics account for the majority of participation.

---

# Important DAX Measures

DAX
Total Athletes = DISTINCTCOUNT(athlete_events[ID])

Total Medals =
CALCULATE(
    COUNTROWS(athlete_events),
    athlete_events[Medal] <> "No Medal"
)

Avg Age = AVERAGE(athlete_events[Age])
