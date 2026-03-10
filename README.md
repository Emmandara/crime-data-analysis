# UK Crime Data Analysis & Socioeconomic Dashboard

**Author:** Emmanuel Oloruntola  
**Project Type:** Exploratory Data Analysis + Data Preparation for Stakeholder Dashboard  
**Tools Used:** Python, Pandas, Matplotlib, Seaborn  
**Data Sources:** UK Police Open Data, ONS Housing Data, IMD Deprivation Index

---

# Project Overview

This project explores **UK street-level crime patterns (2023–2024)** across multiple police forces and prepares a **clean analytical dataset** combining crime data with socioeconomic indicators.

The analysis was conducted to support **housing and real-estate decision making**, helping stakeholders understand how **crime, deprivation, housing prices, and employment indicators interact across regions.**

The project is divided into two main phases:

1. **Exploratory Data Analysis (EDA)** — understanding crime patterns across police forces.
2. **Data Cleaning & Integration** — preparing a structured dataset for dashboard development.

---

# Key Objectives

- Analyse crime trends across major UK police forces.
- Identify the most common crime types.
- Detect seasonal patterns in crime activity.
- Prepare a **Local Authority District (LAD) level dataset** for stakeholder analysis.
- Combine crime data with:
  - Deprivation scores
  - Housing prices
  - Claimant unemployment rates

---

# Data Sources

| Dataset | Description |
|------|------|
| UK Police Street Level Crime | Monthly crime records (2023–2024) |
| Index of Multiple Deprivation (IMD) | Socioeconomic deprivation scores |
| ONS House Price Statistics | Median housing prices |
| Claimant Rate Dataset | Local unemployment indicator |

All crime data was sourced from:

**https://data.police.uk**

---

# Exploratory Data Analysis

The initial analysis compared **four police forces:**

- Metropolitan Police
- West Midlands Police
- Leicestershire Police
- City of London Police

## Major Findings

### 1. Crime Volume by Region
- **Metropolitan Police** recorded the highest crime volume.
- **West Midlands Police** had the second highest.
- **City of London Police** recorded the lowest due to its small residential population.

### 2. Most Common Crime Types

Top crime categories included:

1. Violence and Sexual Offences
2. Theft Related Crimes
3. Shoplifting
4. Anti-social Behaviour

Violence-related offences consistently represented the **largest share of crimes across all forces.**

### 3. Seasonal Crime Patterns

Crime trends show **seasonal increases during summer months**.

Possible drivers include:

- Increased tourism
- More outdoor activity
- Higher retail activity

Shoplifting in particular shows **strong summer spikes.**

---

# Data Cleaning & Preparation

Before building the dashboard dataset, extensive preprocessing was performed.

## Crime Data Cleaning

Steps included:

- Removed rows missing **latitude or longitude**
- Converted **month column to datetime**
- Trimmed whitespace from text fields
- Standardised text formatting
- Removed duplicate crime IDs

---

# Socioeconomic Data Processing

## IMD (Deprivation Index)

- Selected relevant columns only
- Standardised Local Authority names
- Filtered for study region
- Aggregated LSOA scores to **LAD level using mean**

---

## House Price Data

- Removed rows with missing values
- Standardised LAD names
- Aggregated prices to **median LAD house price**

---

## Claimant Rate Data

- Selected latest month available
- Removed summary rows
- Converted values to numeric
- Standardised LAD naming format

---

# Dataset Integration

All datasets were merged using a common key:
