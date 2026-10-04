# IBM Data Analyst Professional Certificate Capstone Project

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![IBM Cognos](https://img.shields.io/badge/IBM%20Cognos-05122A?style=for-the-badge&logo=ibm&logoColor=white)

---

## 📌 Executive Summary
In this capstone project, I assumed the role of a Data Analyst at an IT consulting firm to evaluate technology adoption trends and demographic distributions across the global developer community. 

The objective of this analysis is to provide corporate stakeholders with actionable insights to inform strategic decisions regarding:
* **Internal Training & Upskilling:** Identifying emerging programming languages, databases, and frameworks that justify corporate training budget allocations.
* **Talent Acquisition & Global Sourcing:** Leveraging developer geographic and demographic trends to optimize global recruitment pipelines and remote sourcing.

---

## 💡 Key Analytical Insights

### 1. Programming Languages & Frameworks
* **Web Engineering Baseline:** Core web technologies (**JavaScript**, **HTML/CSS**) maintain a dominant baseline across engineering teams.
* **AI & Data Science Growth:** A steady rise in **Python** usage underscores an industry-wide acceleration toward Data Science, AI, and Machine Learning workflows.
* **Mobile Stack Demand:** Declarative modern languages like **Kotlin** are experiencing increased adoption for native and cross-platform mobile development.

### 2. Database Systems
* **Modernization Trends:** Traditional relational databases (MySQL, Microsoft SQL Server) show declining momentum, while modern relational and NoSQL engines like **PostgreSQL** and **MongoDB** demonstrate strong adoption growth.
* **Legacy Systems:** Interest in legacy enterprise databases such as **Oracle** continues to decline in favor of open-source and flexible solutions.

### 3. Developer Demographics & Geography
* **Geographic Concentration:** Developer talent remains heavily concentrated in the **United States** and **India**, marking prime regions for tech hub expansion or distributed engineering teams.
* **Gender Representation:** A significant gender disparity exists within the developer population (**93.5% Male** vs. **6.5% Female**), highlighting key opportunities for targeted diversity initiatives and inclusive hiring strategies.

---

## 🛠️ Data Pipeline & Methodology

### Phase 1: Data Collection & Extraction
* Extracted job posting datasets using REST APIs from Kaggle's *Jobs on Naukri.com* repository.
* Programmatically scraped live programming language and salary benchmark tables using Python (`BeautifulSoup` / `requests`).
* Ingested and integrated developer survey data from the *Stack Overflow Developer Survey*.

### Phase 2: Data Cleaning & Wrangling
* Purged duplicate entries to maintain statistical integrity.
* Imputed missing values across numerical and categorical columns using median and mode imputation strategies.
* Standardized compensation fields (`CompFreq` and `CompTotal`) into a normalized **Annual Salary ($USD)** variable for direct cross-developer analysis.

### Phase 3: Exploratory Data Analysis (EDA)
* Identified and removed salary outliers using Interquartile Range (IQR) bounds to prevent skewed distribution metrics.
* Evaluated correlation matrices across developer experience, age, compensation, and technology stacks.

### Phase 4: Business Intelligence & Visualization
Designed interactive executive dashboards in **IBM Cognos Analytics**, categorized into three strategic views:
1. **Current Technology Usage:** Visualized top languages, databases, web frameworks, and operating platforms currently worked with.
2. **Future Technology Trends:** Comparative analysis highlighting top desired technologies (languages, databases, frameworks, platforms) for the upcoming year.
3. **Demographics:** Visual breakdowns of gender representation, respondent distribution by country, age distributions, and formal education levels.

---

## 📂 Repository Structure

```text
.
├── 0_Jobs_API.ipynb                              # API extraction of job market datasets
├── 1.1_Collecting_Jobs_Data_Using_API.ipynb      # API data collection pipeline
├── 1.2_Collecting_Pragramming_Language_Data...   # Web scraping script for language & salary data
├── 1.3_Exploring_DataSet.ipynb                   # Initial data inspection and structural audit
├── 2_Data_Wrangling.ipynb                        # Data cleaning, missing value imputation & salary normalization
├── 3_Exploratory_Data_Analysis.ipynb             # Outlier treatment, distribution plots & correlation analysis
├── 4_Data_Visualization_Using_Python.ipynb      # Initial visual data analysis in Python
├── 5_IBM_Cognos_Dashboards.pdf                   # Final executive dashboard exports & visual reports
