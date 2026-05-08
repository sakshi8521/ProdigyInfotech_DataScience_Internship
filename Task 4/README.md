# 📊 Social Media Sentiment Analysis: Public Perception & Brand Health

## 📝 Project Overview
This project focuses on analyzing and visualizing sentiment patterns in social media data to decode public opinion toward specific topics or brands[cite: 1]. By leveraging Natural Language Processing (NLP), we transform thousands of unstructured tweets into actionable insights regarding brand reputation and consumer sentiment trends[cite: 1].

---

## 🏗️ The Data Science Pipeline

The project follows a rigorous end-to-end pipeline to ensure data integrity and analytical depth:

### 1. Data Acquisition & Structural Setup
*   **Source:** Prodigy InfoTech Task-04 Dataset (`twitter_training.csv`)[cite: 1].
*   **Initial Setup:** As the raw data lacked headers, columns were manually mapped to `ID`, `Entity`, `Sentiment`, and `Content` to establish a clean working schema[cite: 1].

### 2. Exploratory Data Analysis (EDA)
*   **Label Audit:** Analyzed the distribution of existing sentiment labels (Positive, Negative, Neutral, and Irrelevant)[cite: 1].
*   **Visual Distribution:** Used Seaborn count plots to identify the volume of "Irrelevant" data, which helps in understanding the level of noise within the dataset[cite: 1].

### 3. Advanced Data Preprocessing
*   **Noise Removal:** Utilized Regular Expressions (Regex) to strip URLs, HTML tags, and user `@mentions`[cite: 1].
*   **Linguistic Normalization:** Converted text to lowercase and removed special characters/numbers to focus purely on descriptive vocabulary[cite: 1].
*   **Stability Handling:** Cleaned missing values and empty strings to prevent computational errors during scoring[cite: 1].

### 4. Sentiment Intensity Scoring (VADER)
*   **Metric:** Implemented the **VADER (Valence Aware Dictionary and sEntiment Reasoner)** model[cite: 1].
*   **Compound Score:** Every post was assigned a granular score between `-1.0` (Highly Negative) and `+1.0` (Highly Positive)[cite: 1].
*   **Contextual Logic:** VADER was chosen for its ability to recognize emotional intensity in capitalization (e.g., "GREAT") and punctuation (e.g., "!!!")[cite: 1].

### 5. Visual Insights & Pattern Recognition
*   **Brand Health Index:** Aggregated average sentiment scores by `Entity` to identify which brands have the most resilient positive reputations[cite: 1].
*   **Qualitative Analysis:** Generated Word Clouds for negative sentiment to pinpoint specific recurring "pain points" like "broken," "crash," or "fix"[cite: 1].

---

## 🛠️ Technical Stack
*   **Language:** Python 3.x
*   **Data Wrangling:** Pandas, NumPy[cite: 1]
*   **NLP Engine:** VADER Sentiment Intensity Analyzer[cite: 1]
*   **Visualization:** Matplotlib, Seaborn, WordCloud[cite: 1]
*   **Text Logic:** Regular Expressions (Regex)[cite: 1]

---

## 💡 Key Insights & Findings
*   **Sentiment Drivers:** Word Clouds revealed that negative sentiment is frequently driven by technical failures (e.g., "broken," "fix"), providing a direct feedback loop for product development[cite: 1].
*   **Brand Reputation:** By calculating average scores, we can objectively measure brand performance beyond simple mention counts[cite: 1].
*   **Preprocessing Impact:** A significant portion of social media data is "Irrelevant," proving that raw feeds require heavy filtering for accurate business intelligence[cite: 1].

---

## 📂 File Structure
```text
├── twitter_training.csv           # Raw training dataset
├── twitter_validation.csv         # Validation dataset
├── Detailed_Sentiment_Report.pdf  # Comprehensive analytical report[cite: 1]
├── sentiment_analysis.ipynb       # Main Jupyter Notebook with full implementation
└── README.md                      # Project documentation (this file)
```
# ⚙️ Installation & Usage
Clone the Repository:

```Bash
git clone [https://github.com/yourusername/sentiment-analysis-task.git](https://github.com/yourusername/sentiment-analysis-task.git)
```
Install Dependencies:
```Bash
pip install pandas seaborn matplotlib vaderSentiment wordcloud
```
3. **Execute Analysis:**
```Bash
    Open `sentiment_analysis.ipynb` in Jupyter Notebook or VS Code and run all cells to generate the reports and visualizations.
```
---
**Project completed as part of the Prodigy InfoTech Data Science Internship (Task-04).**
