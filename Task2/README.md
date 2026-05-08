# Automobile Data Analysis & Preprocessing (Task 2)

## 📌 Project Overview
This project focuses on the **Exploratory Data Analysis (EDA)** and **Data Preprocessing** of the Automobile dataset. The goal is to clean a raw dataset containing various vehicle specifications—ranging from engine size and fuel type to market price—and prepare it for subsequent statistical analysis or machine learning modeling.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `Pandas`: Data manipulation and structural analysis.
    * `NumPy`: Numerical operations and handling missing values.
    * `Matplotlib` & `Seaborn`: Statistical data visualization.

## 🚀 Key Achievements & Workflow

### 1. Data Cleaning & Standardization
* **Handling Non-Numeric Placeholders:** Identified that the dataset used `"?"` to represent missing values. These were systematically replaced with `NaN` (Not a Number) to make the data compatible with Python's analytical tools.
* **Column Transformation:** Converted the following features from `object` to `float64` to allow for mathematical computations:
    * `normalized-losses`, `bore`, `stroke`, `horsepower`, `peak-rpm`, and `price`.

### 2. Missing Value Imputation
* **Numerical Data:** Applied **Mean Imputation** to fill gaps in numerical columns, ensuring that the statistical distribution remained consistent without losing 15% of the data through row deletion.
* **Categorical Data:** Used **Mode Imputation** for features like `num-of-doors` to maintain the integrity of the categorical profiles.

### 3. Exploratory Data Analysis (EDA)
* **Price Distribution:** Discovered that the average car price is approximately **$13,207**, with a right-skewed distribution indicating a concentration of affordable cars and a few high-end luxury outliers.
* **Performance Metrics:** Analyzed the relationship between engine size (avg: 126.9) and horsepower (avg: 104.25).
* **Fuel Efficiency:** Established baseline fuel economy metrics with an average of **25.2 City MPG** and **30.7 Highway MPG**.

📊 Key Exploratory Findings

| Metric | Value | Statistical Insight |
| :--- | :--- | :--- |
| **Average Price** | ~$13,207 | Right-skewed distribution; presence of luxury outliers. |
| **Avg Horsepower** | 104.25 hp | Most vehicles fall in the mid-range performance category. |
| **City Efficiency** | 25.2 MPG | Critical factor for urban-targeted vehicle analysis. |
| **Highway Efficiency**| 30.7 MPG | Baseline for long-distance fuel economy studies. |

---

## 🏁 Conclusion & Next Steps
The dataset is now fully preprocessed and standardized. With all 205 records preserved and optimized, the project is ready for:
1. **Correlation Analysis:** Determining which features (e.g., engine size, weight) most strongly influence price.
2. **Predictive Modeling:** Developing regression models to estimate vehicle market value.
3. **Advanced Visualization:** Generating heatmaps and pair plots to visualize feature relationships.

---


## 📁 Project Structure
```text
├── DSTask2.ipynb          # Main Jupyter Notebook with code and visualizations
├── automobile_data.csv    # Raw dataset (assumed)
└── README.md              # Project documentation
