# Customer_behavior_Analysis
Data Analytics project showcasing customer behavior analysis using python, sql and power bi
# 📊 Data Analytics Project

## 📌 Overview

This project demonstrates an end-to-end **Data Analytics workflow**, starting from raw data and transforming it into meaningful business insights.

The project covers:

* Loading and exploring a dataset using **Python**
* Performing **Exploratory Data Analysis (EDA)**
* Cleaning and preprocessing the data
* Analyzing data using **SQL**
* Working with **PostgreSQL / MySQL**
* Creating an interactive **Power BI Dashboard**
* Preparing a detailed analytical **Report**
* Creating a project presentation using **Gamma**

The goal is to understand the dataset, identify important patterns and trends, and present the findings through clear visualizations and business insights.

---

## 📂 Dataset

The project uses a structured CSV dataset containing customer/business-related information.

### Dataset includes:

* Customer information
* Purchase/transaction details
* Product information
* Ratings and other relevant attributes
* Business-related metrics

> **Dataset :[**"customer_shopping_behavior.csv"]

The raw dataset is stored in the `data/` folder.

---

## 🛠️ Tools & Technologies

| Tool                     | Purpose                                   |
| ------------------------ | ----------------------------------------- |
| **Python**               | Data loading, analysis and preprocessing  |
| **Pandas**               | Data manipulation                         |
| **NumPy**                | Numerical operations                      |
| **Matplotlib / Seaborn** | Data visualization                        |
| **PostgreSQL / MySQL**   | SQL-based data analysis                   |
| **Power BI**             | Interactive dashboard                     |
| **Gamma**                | Project presentation                      |
| **Jupyter Notebook**     | Python analysis                           |
| **GitHub**               | Project documentation and version control |

---

# 🔄 Project Workflow

```text
Raw Dataset
     ↓
Load Data in Python
     ↓
Data Exploration
     ↓
Data Cleaning & Preprocessing
     ↓
EDA & Visualization
     ↓
Load Data into PostgreSQL / MySQL
     ↓
SQL Analysis
     ↓
Power BI Dashboard
     ↓
Business Report
     ↓
Gamma Presentation
```

---

# 1️⃣ Data Loading

The dataset was first loaded into Python using **Pandas**.

```python
import pandas as pd

df = pd.read_csv("Customer_shopping_behavior.csv"")

print(df.head())
print(df.shape)
print(df.columns)
```

The initial analysis helped understand:

* Number of rows and columns
* Column names
* Data types
* Missing values
* Duplicate records
* Basic statistics

---

# 2️⃣ Exploratory Data Analysis (EDA)

EDA was performed to understand the structure and patterns in the dataset.

### Key EDA activities:

* Checking dataset shape
* Understanding data types
* Identifying missing values
* Checking duplicate records
* Analyzing numerical columns
* Analyzing categorical columns
* Studying distributions
* Identifying trends and patterns
* Creating visualizations

Example:

```python
df.info()
df.describe()
df.isnull().sum()
df.duplicated().sum()
```

Visualizations were created using **Matplotlib and Seaborn** to understand relationships and trends within the data.

---

# 3️⃣ Data Cleaning

The raw dataset was cleaned before performing SQL analysis and dashboard development.

### Data cleaning steps included:

* Handling missing values
* Removing duplicate records
* Correcting data types
* Standardizing categorical values
* Handling inconsistent data
* Checking invalid or unusual values
* Preparing the final dataset for analysis

Example:

```python
df = df.drop_duplicates()

df['column_name'] = df['column_name'].fillna(0)
```

The cleaned dataset was then prepared for database analysis.

---

# 4️⃣ SQL Analysis

The cleaned data was loaded into **PostgreSQL / MySQL** for structured analysis.

SQL was used to answer business-related questions and generate useful insights.

### SQL concepts used:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `HAVING`
* `ORDER BY`
* `LIMIT`
* Aggregate functions
* `CASE`
* Subqueries
* Joins
* CTEs

Example:

```sql
SELECT 
    item_purchased,
    ROUND(AVG(review_rating), 2) AS average_rating
FROM customer
GROUP BY item_purchased
ORDER BY average_rating DESC
LIMIT 5;
```

SQL analysis helped identify important metrics, top-performing categories/products, customer behavior, and other business patterns.

---

# 5️⃣ Power BI Dashboard

The cleaned and analyzed data was used to build an interactive **Power BI Dashboard**.

