# UK Crime Data – Exploratory Data Analysis (Part 1)

##  Project Overview
This project is Part 1 of a larger analytical workflow for understanding crime patterns in the UK to assist a real estate company.  
The goal is to extract, clean, and explore street-level crime data for a selection of police forces over a two-year period.  
The analysis aims to identify broad regional trends and ultimately select **two police forces** for deeper study in Part 2.

---

##  Objectives (from the project brief)

- Use **at least 4 UK Police forces**
- Use **at least 2 years** of crime data (2023–2024)
- Perform a clear and structured **Exploratory Data Analysis (EDA)**:
  - Crime distributions by type  
  - Regional comparisons  
  - Crime counts over time  
  - Top offence categories  
  - Map-based visualisation (hexbin / scatter)  
- Produce clean, readable preprocessing in Jupyter  
- Deliver a professional, coherent report summarising findings
- Select **two forces** for further analysis in later stages

---

##  Data Used

All data was obtained from the official UK Police service:

 https://data.police.uk/data/

**Forces used:**
1. Metropolitan Police  
2. West Midlands Police  
3. Leicestershire Police  
4. City of London Police  

**Time period:**  
**January 2023 – December 2024**

The following datasets were used:
- *Street-level crime* (main dataset)
- *Optional*: Outcomes dataset (not required )

---

##  Preprocessing Summary

Data cleaning was performed in a separate Jupyter notebook:
- Loaded multiple monthly CSV files  
- Removed unused columns  
- Standardised column names  
- Handled missing values in latitude/longitude  
- Extracted month/year    
- Verified dataset size and quality

---

##  Exploratory Data Analysis (EDA)

The EDA notebook includes:
- Total crimes by region  
- Crime type distributions  
- Top offence categories  
- Monthly trends (2023–2024)  
- Spatial visualisations  
- Comparisons between the four forces  

---

##  Key Findings (Part 1)

- The **Metropolitan Police** has by far the highest total crime counts.
- **West Midlands Police** shows strong urban clustering around Birmingham.
- **Leicestershire Police** presents moderate crime levels, mostly in Leicester city centre.
- **City of London Police** has very low volumes but specific business-district patterns.
- Crime trends remain relatively stable across 2023–2024.

###  Selected forces for further study:
**West Midlands Police** and **Leicestershire Police**

These were chosen because:
- They provide meaningful contrast (urban vs mixed urban–rural)
- They show clear spatial patterns suitable for deeper analysis
- They avoid the extreme outliers of Met (too large) and City of London (too small)

---

## Project Structure
Project_Folder/
│
├── data/
│ ├── raw/ # monthly crime CSVs
│ └── processed/ # cleaned combined dataset
│
├── notebooks/
│ ├── 01_preprocessing.ipynb
│ └── 02_eda.ipynb
│
├──Project Statement of Work
|
├──Flowchart
├── EDA_Report.pdf 
│
└── README.md

---

##  Tools Used
- Python (Pandas, Matplotlib, Seaborn)
- Jupyter Notebook
- Git / GitHub

---

##  Deliverables
- Preprocessing notebook  
- EDA notebook with visualisations  
- Full written report (PDF)  
- README (this file)  
