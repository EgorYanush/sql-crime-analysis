# SQL Crime Data Analysis in Israel (2018–2023)

## 🌟 Overview

This project is a final assignment for a college SQL course. It analyzes crime trends in the Haifa district of Israel using publicly available data. The project includes data loading, SQL queries, and insights based on crime records between 2018 and 2023.

## 📂 Data

* **Source**: [data.gov.il](https://data.gov.il/dataset/crime_records_data)
* **Scope**: Subset of data filtered by police district
* **Format**: CSV files hosted on GitHub
* **Example Columns**:

  * `PoliceDistrict`
  * `PoliceStation`
  * `Quarter` (e.g. Q1 2022)
  * `StatisticCrimeGroup`, `StatisticCrimeType`
  * `TikimSum` (total number of cases)

## 🤝 Methodology

* Work done in **Google Colab** using **Python** and **pandas**
* Data pulled from GitHub using **GitPython**
* SQL logic written with **pandasql** or SQLite
* Notebook contains full pipeline: load data, clean, query, analyze

## 📊 Key SQL Queries & Insights

Some examples of queries:

```sql
-- Total cases per district\SELECT PoliceDistrict, SUM(TikimSum) AS TotalCases
FROM CrimeData
GROUP BY PoliceDistrict
ORDER BY TotalCases DESC;

-- Yearly trends for top 5 crimes
SELECT Quarter, StatisticCrimeType, SUM(TikimSum)
FROM CrimeData
GROUP BY Quarter, StatisticCrimeType
ORDER BY Quarter;
```

## 🚀 How to Run

1. Open the notebook in [Google Colab](https://colab.research.google.com/github/EgorYanush/sql-crime-analysis/blob/main/draft1_Yanushkevich_Egor_sql.ipynb)
2. Follow instructions to install dependencies and fetch data
3. Run all cells to reproduce results

## 📄 Repository Structure

```
.
├── draft1_Yanushkevich_Egor_sql.ipynb  # Main notebook
├── README.md                            # Project documentation
├── requirements.txt                     # Python packages (optional)
```

## 📊 Results

* Identified top 5 crime categories by frequency
* Trends show seasonal spikes in property crimes
* Certain districts consistently rank higher in violent crime cases

## 🔬 Technologies Used

* SQL (via pandasql or SQLite)
* Python (pandas, GitPython)
* Google Colab
* GitHub for dataset access

## 🔧 Future Improvements

* Add data visualizations (e.g. bar charts, line graphs)
* Create interactive dashboard (e.g. Streamlit)
* Expand analysis with demographic or geographic overlays

## 📅 Time Frame

Project completed in July 2025 as part of college curriculum at Michlala Atid.

## 👍 Acknowledgments

* [data.gov.il](https://data.gov.il/dataset/crime_records_data)
* GitHub dataset mirror by [annakoopenu](https://github.com/annakoopenu/SQL_ATID_FINAL)

## ⚖️ License

This project is released for educational purposes.
