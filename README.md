# 🚀 Adventure Works 2020: Sales Performance Deep Dive

[![Power BI](https://img.shields.io/badge/Tool-Power%20BI-yellow?logo=power-bi)](https://powerbi.microsoft.com/)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📊 Project Overview

This **Power BI report** provides a robust, interactive deep dive into the **Adventure Works 2020 fiscal year sales performance**.  
The goal of this project is to transform complex transactional data into **actionable insights**, enabling **performance monitoring, evaluation, and strategic decision-making** across multiple dimensions: **Product**, **Region**, and **Salesperson**.

The report enables **deep analytical exploration** through advanced Power BI features:

- 🔍 **Layered Drill-Downs:** Navigate from high-level summaries to city-level insights.  
- 💬 **Visual Tooltips & Drill-Through:** Access contextual and transaction-level detail instantly.  
- 📱 **Mobile Layout:** Optimized for accessibility and on-the-go analytics.

---

## 🏗️ Semantic Model Architecture

The report is built on a **high-performance Star Schema**, ensuring efficient query execution and scalability within the Power BI engine.

### 🔹 Data Model Components

| **Component**     | **Granularity**            | **Role**                                                      |
|--------------------|----------------------------|----------------------------------------------------------------|
| `factSales`        | Daily Order Line Level     | Central fact table storing all transactional data.             |
| `dimProduct`       | Product Key                | Dimension for detailed product and category analysis.          |
| `dimDate`          | Date Key                   | Dimension for time-intelligence and temporal analysis.         |
| `dimSales`         | Sales Key                  | Dimension providing sales channel and context.                 |
| `dimSalesperson`   | Employee Key               | Dimension for analyzing individual sales agent performance.    |

### 🔸 Model Integrity & Optimization

- **Relationships:** All relationships are **one-directional** to maintain stability and prevent circular dependencies.  
- **Performance Optimization:** The `factSales` table is **partitioned by year** for faster DAX query execution and improved scalability.

---

## ⚙️ Core DAX Measures

The report’s quantitative analysis is powered by **precise DAX measures**, defining key performance indicators (**KPIs**) such as sales, profit, and margin.

| **Measure Name** | **Description** | **DAX Formula Snippet** |
|------------------|-----------------|--------------------------|
| **Total Sales** | Calculates the total revenue generated across all transactions. | ```dax Total Sales = SUMX( Sales, Sales[Unit Price] * Sales[Quantity] )``` |
| **Profit** | Determines the net profit by subtracting total cost from total sales. | ```dax Profit = SUMX (Sales, Sales[Cost] - Sales[Unit Price])``` |
| **Profit Margin** | Efficiency metric, expressed as a percentage of Profit relative to Total Sales. | ```dax Profit Margin = DIVIDE( [Profit], [Total Sales] )``` |

---

## 📄 Report Structure & Navigation

The report is organized for **seamless exploration**, starting from a **centralized navigation hub**.

### 1. 🏠 Home Page (Navigation Hub)
Acts as a main dashboard, providing:
- Overview of total performance
- Buttons linking to deep-dive pages (Regional, Product, Salesperson)

### 2. 🌍 Regional Analysis Page
- **Visual Focus:** Dynamic map showing *Sum of Sales by Country-Region*  
- **Interactivity:** Drill-down functionality from *Country → State → City*  
- **Insight:** Highlights top-performing and underperforming markets globally

### 3. 📦 Other Key Pages
If included, other analytical pages may cover:
- **Product**  
- **Sales**  


---

## 🚀 Getting Started

### 🗄️ Data Source

This report connects to the **Adventure Works 2020 sample database**.  
Ensure the database is accessible to refresh or update the visuals.

### ⚙️ Prerequisites

To view and fully interact with the `.pbix` file, you need:

- [**Power BI Desktop**](https://powerbi.microsoft.com/desktop/) — the official free application from Microsoft.

---

## 📈 Key Insights

- Clear visualization of **regional sales trends** and **performance variance**  
- Ability to identify **top-performing products** and **sales representatives**  
- Interactive design supports **data-driven strategic planning**

---

## 🧩 Tools & Technologies

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Star Schema Modeling**
- **Adventure Works 2020 Dataset**

---

