# NYC Real Estate SQL Analysis

## Project Overview
SQL analysis of 845,000+ NYC property sales transactions from 2016 to 2025, sourced from the NYC Department of Finance via NYC Open Data. Raw data was loaded into PostgreSQL, cleaned and transformed using SQL, and analyzed to surface insights not visible in aggregate dashboard views.

This project complements an interactive Power BI dashboard built on the same dataset. [View the dashboard here.](https://app.powerbi.com/view?r=eyJrIjoiOTk0YjQ0OWMtMDVjNy00MjhmLWE5MDItOWFjMDM0NTUzYzljIiwidCI6ImE4ZDNlMTJhLWE0ZjktNDdjMy1iN2JkLTBmMThmNTBjNDcxMyIsImMiOjN9)

## Tools
- PostgreSQL
- pgAdmin 4
- Notepad ++

## Data Source
NYC Department of Finance - Rolling Sales Data
Source: NYC Open Data (publicly available) <br>
Raw dataset: 845,607 rows | Cleaned dataset: 568,541 rows

## Data Cleaning
- Removed dollar signs, commas, and whitespace from numeric columns using REPLACE, TRIM, and CAST
- Filtered transactions below $10,000 to exclude sales where a personal or business relationship may have been in place
- Created a cleaned view (nyc_sales_clean) preserving the raw table intact

## Queries & Key Findings

**Query 1: Year Over Year Price Change by Borough** 

Manhattan posted the steepest single-year appreciation at 20.41% from 2016 to 2017. The Bronx recorded the only meaningful price decline at around 4% in 2023, which is consistent with Federal Reserve rate hikes shrinking buyer purchasing power in the most affordable market. 

**Query 2: Neighborhood Transaction Growth 2016-2025** 

Transaction growth was geographically broad across all five boroughs. Brooklyn dominated with 7 of the top 20 neighborhoods including Boerum Hill, Greenpoint, and Park Slope. Bedford Park and Highbridge/Morris Heights in the Bronx signal early-stage gentrification in historically affordable markets. 

**Query 3: Top Neighborhoods by Price Per Square Foot** 
Manhattan accounts for 9 of the top 10 neighborhoods by median price per square foot, with Greenwich Village West leading at $2,372. This number is roughly 4 to 5 times the citywide median of $430. 

**Query 4: Building Type Impact on Price Per Square Foot** 

Single family homes show the widest borough spread with Manhattan leading at $1,870 per square foot versus $339 in the Bronx. Manhattan elevator apartments rank fourth among boroughs at this property type, trailing Brooklyn, Queens, and the Bronx. Note: co-ops were excluded due to missing square footage data in NYC property records.

**Query 5: Top 10 Zip Codes by Median Sale Price** 

Manhattan accounts for 8 of the top 10 zip codes. SoHo/Tribeca's 10013 leads at $3.7M median. Brooklyn makes two appearances with Carroll Gardens/Cobble Hill and Park Slope/Boerum Hill both exceeding $1.5M median. 

**Query 6: Borough Market Summary** 

Brooklyn, the Bronx, Manhattan, and Queens average construction years between 1933 and 1942, reflecting NYC's pre-war development boom. Staten Island's 1968 average reflects its suburban character and aligns with the completion of the Verrazzano Bridge. Manhattan's maximum transaction of $2.4B is nearly three times Brooklyn's $870M, signaling large commercial portfolio activity concentrated in Manhattan. 
