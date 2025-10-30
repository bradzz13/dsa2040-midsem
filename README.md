# DSA2040 Mid-Semester Exam Project — Extract & Transform (ET)

## 1. Project Overview
This project was developed as part of the DSA2040 Mid-Semester examination.  
The objective was to **extract** and **transform** a raw dataset to prepare it for further analytics and visualization.  

The tasks include:
- Importing and exploring the dataset
- Cleaning and handling missing values
- Standardizing data types and column names
- Creating new derived fields
- Exporting transformed data for future analysis


## 2. Data Source
Dataset provided via course materials.

**Description:**
- Contains records relevant to the exam dataset
- Includes multiple variables for processing, cleaning, and transformation
- Used to demonstrate core ET concepts


- 🔗 Dataset link: `(https://www.kaggle.com/datasets/sahilprajapati143/retail-analysis-large-dataset)



## 3. ET Phases

### ✅ Extract
- Loaded dataset into Python using **Pandas**
- Inspected structure with `.info()` and `.head()`
- Validated row/column counts

### ✅ Transform
Performed multiple transformation steps, including:
- Renaming columns for consistency
- Removing duplicates
- Handling missing/null values
- Changing data types
- Creating new features (derived attributes)
- Filtering out invalid/unwanted records
- Exporting the cleaned dataset into a new CSV

---

## 4. Tools Used
This project was built using:

| Tool | Purpose |
|------|---------|
| Python | Core programming |
| Pandas | Data manipulation & transformation |
| Jupyter Notebook | Environment for development & testing |

---
## 5 Load & Verification

### Format Used
For this phase, both **SQLite** and **Parquet** formats were used to load the transformed datasets.

- **SQLite files** were stored in:  
  `loaded/full_data.db` and `loaded/incremental_data.db`
- **Parquet files** were stored in:  
  `loaded/full_data.parquet` and `loaded/incremental_data.parquet`

### Verification
Below is a sample code snippet that verifies data loading for both formats:

```python
import sqlite3, pandas as pd

# SQLite Verification
conn = sqlite3.connect('loaded/full_data.db')
pd.read_sql('SELECT * FROM full_data LIMIT 5', conn)

# Parquet Verification
pd.read_parquet('loaded/full_data.parquet').head()


author ~ bradley ochola 346
```bash
git clone https://github.com/bradzz13/dsa2040-midsem.git
