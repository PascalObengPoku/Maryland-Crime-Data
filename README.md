# Maryland Crime Data Analysis (1975 - 2020)

## Project Overview
This project performs a comprehensive exploratory data analysis (EDA) of crime statistics across Maryland jurisdictions. Using a dataset of 1,104 records and 38 variables, the analysis tracks crime trends, identifies geographic hotspots, and evaluates the correlation between population growth and various crime categories.

## Dataset Description
- **Source:** Maryland Open Data / Uniform Crime Reporting (UCR).
- **Timeframe:** 1975 – 2020.
- **Scope:** 1,104 entries covering major Maryland jurisdictions.
- **Key Features:** Population, Violent Crime (Murder, Rape, Robbery, Assault), Property Crime (Burglary, Larceny, M/V Theft), and calculated crime rates per 100,000 people.

## Data Cleaning & Preprocessing
To ensure the integrity of the analysis, the following cleaning steps were performed using Python and Pandas:

1. **Handling Missing Values:** 
   - Identified 24 missing entries (~2%) in the `PERCENT CHANGE` columns.
   - Applied `df.dropna(subset=['PERCENT_CHANGE'])` or mean-imputation where appropriate to maintain statistical consistency.
2. **Column Standardization:**
   - Sanitized column names by replacing spaces and special characters (e.g., `B & E` to `B_AND_E`, `AGG. ASSAULT` to `AGG_ASSAULT`) to prevent syntax errors during coding.
3. **Data Type Correction:** 
   - Verified that `YEAR` and `POPULATION` were stored as integers, while all `RATE` and `PERCENT` columns were cast to floats for precise calculation.
4. **Feature Engineering:**
   - Created a `DIFFERENCE` column to validate the accuracy of the reported `PERCENT_CHANGE` against raw crime counts.
5. **Filtering:**
   - Segmented data by `YEAR == 2020` to isolate the most recent "hotspot" trends from historical averages.

## Key Findings
- **Dominant Crime Types:** Larceny Theft and Burglary (B&E) represent the highest volume of incidents historically.
- **Primary Hotspots:** Baltimore City and Prince George's County consistently lead in both total volume and per-capita crime rates.
- **Population Correlation:** Total crime volume scales with population (r ≈ 0.9+), but crime *rates* show significant variance in smaller jurisdictions (e.g., Worcester County) due to seasonal population shifts.

## Tools & Technologies Used
- **Python 3.x**
- **Pandas:** Data manipulation and cleaning.
- **Matplotlib & Seaborn:** Data visualization.


## Visualization
- Crime By Year
  ![Crime By Year](https://github.com/PascalObengPoku/Maryland-Crime-Data/blob/main/visualization/Crime%20By%20Year.png)
- Crime Distribution By Type
  ![Crime Distribution By Type](https://github.com/PascalObengPoku/Maryland-Crime-Data/blob/main/visualization/Total%20Crime%20Rate%20In%20Maryland%20By%20Type.png)
- Top 5 Dangerous Jurisdictions
![Top 5 Dangerous Jurisdictions](https://github.com/PascalObengPoku/Maryland-Crime-Data/blob/main/visualization/Top%205%20Dangerous%20Jurisdictions.png)

## Author
Pascal Obeng-Poku

Data Analyst

Github: http://github.com/PascalObengPoku

Linkedin: http://Linkedin.com/in/PascalObengPoku

Email: pascalobengpoku [at] gmail [dot] com


