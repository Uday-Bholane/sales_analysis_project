# 📊 Sales Data Analysis - Complete EDA Project

A comprehensive data analysis project with **data cleaning and 20+ visualizations** - all in a single Jupyter notebook.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Data Cleaning Steps](#data-cleaning-steps)
- [Complete List of Visualizations](#complete-list-of-visualizations)
- [Key Insights](#key-insights)
- [How to Run](#how-to-run)
- [Requirements](#requirements)
- [File Structure](#file-structure)
- [Author](#author)
- [License](#license)

## 🎯 Project Overview

This project performs end-to-end data analysis on e-commerce sales data including:

- **Data Cleaning** - Handling missing values, duplicates, outliers, and data type conversion
- **Exploratory Data Analysis (EDA)** - Statistical analysis and data profiling
- **20+ Data Visualizations** - Comprehensive charts exploring various business metrics

## 📁 Dataset Description

The dataset contains e-commerce transaction data with 15 columns:

| Column            | Data Type | Description                        |
| ----------------- | --------- | ---------------------------------- |
| `Order_ID`        | Integer   | Unique order identifier            |
| `Customer_Name`   | String    | Customer name                      |
| `Gender`          | String    | Customer gender (Male/Female)      |
| `Age`             | Integer   | Customer age                       |
| `City`            | String    | Customer location                  |
| `Product_Name`    | String    | Product purchased                  |
| `Category`        | String    | Product category                   |
| `Unit_Price`      | Float     | Price per unit                     |
| `Quantity`        | Integer   | Number of units purchased          |
| `Discount`        | Float     | Discount applied (0-1 range)       |
| `Total_Price`     | Float     | Final transaction amount           |
| `Payment_Method`  | String    | Payment method used                |
| `Order_Date`      | DateTime  | Date of order                      |
| `Delivery_Days`   | Integer   | Days taken for delivery            |
| `Customer_Rating` | Float     | Customer satisfaction rating (1-5) |

## 🔧 Data Cleaning Steps Performed

The following data cleaning operations were performed in the notebook:

1. **Duplicate Removal**
   - Removed all duplicate rows from the dataset

2. **Missing Value Handling**
   - Dropped rows with null `Product_Name`
   - Dropped rows with null `Order_Date`
   - Filled null numeric values with median

3. **Data Type Conversion**
   - Converted numeric columns (`Age`, `Unit_Price`, `Discount`, `Total_Price`, `Delivery_Days`) to numeric type
   - Converted `Order_Date` to datetime format

4. **Outlier Treatment (IQR Method)**
   - Calculated Q1, Q3, and IQR for numeric columns
   - Replaced outliers with NaN, then filled with median

5. **Logical Cleaning**
   - Removed rows with negative values in numeric columns
   - Removed rows with `Total_Price` <= 0
   - Removed rows with `Quantity` < 1
   - Removed rows with `Customer_Rating` outside 1-5 range
   - Removed rows with `Discount` > 1

6. **Categorical Data Standardization**
   - Applied `.strip().title()` to all categorical columns

7. **Feature Engineering**
   - Created `Year` column from `Order_Date`
   - Created `Month` column from `Order_Date`
   - Created `Day_Name` column from `Order_Date`
   - Created `Week` column from `Order_Date`
   - Created `Cumulative Price` column for time series analysis

## 📊 Complete List of Visualizations

| #   | Chart Type           | Analysis                                                                             |
| --- | -------------------- | ------------------------------------------------------------------------------------ |
| 1   | Line Chart           | Monthly sales trend (2024)                                                           |
| 2   | Bar Chart            | Total sales by product category                                                      |
| 3   | Horizontal Bar Chart | Top 10 highest-selling products                                                      |
| 4   | Pie Chart            | Payment method distribution                                                          |
| 5   | Histogram            | Customer age distribution                                                            |
| 6   | Scatter Plot         | Unit Price vs Total Price relationship                                               |
| 7   | Boxplot              | Delivery days by category                                                            |
| 8   | Violin Plot          | Customer rating distribution                                                         |
| 9   | Stacked Area Chart   | Category sales over time                                                             |
| 10  | Heatmap              | Correlation between numerical columns                                                |
| 11  | Bar Chart            | Number of orders from each city                                                      |
| 12  | Bar Chart            | Average discounts across categories                                                  |
| 13  | Subplot Dashboard    | 4-in-1 dashboard (Sales Trend, Category Sales, Payment Methods, Rating Distribution) |
| 14  | Boxplot              | Outliers in Total Price                                                              |
| 15  | Line Chart           | Cumulative sales over time                                                           |
| 16  | Scatter Plot         | Quantity vs Total Price                                                              |
| 17  | Grouped Bar Chart    | City-wise category sales                                                             |
| 18  | KDE Plot             | Density plot for Unit Price                                                          |
| 19  | Line Chart           | Weekly sales trend                                                                   |
| 20  | Bar Chart            | Average delivery time per city                                                       |

## 📈 Key Insights

### Sales Insights

- Peak sales occur during specific months (visible in monthly trend chart)
- Electronics and Clothing categories generate highest revenue
- Top 10 products contribute significantly to total sales

### Customer Insights

- Core customer age range: 25-45 years
- Customer ratings show a certain distribution pattern (see violin plot)
- Order distribution varies significantly by city

### Payment & Delivery Insights

- Most popular payment methods (see pie chart)
- Delivery times vary by category (boxplot analysis)
- Average delivery time differs by city (bar chart)

### Price & Quantity Insights

- Positive correlation between Unit Price and Total Price
- Quantity and Total Price relationship (scatter plot)

## 🚀 How to Run

### Prerequisites

- Python 3.8 or higher installed
- pip package manager

### Step-by-Step Instructions

```bash
# 1. Clone this repository
git clone https://github.com/YOUR_USERNAME/sales-data-analysis.git
cd sales-data-analysis

# 2. Install required packages
pip install -r requirements.txt

# 3. Launch Jupyter Notebook
jupyter notebook

# 4. In Jupyter, open: practice_project.ipynb

# 5. Run all cells (Kernel → Restart & Run All)
```
