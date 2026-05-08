# US Traffic Accident Analysis (2016 - 2023)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Library-Pandas-orange)
![Seaborn](https://img.shields.io/badge/Library-Seaborn-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
This project focuses on performing **Exploratory Data Analysis (EDA)** on a large-scale dataset of traffic accidents across the United States. The goal is to identify hidden patterns related to road conditions, weather, and time of day to provide actionable insights for road safety.

**Dataset Link:** [US Accidents (2016 - 2023)](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents)

## 🚀 Project Pipeline

1.  **Data Acquisition:** Managing a large-scale (7.7M+ records) CSV dataset using memory optimization techniques.
2.  **Data Cleaning:** * Handled missing values for weather and temperature.
    * Removed redundant columns (`End_Lat`, `End_Lng`).
    * Standardized date-time formats.
3.  **Feature Engineering:** Extracted `Hour`, `Day`, and `Month` to analyze temporal trends.
4.  **Exploratory Data Analysis (EDA):**
    * **Time Analysis:** Identified peak accident hours and weekday vs. weekend shifts.
    * **Environmental Analysis:** Correlation between weather conditions and accident frequency.
    * **Infrastructure Analysis:** Impact of traffic signals, junctions, and crossings.
5.  **Visualization:** Built high-quality heatmaps and distribution plots using Seaborn and Matplotlib.

## 📊 Key Insights

* **The Rush Hour Effect:** Accidents peak significantly during weekday morning (7-9 AM) and evening (4-6 PM) commutes.
* **The Volume Paradox:** Contrary to expectations, ~70% of accidents occur during **Clear/Fair** weather, likely due to increased traffic volume and higher driver speeds.
* **Infrastructure Hotspots:** Traffic Signals and Junctions represent the highest conflict zones for drivers.
* **Top States:** California, Florida, and Texas show the highest density of incidents, correlating with high population and extensive road networks.

## 🛠️ Technology Stack
* **Language:** Python 3.x
* **Libraries:** * `Pandas`: Data Manipulation
    * `Matplotlib`: Base Plotting
    * `Seaborn`: Advanced Statistical Visuals
    * `DateTime`: Time-series Analysis

## 📂 Project Structure
```text
├── US_Accidents_Analysis.ipynb   # Main Analysis Notebook
├── US_Accident_Report.pdf        # Detailed Project Report
├── data/                         # Directory for Dataset (not uploaded due to size)
└── README.md                     # Project Documentation
```
📝 How to Run
Clone the repository:

```Bash
git clone [https://github.com/yourusername/us-accident-analysis.git](https://github.com/yourusername/us-accident-analysis.git)
```
Install dependencies:

```Bash
pip install pandas matplotlib seaborn
Download the dataset from Kaggle and place it in the root directory.
```
Run the Jupyter Notebook or Python script.

🤝 Acknowledgements
Dataset Author: Sobhan Moosavi

Organization: Internship Task-05 for ProDigy Infotech.

Created as part of the Data Science Internship program at ProDigy Infotech.

