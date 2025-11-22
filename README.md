# Multi-country Manufacturing vs Services Analysis (EU, 2013-2020)

## Introduction

This project presents a comparative analysis of the **Manufacturing** and **Services** Sectors across six major Eurpoean economies using official data from Eurostat (2005-2020).

The goal is to understand how these two sectors differ in:
- Growth performance
- Stability and Volatility
- Revenue/Production scale
- Long-term trends and patterns

Using SQL, Python and Exploratory Data Analysis(EDA), this project uncovers structural differences between the two sectors and identifies the top-performing, stable and high-risk economies.
The analysis highlights how enterprise base, production value and turnover shape the economic landscape of Europe.

## Data Sources 
**Eurostat Strctural Business Statistics**
1. **Manufacturing Sector (NACE Rev. 2 B-E)**
   *Annual detailed enterprise statistics for industry(2005-2020)*
2. **Services Sector (NACE Rev. 2 G-N, S95)**
   *Annual detailed enterprise statistics for Services (2005-2020)*

Both datasets include:
1. Enterprise count
2. Turnover
3. Production value
4. Year-wise breakdown
  
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

**Why this project?**
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

**This project demonstrated:**
1. **Extracted and cleaned raw Eurostat data**
2. **Unpivoted** 6 sheets (3 manufacturing and 3 services)
3. **Ran SQL** to compute KPIs for each sector
4. **Merged all datasets in Python**
5. **Performed EDA** (Histogram, boxplots, Heatmap, Summary statistics)
6. **Created Sector-wise visual comparisons**
7. **Generated insights** for both industries
The result is a consolidated understanding of **Europe's manufacturing vs. service performance** from 2013 - 2020
  
## Tools and Technologies Used 
1. Google sheets(unpivot with ARRAYFORMULA, FLATTEN, SPLIT)
2.  Excel
   
**SQL Analysis**
1. SQlite (DB Browser/Online SQLite editor)
2. SQL DDL + DML for:
   - Average growth (%)
   - Average value
   - Volatility range
   - Overall Growth (%)

**Python Analysis**
-  Google colab
-  Pandas
-  Numpy
-  Matplotlib
-  Seaborn
  
**Version control**
Git & Github

## Folder Structure 
This Repository follows a clean and professional structure for clarity, reproducibility and evaluation by universities/Recruiters.

**Project Layout**

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

## Final dataset Overview
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
   
**Why these countries?**

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

## How to run this project
Follow the steps below to reproduce the SQL analysis, Python analysis and visualisations

*1. Clone the repository*

git clone https://github.com/<pavithrajonna-93>/<Eurostat_Manufacturing_vs_Services_Analysis>.git
cd<Eurostat_Manufacturing_vs_Services_Analysis>

*2.Install required pythin libraries*
- pip install pandas numpy matplotlib seaborn
- If you are working in Google colab, these libraries are already installed.

*3. Open the notebook*
- Option A - Google colab 
   1. Go to notebook/folder
   2. Open the file: EU_Manufacturing_services_Analysis.ipynb
   3. Click open in colab
   4. Run all the cells
- Option B - Jupyter Notebook
   Open the notebook file from notebooks/.

*4. Run the SQL Analysis*
- Use DB Browser for SQLite, or an online SQLite editor
   1. Open a new database
   2. Go to execute SQL
   3. Copy queries from:
       - sql/SQL Scripts
   4. Run them to recreate all KPIs
   5. Export the results to CSV

*5. Run python EDA and Visualisations*
The notebook will:
   1. load master datasets
   2. merge manufacturing and services
   3. perform EDA (Summary stats, histograms, boxplots)
   4. Generate bar charts comparing the sectors
   5. Export visualizations
Results will appear automatically in output cells.

*6. View project outputs*
You can find:
   1. Processed datasets - /data/
   2. Visual charts - /charts/
   3. Full report - /reports/
   4. Notebook outputs - /notebooks/
Everything is reproducible with the code in this repositoty.

## Key Insights & Findings 

The combined SQL and Python analysis reveals clear differences in performance, stability and growth between the Manufacturing and Services sectors across six major European economies.

**1. Sector-level Insights**
   **Manufacturing** 
       - *Highly concentrated sector* - A small group of countries (Italy, Germany, Netherlands) dominate enterprise count, turnover and production value.
       - *High Volatility* - Manufactuing shows significant fluctuations in turnover and production output, indicating sensivity to economic cycles.
       - *Uneven production capacity* - large gaps between high-performing and low-performing countries suggest unequal industrial infrastructure.
       - *Growth patterns mixed* - several countries show negative or inconsistent growth values across years.

