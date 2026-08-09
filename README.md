# ✈️ Indian Airline Ticket Price Analytics

> An exploratory data analysis project uncovering what really drives airline ticket price variation in India — built with Python and brought to life in Power BI.

---

## 📌 Project Overview

Airline pricing rarely feels rational to the traveler booking the ticket — but it isn't random either. For example, one day a flight costs ₹5,000, and the next day the same route costs ₹8,500. What changed? Fares shift with booking lead time, airline, travel class, number of stops, flight duration, and even the time of day a flight departs or arrives.

This project digs into historical Indian flight booking data to uncover the patterns behind airfare variation, examining how pricing differs across routes, classes, and booking conditions. Rather than building a model to predict future prices, the goal here is to explain the "why" behind the numbers — turning raw booking data into pricing insight.

The analysis pairs Python-based exploratory data analysis with an interactive Power BI dashboard, translating statistical findings into insights a business or traveler could actually act on.

### 🛠️ Tech Stack

`Python` · `pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Power BI` · `Jupyter Notebook`

---

## 🎯 Business Problem

Airline pricing in India is highly dynamic. Two travelers flying the same origin-destination pair, on similar dates, can end up paying very different fares — depending on how early they booked, which airline they chose, which class they flew, and more.

This project sets out to answer one central question:

> **What factors are associated with differences in airline ticket prices in the Indian domestic aviation market?**

Specifically, the analysis explores:

- Which airlines operate the most flights?
- Which airlines command higher average fares?
- How much does travel class affect price?
- Does booking earlier actually save money?
- How does flight duration relate to ticket price?
- What effect do layovers and stops have on fares?
- Which routes carry the highest average fares?
- Does departure or arrival timing move the price needle?

---

## 🎯 Project Objectives

This project aims to:

- Analyze the overall distribution of airline ticket prices
- Compare pricing across airlines and travel classes
- Understand the relationship between booking lead time and fare
- Examine how flight duration and number of stops influence price
- Identify the highest-priced source-destination routes
- Explore pricing differences across departure and arrival time slots
- Uncover relationships between numerical flight attributes and price
- Present all findings through an interactive Power BI dashboard

---

## 📊 Dataset

This project uses a secondary dataset sourced from Kaggle:

**Flight Price Prediction Dataset — EaseMyTrip**

The dataset contains approximately **300,261 flight booking records** collected from the EaseMyTrip website, covering domestic routes between six major Indian metropolitan cities.

### Dataset Characteristics

| Attribute | Description |
|---|---|
| Records | 300,261 |
| Features | 11 |
| Geography | Domestic India |
| Cities | Six major metropolitan cities |
| Travel Classes | Economy, Business |
| Collection Period | Approximately 50 days |
| Period | February–March 2022 |
| Data Type | Historical booking data |

### Source

Dataset: [Kaggle — Flight Price Prediction](https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction)

> **Note:** This dataset reflects a historical snapshot in time and should not be interpreted as a complete or current representation of Indian airline pricing today.

---

## 🧭 Methodology

The analysis followed a structured EDA workflow:

1. **Data Cleaning & Preparation**
   - Removed duplicate records and irrelevant index columns
   - Standardized categorical fields (airline names, city names, class labels)
   - Converted duration and days-left fields into consistent numeric formats
   - Checked for and handled missing values and outliers in the `price` column

2. **Univariate Analysis**
   - Examined the distribution of ticket prices using histograms and box plots
   - Identified skewness and price outliers across the dataset

3. **Bivariate & Multivariate Analysis**
   - Compared price distributions across airlines, classes, and number of stops using box plots and bar charts
   - Analyzed price vs. days-left-to-departure to test the "book early, pay less" assumption
   - Examined price vs. duration and price vs. departure/arrival time bands
   - Used a correlation heatmap to surface relationships among numerical features

4. **Route-Level Analysis**
   - Grouped data by source–destination pairs to identify the highest and lowest average-fare routes

5. **Dashboard Development**
   - Rebuilt key EDA findings as interactive visuals in Power BI
   - Added filters for airline, class, route, and stops to allow self-service exploration

*Full code and transformations are available in [`Indian_Airline_Ticket_Price_Analytics.py`](./Indian_Airline_Ticket_Price_Analytics.py).*

---

## 📈 Key Findings

> ⚠️ *Placeholder — replace each bullet below with your actual output (numbers, airline names, and route names) once pulled from your analysis.*

- **Class is the dominant price driver.** Business class fares averaged roughly **[X]×** higher than Economy on comparable routes.
- **Booking lead time matters.** Fares booked **[X] days or fewer** before departure were on average **[X]% higher** than those booked 3+ weeks out.
- **Airline pricing varies significantly.** **[Airline name]** had the highest average fare among major carriers (₹**[X]**), while **[Airline name]** was consistently the most budget-friendly.
- **Stops increase price, up to a point.** Non-stop flights were **[cheaper/pricier]** on average than 1-stop flights, driven largely by **[duration/class mix]**.
- **Duration correlates weakly/moderately with price** (correlation coefficient: **[X]**), suggesting route and class matter more than raw flight time.
- **Route effects are real.** The **[City A → City B]** route carried the highest average fare (₹**[X]**), while **[City C → City D]** was the most affordable major route.
- **Timing has a modest effect.** Flights departing during **[time band]** were priced **[X]%** higher than **[time band]** departures, likely reflecting demand patterns rather than cost.

---

## 📊 Dashboard Preview

![Dashboard Snapshot](./dashboards/Dashboard_Snapshot.png)

The interactive Power BI dashboard (`Indian_Airline_Ticket_Price_Analytics.pbix`) lets users filter by airline, route, class, and stops to explore pricing patterns without touching the underlying code.

---

## 🗂️ Project Structure

```text
Indian_Airline_Ticket_Price_Analytics/
│
├── data/
│   ├── airline_tickets.csv
│   └── airline_tickets_cleaned.csv
│
├── dashboards/
│   ├── Indian_Airline_Ticket_Price_Analytics.pbix
│   └── Dashboard_Snapshot.png
│
├── Indian_Airline_Ticket_Price_Analytics.py
│
├── README.md
│
├── requirements.txt
│
└── workflow.md
```

---

## 👤 Author

**Ashwin Gothwal**
