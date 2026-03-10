# UK Crime Data Analysis for Real Estate Decision Making

**Author:** Emmanuel Oloruntola  
**Tools Used:** Python, Pandas, Matplotlib, Seaborn, Power BI  
**Project Type:** Exploratory Data Analysis + Data Enrichment + Business Intelligence  
**Stakeholder:** Nadine Green – Head of Sales  

---

# Project Overview

This project analyses **UK street-level crime data** to support decision-making within a real estate company.

The stakeholder, **Head of Sales Nadine Green**, requested an analysis to understand **which regions in the UK are most and least desirable** based on crime trends and related socioeconomic factors.

Understanding crime levels is important when evaluating **property investment opportunities, sales strategy, and regional desirability**.

The project was completed in **two phases**:

- **Part 1 – Exploratory Data Analysis (EDA)**
- **Part 2 – Data Enrichment and Business Reporting**

---

# Business Problem

Real estate companies must consider multiple factors when evaluating locations, including:

- Crime levels
- Socioeconomic conditions
- Employment indicators
- Property prices

The objective of this project was to analyse crime across several UK regions and identify patterns that could help guide **property sales and investment decisions**.

---

# Data Source

Primary dataset:

UK Police Open Data  
https://data.police.uk/data/

This dataset provides **monthly street-level crime records across UK police forces**.

---

# Part 1 – Exploratory Data Analysis

The first stage focused on understanding **crime patterns across multiple police forces**.

### Requirements

- Analyse **at least 4 police forces**
- Use **at least 2 years of crime data**
- Analyse **street crime datasets**
- Investigate crime distributions and patterns
- Explore **time trends**
- Produce visualisations using Python

### Police Forces Analysed

- Metropolitan Police
- West Midlands Police
- Leicestershire Police
- City of London Police

### Key Exploratory Analysis

The analysis explored:

- Crime distribution by police force
- Top crime categories
- Monthly crime trends
- Seasonal crime patterns
- Comparative regional analysis

### Key Findings

Some early insights included:

- The **Metropolitan Police** recorded the highest crime volume.
- **City of London Police** recorded the lowest due to its small residential population.
- **Violence and sexual offences** were the most common crime category.
- Crime shows **seasonal increases during summer months**.

### Outcome of Part 1

The exploratory analysis identified **two police forces for deeper analysis**:

- **West Midlands Police**
- **Leicestershire Police**

These forces were selected because they provide a useful comparison between:

- **Large metropolitan environments**
- **Mixed urban-rural regions**

---

# Part 2 – Data Enrichment and Reporting

The second phase expanded the analysis by incorporating **additional datasets** to provide deeper insight into regional conditions.

### Additional Data Sources

The following datasets were integrated:

| Dataset | Purpose |
|------|------|
| Index of Multiple Deprivation (IMD) | Measures socioeconomic deprivation |
| ONS House Price Statistics | Median property values |
| Claimant Rate Data | Employment indicator |

These datasets help analyse relationships between:

- Crime levels
- Deprivation
- Housing prices
- Employment conditions

---

# Data Cleaning & Processing

Data preprocessing was performed in **Python using Pandas**.

### Crime Data Cleaning

- Removed rows missing latitude or longitude
- Converted month column to datetime
- Trimmed whitespace from text fields
- Standardised text formatting
- Removed duplicate records

### IMD Data Processing

- Selected relevant columns
- Standardised Local Authority District names
- Aggregated LSOA scores to **LAD level**

### House Price Data

- Removed missing values
- Aggregated prices to **median house price per LAD**

### Claimant Rate Data

- Selected latest month available
- Converted values to numeric
- Standardised Local Authority names

---

# Data Integration

All datasets were merged using a common key:


lad_clean


Merge order:

1. Crime dataset
2. Deprivation dataset
3. House price dataset
4. Claimant rate dataset

The final dataset was aggregated at **Local Authority District (LAD) level**.

---

# Final Analytical Dataset

The cleaned dataset includes the following fields:

| Column | Description |
|------|------|
| lad_name | Local Authority District |
| crime_count | Total recorded crimes |
| median_house_price | Median property price |
| imd_score | Average deprivation score |
| claimant_rate | Local unemployment indicator |

The final dataset was exported as:


lad_summary_clean.csv


---

# Dashboard

A **self-serve dashboard** was built to allow stakeholders to explore the data interactively.

The dashboard enables users to analyse:

- Crime levels by region
- Relationships between crime and deprivation
- Property price distribution
- Employment indicators by area

The goal is to provide **data-driven insights for real estate decision making**.

---

# Visualisations

The analysis includes multiple visualisations created in Python, including:

- Crime by police force
- Top crime categories
- Monthly crime trends
- Seasonal crime patterns
- Regional comparisons

---

# Project Structure


crime-data-analysis
│
├── notebooks
│ ├── data_preprocessing.ipynb
│ └── crime_eda_analysis.ipynb
│
├── data
│ ├── raw
│ └── processed
│
├── reports
│ ├── EDA_Report
│ └── Data_Cleaning_Report
│
├── dashboard
│ └── powerbi_dashboard.pbix
│
└── README.md


---

# Limitations

- Some crime records contained missing geographic coordinates.
- Crime counts vary significantly due to **population differences between regions**.
- Some datasets required aggregation from **LSOA to LAD level**, which may smooth local variation.

---

# Future Improvements

Potential extensions to this project include:

- Adding **population density data**
- Expanding analysis to **more police forces**
- Building **crime prediction models**
- Performing **geospatial hotspot analysis**
- Automating data updates for **continuous reporting**

---

# Author

**Emmanuel Oloruntola**

Aspiring Data Analyst focused on using data to support **real-world business decisions in property, urban environments, and public policy.**

---

# Data License

All data used in this project is publicly available from UK government sources.

https://data.police.uk