**Top manufacturing performers**

1. *Italy* - Highest turnover and production value
2. *Germany* - Most stable, consistent performer
3. *Netherlands* - Strong enterprise base and turnover
   
    **Services**
       - More stable than manufacting - lower volatility across all KPIs.
       - Balanced distribution - fewer outliers and more uniform performance among countries
       - Better long-term predictability - services sector shows steady patterns across most metrics
       - ICT - driven economies - countries strong in manufacturing also tend to perform well in services
   
**Top Services performers**

1. Germany
2. Netherlands
3. Sweden 

**3. Cross-sector comparison**
 - Manufacturing - **High value and High volatility**
 - Services - **moderate value, High stability**

Key observations:
1. Countries with strong manufacturing foundations also show strong services performance
2. Manufacturing leads in output but struggle with stability
3. Services outperform manufacturing in growth steadiness
4. Enterprise count does not directly drive turnover or growth

**4. Growth Insights**
1. **Germany and Sweden** show consistent positive long-term growth
2. **Italy and the Netherlands** have strong revenue but unstable growth patterns
3. Many countries show negative growth values in manufacturing, indicating structural challenges

**5. Volatility Insights**
1. **Italy and the Netherlands** show high volatility - indicating unpredictable revenue cycles.
2. **Germany and Sweden** show low volatility - making them economically resilient
3. Volatility is strongly correlated with turnover - high-value markets are also high-risk.

**6. Correlation Insights**
1. **Turnover - Production value** - Strong positive correlation
2. **Growth - Enterprise count** - Weak correlation
3. **Volatility - Turnover** - Moderate correlation

This indicates:
- High production - high Turnover
- More Enterprises is not mean higher growth
- Large market experience higher fluctuations

**Summary**
- Manufacturing sector is powerful but unstable
- Services sector is stable and evenly distributed
- Germany is the most consistent economy across all KPIs
- Italy and Netherlands generate the highest value but at high risk
- Sweden shows balanced, sustainable growth
- Structural disparities exist between countries

These insights help understand economic stability, risk and performance across Europe.

**Recommendations**
 1. **Prioritize stable economies**:
    Germany and Sweden for long-term investment.
2. **Monitor high-value but volatile markets**:
   Italy and Netherlands.
3. **Strengthen weak performers**:
   Improve digital infrastructure and enterprise innovation.
4. **Enhance manufacturing with service-integration**:
   ICT-driven manufacturing improves resilience.

**Future Scope**
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

## Badges and Project Highlights 
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![SQL](https://img.shields.io/badge/SQL-SQLite-lightgrey)
![EDA](https://img.shields.io/badge/EDA-Exploratory_Data_Analysis-orange)
![Eurostat](https://img.shields.io/badge/Data-Eurostat-blueviolet)
![Visualization](https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-yellow)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-red)
![License](https://img.shields.io/badge/License-MIT-success)

## Project highlights 

- End-to-end data analysis (raw-cleaned- SQL KPIs - Python EDA - Insights)
- Compared two major economic sectors across 6 European countries
- Created 24 KPI tables in SQL (6 sheets x 4 KPIs)
- Built unified master datasets for manufacturing and services
- Delivered Full EDA including histograms, boxplots, heatmaps
- Produced polished charts for growth, volatility and sector performance
- Structured the project using industry-standard folder hierarchy
- Delivered a professional report and appendix in '/reports/' folder
- Ready for academic admissions, job interviews and portfolio showcases

## Key Features of this  Repository 

1. Clean project structure
2. Reproducible SQL analysis
3. Well-documented Python notebook
4. High-quality visualizations
5. Strong insight generation
6. Complete project report included
7. Public and shareable Github repository



## Author
**Pavithra jonna**
HR Data managemet Specialist 

This project was created as part of an applied analytics and data-driven decision-making portfolio, demonstarting skills in:
- SQL Data analysis
- Python Programming
- EDA and Visualization
- Report writing
- Github documentation
- Business Insights and Interpretation

For queries or collaboration:
*pavithra.jonna@gmail.com*

## Acknowledgements 
- Eurostat structural Business Statistics (SBS) Dataset
- Google colab
- Pandas, Numpy, Matplotlib, Seaborn
- DB Browser for SQLite
  

 






























