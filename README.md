## 🧠 Search Queries Anomaly Detection using Python

### 📌 Overview

This project detects **anomalies in Google Search performance data** using **Isolation Forest**, a machine learning algorithm for outlier detection.
It focuses on identifying unusual trends in **CTR (Click-Through Rate)**, **Impressions**, and **Average Position**, helping SEO analysts and marketers quickly detect performance issues or unexpected ranking changes.

---

### 📊 Sample Dataset

Example subset of the dataset used:

| Top Queries                               | Clicks | Impressions | CTR    | Position |
| ----------------------------------------- | ------ | ----------- | ------ | -------- |
| number guessing game python               | 5223   | 14578       | 35.83% | 1.61     |
| python projects with source code          | 2077   | 73380       | 2.83%  | 5.94     |
| classification report in machine learning | 2012   | 4959        | 40.57% | 1.28     |
| python turtle graphics code               | 1455   | 13585       | 10.71% | 4.6      |
| guess the number python                   | 1287   | 4569        | 28.17% | 2.36     |

The goal is to identify **outlier queries** whose CTR or ranking deviates from normal search trends.

---

### ⚙️ Project Workflow

#### 1. **Data Collection**

* Exported Google Search Console data to CSV.
* Columns include `Top Queries`, `Clicks`, `Impressions`, `CTR`, and `Position`.

#### 2. **Data Preprocessing**

* **Handle missing or inconsistent values**.
* **Convert CTR from percentage strings to numeric values** for model analysis.

#### 3. **Exploratory Analysis**

* Frequency analysis using `Counter` to understand top and rare search queries.
* Text cleaning and normalization with **regex (`re`)** to ensure uniform query format.

#### 4. **Anomaly Detection (Isolation Forest)**

* Applied **`sklearn.ensemble.IsolationForest`** to detect anomalies in CTR and Position.
* The model isolates outliers that show abnormal ranking or CTR fluctuations.
* Results highlight which queries may require SEO review or optimization.

#### 5. **Visualization**

* Built interactive visualizations using **Plotly Express** and **Plotly IO**.
* Plots highlight anomalies directly on CTR or ranking distribution charts.

#### 6. **Output and Insights**

* Anomalies displayed with visual markers.
* Results can be exported or saved for reporting and SEO monitoring.

---

### 🧩 Key Features

✅ Isolation Forest-based anomaly detection
✅ Automated preprocessing of search query metrics
✅ Regex-based query cleaning
✅ Interactive Plotly visualizations
✅ Ready-to-run Jupyter Notebook implementation

---

### 🧰 Tech Stack

* **Language:** Python
* **Libraries:** `pandas`, `plotly`, `scikit-learn`, `re`, `collections`
* **Environment:** Jupyter Notebook
* **Dataset Source:** Google Search Console

---

### 🚀 How to Run

#### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-username>/search-queries-anomaly-detection.git
cd search-queries-anomaly-detection
```

#### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

#### 3️⃣ Run the Notebook

```bash
jupyter notebook "Search Queries Anomaly Detection using Python.ipynb"
```

#### 4️⃣ View Results

* Visualizations and anomaly tables appear in the notebook.
* You can export the anomalies list for further SEO insights.

---

### 🧪 Future Enhancements

* Integrate Google Search Console API for real-time updates.
* Build a Streamlit dashboard for daily anomaly reporting.
* Add automated email alerts for severe CTR drops.

