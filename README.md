# ProdigyInfotech_DataScience_Internship
# README: Population Data Distribution Analysis

## 📌 Project Overview
This project involves performing Exploratory Data Analysis (EDA) on global population datasets. The primary objective is to visualize the distribution of categorical variables (Regions) and continuous variables (Total Population) to identify patterns, outliers, and data characteristics.

## 📊 Dataset Information
The analysis utilizes standard World Bank datasets:
*   **Main Dataset:** `TimelineData.csv` (Time-series population data).
*   **Metadata:** `Metadata_Country_API_SP.POP.TOTL_DS2_en_csv_v2_127039.csv` (Regional and income group classifications).

## 🛠️ Requirements
*   **Environment:** Jupyter Notebook.
*   **Language:** Python 3.x.
*   **Libraries:** `pandas`, `matplotlib`, `seaborn`.

## 🚀 Execution Steps

### 1.  Data Loading
The World Bank CSV contains 4 rows of metadata at the top. We use `skiprows=4` to access the clean data table[cite: 1].
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load datasets
df = pd.read_csv('TimelineData.csv', skiprows=4)
metadata = pd.read_csv('Metadata_Country_API_SP.POP.TOTL_DS2_en_csv_v2_127039.csv')
# Merging data
merged_df = pd.merge(df, metadata, on='Country Code')

# Plotting distribution by Region
plt.figure(figsize=(10, 6))
sns.countplot(data=merged_df, y='Region', order=merged_df['Region'].value_counts().index)
plt.title('Distribution of Countries by Region')
plt.show()

# Histogram of 2023 Population
plt.figure(figsize=(10, 6))
sns.histplot(df['2023'].dropna(), bins=30, kde=True)
plt.xscale('log')  # Applying log scale due to extreme outliers
plt.title('Distribution of World Population (2023)')
plt.show()
```
# Project Insights: World Population Distribution Analysis

## 📌 Executive Summary
This section documents the key findings derived from the Exploratory Data Analysis (EDA) of the World Bank population dataset. The analysis focused on regional distribution and population scale using categorical and continuous variables[cite: 1].

---

## 📊 Key Insights

### 1. Categorical Analysis (Regional Distribution)
*   **Granularity**: Sub-Saharan Africa and Europe & Central Asia have the highest count of reporting entities, making them the most granular regions in the data[cite: 1].
*   **Representation**: While the dataset is globally comprehensive, the "North America" region represents only a small number of sovereign entities (e.g., USA, Canada, and Bermuda), which contrasts with its high economic influence[cite: 1].

### 2. Continuous Analysis (Population Scale)
*   **Power Law Distribution**: The population data is heavily right-skewed, demonstrating that population is not distributed "normally" across the globe[cite: 1].
*   **Global Giants**: A few "Global Giants" (specifically India and China) act as extreme outliers that significantly inflate the global mean[cite: 1].
*   **Typical Scale**: The majority of the world's sovereign entities manage populations under 20 million, highlighting a massive scale disparity compared to top-tier nations[cite: 1].

---

## 🛠️ Data Science Context
*   **Logarithmic Scaling**: Due to the presence of extreme outliers, a logarithmic scale was essential for the histogram to visualize the "Long Tail" of the distribution effectively[cite: 1].
*   **Data Skewness**: Understanding that the **Median** population is a more representative metric than the **Mean** is critical for this dataset, as the mean is skewed by the highly populated outliers[cite: 1].

---