### Dashboard includes:

* Key Performance Indicators (KPIs)
* Trend analysis
* Category/product analysis
* Customer analysis
* Sales/revenue metrics
* Interactive filters and slicers
* Charts and visualizations

### Dashboard Features

* 📌 KPI Cards
* 📊 Bar Charts
* 📈 Trend Charts
* 🥧 Category Analysis
* 🔎 Interactive Filters
* 📋 Summary Tables

The dashboard allows users to interact with the data and quickly identify important business insights.

---

## 📊 Dashboard Preview

> Add your Power BI dashboard screenshot here.

```text
![Power BI Dashboard](images/dashboard.png)
```

---

# 6️⃣ Business Report

A detailed report was created to summarize the analysis and findings.

The report covers:

### Executive Summary

A brief overview of the project and major findings.

### Data Analysis

Explanation of the dataset, cleaning process, and analytical approach.

### Key Insights

Important trends, patterns, and observations discovered during the analysis.

### Business Recommendations

Actionable recommendations based on the analytical findings.

---

# 7️⃣ Project Presentation

A presentation was created using **Gamma** to communicate the project in a clear and professional format.

The presentation covers:

1. Project Introduction
2. Business Problem
3. Dataset
4. Data Cleaning
5. EDA
6. SQL Analysis
7. Power BI Dashboard
8. Key Insights
9. Recommendations
10. Conclusion

---

# 📈 Key Results

The project helped convert raw data into meaningful business insights.

### Major outcomes:

* Identified important trends and patterns
* Improved data quality through cleaning
* Used SQL to answer analytical questions
* Built an interactive Power BI dashboard
* Generated business-focused insights
* Created a professional analytical report
* Presented the complete analysis using Gamma

> **Note:** Add your actual numerical findings here, for example:
>
> * Identified the top 5 products/categories
> * Found the highest-performing customer segment
> * Identified major sales trends
> * Analyzed average ratings and purchase behavior

---

# 🚀 How to Run

## Step 1 — Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git
```

```bash
cd your-repository
```

## Step 2 — Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy psycopg2-binary
```

If you are using MySQL:

```bash
pip install mysql-connector-python
```

## Step 3 — Open the Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook from the `notebooks/` folder.

## Step 4 — Add the Dataset

Place the dataset inside:

```text
data/
```

Example:

```text
data/dataset.csv
```

## Step 5 — Configure the Database

Update your database connection details in the Python/SQL section.

### PostgreSQL example:

```python
from sqlalchemy import create_engine

engine = create_engine(
    "postgresql+psycopg://username:password@localhost:5432/database_name"
)
```

### MySQL example:

```python
engine = create_engine(
    "mysql+mysqlconnector://username:password@localhost/database_name"
)
```

## Step 6 — Run the Analysis

Run the notebook cells in order:

```text
Data Loading
     ↓
EDA
     ↓
Data Cleaning
     ↓
Database Loading
     ↓
SQL Analysis
```

## Step 7 — Open Power BI

Import/connect the cleaned dataset or database into Power BI and open the dashboard file from the `powerbi/` folder.

---

# 📁 Project Structure

```text
Data-Analytics-Project/
│
├── data/
│   └── dataset.csv
│
├── notebooks/
│   └── data_analysis.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── powerbi/
│   └── dashboard.pbix
│
├── report/
│   └── analytical_report.pdf
│
├── presentation/
│   └── project_presentation.pdf
│
└── README.md
```

---

# 🎯 Skills Demonstrated

This project demonstrates practical experience in:

* **Python for Data Analytics**
* **Pandas & NumPy**
* **Exploratory Data Analysis**
* **Data Cleaning**
* **SQL**
* **PostgreSQL / MySQL**
* **Power BI**
* **Data Visualization**
* **Business Analysis**
* **Data Storytelling**
* **Report Preparation**
* **Presentation Development**

---

# 💡 Conclusion

This project demonstrates an end-to-end approach to solving a data analytics problem — from **raw data collection and cleaning to SQL analysis, visualization, dashboard development, and business reporting**.

It showcases the ability to transform raw datasets into **actionable insights** using commonly used industry tools and technologies.

---

## 👤 Author

**Lachi Rakesh Meshram**

B. Tech – Information Technology

**Interested in:** Data Analytics | Business Intelligence | Python | SQL | Power BI

---

⭐ If you found this project useful, consider giving the repository a star!
