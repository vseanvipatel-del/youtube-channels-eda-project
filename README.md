# youtube-channels-eda-project
# Top 5000 YouTube Channels - Exploratory Data Analysis (EDA)

This repository contains a comprehensive Exploratory Data Analysis (EDA) project on the **Top 5000 YouTube Channels** dataset. Utilizing Python's data science ecosystem (**Pandas**, **NumPy**, and **Seaborn**), this analysis uncovers relationships between channel performance indicators such as total uploads, subscriber counts, video views, and platform-assigned grades.

## 📌 Project Overview
The workflow emphasizes **advanced data cleaning and type conversion**. Raw web-scraped data often contains structural impurities (such as metric abbreviations, string patterns in ranks, commas, and null placeholders). This project showcases how to systematically convert these unstructured properties into functional datatypes to perform deep statistical aggregation and correlation analyses.

---

## 📊 Dataset Reference
The pipeline processes the original dataset file:
* **Source Dataset File:** `6-top-5000-youtube-channels.csv`

### Dataset Features:
* **Rank:** Channel standing based on platform traffic.
* **Grade:** Performance evaluation tier (e.g., `A++`, `A+`, `A`, `B+`).
* **Channel name:** The identifier of the YouTube channel.
* **Video Uploads:** The total number of videos published by the channel.
* **Subscribers:** Total subscriber audience base.
* **Video views:** The aggregate lifetime views across all uploads.

---

## 🧼 Data Cleaning & Transformation Pipeline
A substantial portion of this project focuses on robust data pre-processing:
* **Null Identification:** Substituted missing value string placeholders (`'--'`) with `NaN` markers and handled them appropriately.
* **Rank Column Transformation:** Handled string ordinal suffixes (e.g., transforming `1st`, `2nd` to numeric forms) and removed punctuation commas to cast the data into an operational `int` datatype.
* **Feature Type Casting:** Cleaned and cast both `Video Uploads` and `Subscribers` features from raw object types into workable numerical integers.
* **Categorical Encoding:** Standardized and stripped the `Grade` tiers to map them into a logical, sequential ordinal scale (`1` to `5`) for advanced analytics.

---

## 🔍 Analytical Milestones
The codebase answers several quantitative business questions:

1. **Flexible Snapshots:** Displaying dynamic filtered records using head/tail techniques based on dataset dimension offsets.
2. **Metadata Auditing:** Extraction of dataset structural matrices, active types, and tracking missing value distributions via `sns.heatmap`.
3. **Channel Performance Baselines:** Computing statistical centroids and calculating the absolute average video views across specific channels.
4. **Volume Leaders:** Filtering and sorting the top 5 most active YouTube creators based on total raw content generation (`Video Uploads`).
5. **Feature Correlation Matrix:** Building a linear correlation evaluation grid between Uploads, Subscribers, and Lifetime Views to assess growth drivers.
6. **Grade Tier Slicing:** Grouping platform grades to isolate which performance tier maximizes:
    * Peak content production volume (`Video Uploads`).
    * Top average audience consumption patterns (`Video views`).
    * Maximum audience acquisition capacity (`Subscribers`).

---

## 🛠️ Tech Stack & Dependencies
Ensure your workspace includes the following active dependencies:
* **Python** 3.8+
* **Pandas**
* **NumPy**
* **Seaborn**
* **Matplotlib**
* **Jupyter Notebook**

Install requirements via `pip`:
```bash
pip install pandas numpy seaborn matplotlib jupyter
