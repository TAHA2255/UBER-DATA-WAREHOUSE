# Uber Data Warehouse Project

## 1. Introduction
In today’s data-driven landscape, organizations leverage vast amounts of information from various sources to gain insights that support critical decision-making. For ride-sharing companies like Uber and traditional taxi services operating in highly dynamic environments such as New York City, data offers a powerful means to understand customer preferences, optimize operations, and enhance revenue generation strategies. However, managing and analyzing this data can be challenging when it exists in disparate formats across multiple systems.

This project addresses these challenges by implementing a **data warehouse**—a centralized repository that consolidates Uber drive data, NYC taxi data, and Uber customer review data. By integrating these sources, the data warehouse provides a unified foundation for in-depth analysis and reporting. This single source of truth facilitates the generation of accurate and timely insights into key performance indicators (KPIs) such as ride trends, customer satisfaction, and revenue. 

The project’s scope includes:
- Data integration from multiple sources.
- Creation of an **ETL (Extract, Transform, Load)** pipeline to automate data collection, cleaning, transformation, and loading into the warehouse.

---

## 2. Project Objectives
The objectives of this data warehouse implementation are:
- **Centralized Data Storage**: Consolidate data from Uber, NYC Taxi, and Uber Reviews into a single repository.
- **Enhanced Reporting**: Organize data for quick and accurate report generation, enabling the analysis of ride trends, customer experience, and revenue.
- **Data Accuracy**: Ensure integration of clean, consistent data across all sources to support reliable insights.
- **Business Insights and Decision-Making**: Utilize tools such as Power BI or Tableau for visual analytics, aiding stakeholders in data-driven decisions.

---

## 3. Data Sources
The following data sources were integrated:
- **Uber Drive Data**: Includes details such as start and end times, ride category, distance, and purpose.
- **NYC Taxi Data**: Covers information like pickup and drop-off times, trip distance, fare amount, and location IDs.
- **Uber Review Data**: Contains customer feedback, including ratings and comments.

---

## 4. ETL Process
The ETL (Extract, Transform, Load) process included several stages to ensure clean and organized data:

### Step 1: Data Extraction
- Data was extracted using Python’s pandas library, with datasets read into DataFrames for further processing.

### Step 2: Data Transformation
- **Remove Asterisks from Column Names**: Standardized column naming conventions.
- **Column Selection**: Retained only relevant columns such as ride times, distances, categories, fare amounts, ratings, and comments.
- **Column Renaming**: Aligned columns across datasets for consistency (e.g., `tpep_pickup_datetime` → `START_DATE`).
- **Data Type Standardization**: Converted date columns to datetime format and ensured mileage columns were numeric.
- **Duplicate Removal**: Identified and removed redundant entries.
- **Handling Missing Values**: Filtered out rows with missing critical values and filled non-critical fields with placeholders (e.g., `PURPOSE` → "No Purpose").

### Step 3: Data Integration and Load
- **Data Merging**: Combined Uber, NYC Taxi, and Uber Review datasets into a unified dataset.
- **Time of Day Categorization**: Added a `TIME` column to categorize rides as Morning, Afternoon, Evening, or Night.
- **LOAD**: Loaded the consolidated data into a PostgreSQL database.

---

## 5. Challenges in Data Integration
Key challenges encountered during data integration included:
- **Data Inconsistencies**: Variations in data formats (e.g., timestamps, location identifiers).
- **Duplication**: Identifying and filtering duplicate records.
- **Missing Data**: Addressing missing fields using techniques such as imputation.
- **Data Synchronization**: Ensuring consistent time zone and format alignment across datasets.

---

## 6. Application of Data Mining Techniques
Advanced data mining and machine learning algorithms were applied to uncover actionable insights:

- **Clustering for Customer Segmentation**: Grouped customers based on ride frequency, type, and spending behavior, enabling personalized marketing campaigns.
- **Sentiment Analysis**: Classified Uber review comments into positive, neutral, and negative sentiments, providing insights into customer satisfaction.
- **Revenue Prediction**: Used regression models to predict revenue trends and optimize resource allocation.

---

## 7. Key Insights for Enhanced Reporting and Decision-Making
The project delivered valuable insights:
- **Ride Trends**: Analysis of ride categories and purposes identified popular services and peak usage times.
- **Customer Experience Insights**: Sentiment analysis highlighted areas for improving service quality.
- **Revenue Insights**: Insights into average revenue per mile and tipping behavior supported pricing strategy adjustments.

---

## 8. Conclusion
This data warehouse project successfully integrated data from Uber, NYC Taxi, and Uber Reviews into a consolidated repository, enabling advanced analytics and reporting. By overcoming data integration challenges and applying data mining techniques, the project provides actionable insights to:
- Improve operational efficiency.
- Optimize customer experience.
- Support informed decision-making.

---

## Power BI Dashboard
![dwh1](https://github.com/user-attachments/assets/50d675e1-95c7-4d23-ab41-140a9f582546)


## Data Marts

![dwh2](https://github.com/user-attachments/assets/0daabef6-072f-45d8-a1b5-3bf557eda090)
![dwh3](https://github.com/user-attachments/assets/96080980-3e2e-49af-8e7d-54a2d82116e5)
