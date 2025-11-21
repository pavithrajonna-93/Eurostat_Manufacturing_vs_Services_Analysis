# Multi-country Manufacturing vs Services Analysis (EU, 2013-2020)
## Project Summary
This project analyzes the **Manufacturing** and **Services** sectros across six Eurpoean countries - 
**Germany, Italy, Netherlands, Sweden, Spain and France**
Using **Eurostat Structural Business Statistics (2005-2020)**

The study across two sectors compares:
1. **Average Growth(%)**
2. **Average Value** (Enterprise/Turnover/Production value)
3. **Volatility Range**
4. **Overall growth(%)**

The goal is to identify **Economic strengths, stability and sector-wise performance differences**

## Why this project?
Manufacturing and Services are the two economic pillars that define:
1. GDP contribution
2. Employment generation
3. Eport competitiveness
4. Market maturity

This comparative study helps identify:
1. High-Performing countries
2. Stable vs. volatile economies
3. Sectoral strengths
4. Growth potential for businesses

## This project demonstrated:
1. **Extracted and cleaned raw Eurostat data**
2. **Unpivoted** 6 sheets (3 manufacturing and 3 services)
3. **Ran SQL** to compute KPIs for each sector
4. **Merged all datasets in Python**
5. **Performed EDA** (Histogram, boxplots, Heatmap, Summary statistics)
6. **Created Sector-wise visual comparisons**
7. **Generated insights** for both industries
The result is a consolidated understanding of **Europe's manufacturing vs. service performance** from 2013 - 2020

## Data Sources 

## **Eurostat Strctural Business Statistics**
1. **Manufacturing Sector (NACE Rev. 2 B-E)**
   *Annual detailed enterprise statistics for industry(2005-2020)*
2. **Services Sector (NACE Rev. 2 G-N, S95)**
   *Annual detailed enterprise statistics for Services (2005-2020)*

Both datasets include:
1. Enterprise count
2. Turnover
3. Production value
4. Year-wise breakdown

## Final dataset shape
After cleaning final dataset contains 
1. **37 rows**
2. **7 columns**
3. Columns:
   - Country - Selected European Countries (Germany, Italy, Netherlands, Sweden, Spain, France)
   - Category - Enterprise/Turnover/Production value
   - Avg_growth_percent - Average Yoy growth across years
   - Avg_value - Average metric vakue (enterpirse count, turnoer or production)
   - Volatility_Range - Max-Min range across years
   - Overall_growth_percent - Total long-term growth (first vs last year)
   - Sector - Manufacturing or Services

Files in the /data folder includes:

**Manufacturing Datasets**
 - Raw_Manufacturing_enterprise_cleaned.xlsx
 - Raw_Manufacturing_turnover_cleaned.xlsx
 - Raw_Manufacturing_productionvalue_cleaned.xlsx
 - Manufacturing_Master-Manufacturing_Master.xlsx 
 - Manufacturing_final.xlsx
   
**Services Datasets**
 - Raw_services_enterprise.xlsx
 - Raw_services_turnover.xlsx
 - Raw_services_production_value.xlsx
 - Services_Master_services_Master.xlsx 
 - Services_final.xlsx
   
These cleaned datasets were used for:
 - SQL KPI Computation
 - Python Merging
 - EDA
 - Visualisation
   
# Why these countries?
Eurostat provides complete and consistent data only for the following six countries across all metrics:
 - Germany
 - Italy
 - Netherlands
 - Sweden
 - Spain
 - France
   
These countries also represent:
- Major EU economies
- Strong manufacturing and services mix
- Stable long-term data
- High research value for comparative analysis
  
## Tools and Technologies Used 
1. Google sheets(unpivot with ARRAYFORMULA, FLATTEN, SPLIT)
2.  Excel 
## SQL Analysis 
1. SQlite (DB Browser/Online SQLite editor)
2. SQL DDL + DML for:
   - Average growth (%)
   - Average value
   - Volatility range
   - Overall Growth (%)

## Python Analysis 
-  Google colab
-  Pandas
-  Numpy
-  Matplotlib
-  Seaborn
## Version control 
Git & Github

## Folder Structure 
This Repository follows a clean and professional structure for clarity, reproducibility and evaluation by universities/Recruiters.

# Project Layout 

1. README.md
2. data/ - contains raw and cleaned CSVs
  -  Raw_Manufacturing_enterprise_cleaned.xlsx
  -  Raw_Manufacturing_turnover_cleaned.xlsx
  -  Raw_Manufacturing_productionvalue_cleaned.xlsx
  -  Manufacturing_Master-Manufacturing_Master.xlsx
  -  Manufacturing_final.xlsx
  -  Raw_services_enterprise.xlsx
  -  Raw_services_turnover.xlsx
  -  Raw_services_production_value.xlsx
  -  Services_Master_services_Master.xlsx
  -  Services_final.xlsx
3. sql/ - contains all SQL queries and resulted tables 
 - Manufacturing_sql_results.csv
 - Services_sql_results.csv
 - SQL Scripts (PDF)
4. python/ - contains all python scripts - inclduing analysis 
   - python notebook(colab)
5. notebooks/ - full google colab notebook 
   - python notebook(colab)
