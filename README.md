
<div align="center">
  <h1>🛒 Customer Segmentation Using RFM Analysis 📊</h1>
  <p>
    <strong>Unlock the Power of Customer Data!</strong><br>
    <em>A Data Science Project to segment customers based on their purchasing behavior using RFM Analysis and K-Means Clustering.</em>
  </p>
</div>

---

## 📌 Table of Contents / Project Structure

Click on any section to jump directly to it:

*   [📂 Project Overview](#-project-overview)
*   [🛠️ Technologies Used](#%EF%B8%8F-technologies-used)
*   [📂 Dataset](#-dataset)
*   [⚙️ Analysis Workflow](#%EF%B8%8F-analysis-workflow)
    *   [1. Data Cleaning](#1-data-cleaning)
    *   [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
    *   [3. RFM Calculation](#3-rfm-calculation)
    *   [4. K-Means Clustering](#4-k-means-clustering)
*   [📈 Key Insights & Results](#-key-insights--results)
*   [🚀 How to Run](#-how-to-run)
*   [✍️ Author](#-author)
*   [License](#license-)
---

## 📖 Project Overview

This project focuses on identifying distinct customer segments for an online retail business. By analyzing transactional data, we group customers based on their purchasing habits to create targeted marketing strategies. We utilize **RFM Analysis** (Recency, Frequency, Monetary) combined with both rule-based segmentation and machine learning (**K-Means Clustering**).

---

## 🛠️ Technologies Used

The project is built using Python and the following powerful libraries:

*   **Pandas**: Data manipulation and analysis.
*   **NumPy**: Numerical computations.
*   **Matplotlib & Seaborn**: Data visualization (Histograms, Boxplots, Bar charts).
*   **Scikit-Learn**: Machine Learning (StandardScaler, K-Means Clustering).

---

## 📂 Dataset

The analysis is based on the **Online Retail** dataset.
*   **File Path**: `Dataset/Online Retail.xlsx`
*   **Description**: Contains transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.

---

## ⚙️ Analysis Workflow

### 1. Data Cleaning
We start by ensuring high data quality:
*   **Missing Values**: Handling null values in `CustomerID` and `Description`.
*   **Duplicates**: Removing duplicate transactions to avoid skewing data.
*   **Data Types**: Converting `InvoiceDate` to datetime objects.

### 2. Exploratory Data Analysis (EDA)
We visualize the data to understand trends:
*   **Top Countries**: Identifying which countries have the most customers.
*   **Price Distribution**: Analyzing `UnitPrice` to detect outliers.
*   **Orders per Day**: Tracking transaction volume over time.

### 3. RFM Calculation
We compute the three key metrics for every customer:
*   **Recency (R)**: How many days ago was their last purchase?
*   **Frequency (F)**: How often do they buy?
*   **Monetary (M)**: How much do they spend?

*Scores (1-5) are assigned to each metric using Quantiles (`pd.qcut`).*

### 4. K-Means Clustering
We take it a step further with Machine Learning:
*   **Log Transformation**: To handle skewed data distribution.
*   **Scaling**: Using `StandardScaler` to normalize metrics.
*   **Elbow Method**: Determining the optimal number of clusters (`k`).
*   **Clustering**: Grouping customers into mathematical clusters.

---

## 📈 Key Insights & Results

Based on the RFM Scores, customers are categorized into segments such as:

| Segment | Description | Strategy |
| :--- | :--- | :--- |
| 🏆 **Champions** | High R, F, M scores. Bought recently, buy often, and spend the most. | Reward them. Can become early adopters of new products. |
| 💎 **Loyal Customers** | Good Frequency and Monetary scores. | Upsell higher value products. Ask for reviews. |
| ⚠️ **At Risk / Potential** | Aveage Recency, Frequency, and Monetary scores. | Send personalized emails to reconnect, offer renewals. |
| 💤 **Hibernating** | Low Recency, Frequency, and Monetary scores. | Recreate brand value, offer relevant discounts. |

---

## 🚀 How to Run

1.  **Clone the repository**.
2.  **Install dependencies**:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
    ```
3.  **Run the Notebook**:
    Open `notebook.ipynb` in Jupyter Notebook or VS Code and execute the cells sequentially.

---

## Author

- Name: **Mohamed Younis**

---

## License 📄

Add a license that matches how you want others to use your work (e.g., MIT).

<div align="center">
  <p><em>Created with ❤️ for Data Science Enthusiasts</em></p>
</div>

---



