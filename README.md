# ProdigyInfotech_DataScience_Internship
# README: Population Data Distribution Analysis

## 📌 Project Overview
This project involves performing Exploratory Data Analysis (EDA) on global population datasets. The primary objective is to visualize the distribution of categorical variables (Regions) and continuous variables (Total Population) to identify patterns, outliers, and data characteristics.

## 📊 Dataset Information
The analysis utilizes standard World Bank datasets:
*   **Main Dataset:** `API_SP.POP.TOTL_DS2_en_csv_v2_127039.csv` (Time-series population data).
*   **Metadata:** `Metadata_Country_API_SP.POP.TOTL_DS2_en_csv_v2_127039.csv` (Regional and income group classifications).

## 🛠️ Requirements
*   **Environment:** Jupyter Notebook.
*   **Language:** Python 3.x.
*   **Libraries:** `pandas`, `matplotlib`, `seaborn`.

## 🚀 Execution Steps

### 1. Data Loading
The World Bank CSV contains 4 rows of metadata at the top. We use `skiprows=4` to access the clean data table[cite: 1].
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load datasets
df = pd.read_csv('API_SP.POP.TOTL_DS2_en_csv_v2_127039.csv', skiprows=4)
metadata = pd.read_csv('Metadata_Country_API_SP.POP.TOTL_DS2_en_csv_v2_127039.csv')