6. charts/ - Charts created in python analysis 
    - All charts (PDF)
    - EDA Charts (PDF)
7. reports/ - Project report PDFs appendix 
     - Final_project_report(PDF)
     - Appendix (PDF)
     
## Methodology 
 **1. Data cleaning**
     - Selected 6 countries with complete multi-year data
     - Unpivoted 6 sheets using google sheets('FLATTEN', 'SPLIT', 'ARRAYFORMULA')
     - Removed blanks, null, duplicates 
     - Saved each cleaned sheet as CSV
  **2. SQL Analysis (24 KPI tables)**
  For each of the **6 sheets**, 
  
  four KPI tables were generated:
  
    1. **Average Growth (%)**
    2. **Average Value (enterpirse/turnover/prouction)**
    3. **Volatility Range (MAX_MIN)**
    4. **Overall growth(%)**
       
  Created:
  - **Manufacturing_master.csv**
  - **Services_master.csv**
    
**3. Python Analysis**
Steps:
1. Imported master CSV files
2. Merged into a final combined dataset
3. Added 'sector' column
4. Generated Comparative barplots for:
     - overall growth
     - Avergae value
     - Volatility range
     - Average growth
  Saved all charts in a compiled pdf.

**4. Exploratory Data Analysis (EDA) Perfomed**

    1. Descriptive statistics 
    2. Distribution analysis (histograms)
    3. Boxplots (Outlier detection)
    4. Correlation heatmap
    5. KPI-wise bar charts
    6. Cross-country comparisons 

## Key Findings 

**1. Sector-level Insights**
   ## **Manufacturing** 
       - High Value but **high volatility**
       - Dominated by **Italy, Germany, Netherlands**
       - Strong production capacity - uneven growth 
       - More sensitive to economic cycles 
   ## **Services**
       - More **Stable** across countries 
       - Lower volatility 
       - Fewer extreme outliers 
       - Strong ICT and Trade performance 

**2. Country-level Insights**
 **Top Performers**
 
   1. **Germany** - most stable, high turnover and Production
   2. **Italy** - Highest turnover, high output, volatile
   3. **Netherlands** - Strong mix of services and manufacturing sectros 

 **Mid Performers**
   1. **Sweden** - stable growth
   2. **Spain** - Moderate growth, lower volatility

 **Weak performers**
 - Countries with negative long-term growth in both sectors

**3. Cross-sector comparison**
 - Manufacturing - **High value and High volatility**
 - Services - **lower volatility and broader distribution**
 - Counties strong in manufacturing typically strong in services

## Recommendations 
 1. **Prioritize stable economies**:
    Germany and Sweden for long-term investment.
2. **Monitor high-value but volatile markets**:
   Italy and Netherlands.
3. **Strengthen weak performers**:
   Improve digital infrastructure and enterprise innovation.
4. **Enhance manufacturing with service-integration**:
   ICT-driven manufacturing improves resilience.

## Future Scope 
 - Forcasting using ARIMA/Prophet
 - Clustering countries based on stability and growth
 - machine learning models for growth prediction
 - PowerBI or Tableau dashboard
 - Deep-diving into sub-industries


## Project files included 
 - Manufacturing_final.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/manufacturing_final.xlsx)
 - Services_final.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/services_final.xlsx)
 - complete_project_output.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/complete_project_output.xlsx)
 - Manufacturing_Master-Manufacturing_Master.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Manufacturing_Master-Manufacturing_Master.xlsx)
 - Services_Master_Services_Master.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Services_Master_Services_Master.xlsx)
 - Raw_Manufacturing_enterprise_cleaned.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Raw_Manufacture_enterprise_cleaned.xlsx)
 - Raw_Manufacturing_turnover_cleaned.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Raw_Manufacturing_turnover_cleaned.xlsx)
 - Raw_Manufacturing_productionvalue_cleaned.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Raw_Manufacturing_productionvalue_cleaned.xlsx )
 - Raw_services_enterprise.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Raw_Services_Enterprise.xlsx)
 - Raw_services_turnover.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Raw_Services_Turnover.xlsx)
 - Raw_services_production_value.xlsx (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/data/Raw_Services_Production_value.xlsx)
 - Manufacturing_SQL_Results.csv (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Sql/Manufacturing_services_SQLResults.csv)
 - Serices_SQL_Results.csv (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Sql/Manufacturing_services_SQLResults.csv)
 - SQL Scripts (https://github.com/pavithrajonna-93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Sql/SQLScript-Manufacturing-Servicesproject.pdf)
 - Python notebook(Colab) (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Python/Copy_of_project_eurostat_.ipynb)
 - All charts (PDF) (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Charts/All_Charts.pdf)
 - EDA Charts (PDF) (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Charts/EDA_CHARTS_ALL.pdf)
 - Full project report with methodology and insights(PDF) (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Reports/EUStat_Manufacturing_Services_Analysis_Project_Report.pdf)
 - Appendix_Visualisation (PDF) (https://github.com/pavithrajonna93/Eurostat_Manufacturing_vs_Services_Analysis/blob/main/Reports/Eustat_Manufacturing_Services_Analysis_Porject_Appendix.pdf)

## Author
**Pavithra jonna**
HR Data managemet Specialist 


 






























