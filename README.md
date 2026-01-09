Czechoslovakia Banking Data Analysis (1993–1998)
Overview
This project analyzes banking data from Czechoslovakia spanning 1993 to 1998, covering customer demographics, account types, credit card ownership, loans, and transaction patterns. The goal is to provide business insights, KPI analysis, and interactive dashboards to support data-driven decisions.

Dataset
Source: GitHub (Czechoslovakia Bank Dataset)

Description:
Raw data contains tables for Accounts, Clients, Cards, Loans, Orders, Dispositions, and Districts.
Data includes information about customer IDs, account types, credit cards, loan amounts and durations, transaction details, and regional demographics.
Dataset is used for data cleaning, modeling, and visualization.

Data Cleaning & Transformation

Performed in Power Query:

Account Table

Standardized column names (e.g., Account_type → account_type)

Converted account type values to uppercase

Extracted year, month, day from date column

Dropped original date column

Card Table

Created year, month, day, and time columns

Converted data types to integer and time

Uppercased type column

Removed redundant columns

Client Table

Created gender column using Czech birth number logic

Extracted year, month, day from birth number

Created age and age group columns

Dropped original birth_number column

Loan Table

Created loan_type column:

A → Good Debt

B, C, D → Bad Debt

Extracted loan_year and loan_month

District Table

Renamed columns for clarity (district_code, district_name, region, population, cities, avg_salary, crime data)

Dropped unnecessary columns

Standardized region names to uppercase

Order Table

Renamed Bank_to → bank_to

Converted values to lowercase

Data Model & Relationships (Power Pivot)

Account Table is the parent table, linked to:

Loan

Order

District

District Table links to:

Client

Disp

Card

All tables connected via primary and foreign keys, enabling integrated analysis.

Dashboard & Insights

Dashboard includes multi-page interactive Excel visualizations covering:

Key KPIs

Total Accounts: 4,500

Unique Customers: 5,363

Credit Cards Issued: 892

Total Loan Amount: 103,261,740

Average Loan Amount: 151,410

Average Salary: 9,032

Customer & Account Insights

Male and female card ownership nearly equal

Adults are the dominant credit card holders

84% accounts are owner-type, 16% are user-type

Classic cards dominate (74%), followed by Junior (16%) and Gold (10%)

Good loans: 30% | Bad loans: 70%

Geographic Insights

Hl. m. Praha: 554 credit card holders (top city)

North & South Moravia: highest account and loan volumes

Bohemia region: lowest credit card penetration

Loan & Transaction Insights

Total Loans: 682

Total Amount Transferred: 21,228,993

Long-duration loans (4–5 years) dominate

Loan growth spiked in 1994 (510%) then declined in 1995

Peak months: May, June, December

Lowest growth: October

Czechoslovakia-Banking-Data-Analysis/
├── Czechoslovakia-Banking-Data-Analysis.xlsx    # Cleaned dataset, Power Pivot model, dashboards
├── Dashboard_Snapshots.pdf                      # Screenshots of interactive dashboards
├── report.docx                                  # Project report with insights
├── Raw CSV files                                # Account, Client, Card, Loan, Disp, District, Order


Key Takeaways

High proportion of bad loans → increased credit risk

Strategy opportunities:

Convert users to owners

Attract more youth customers

Grow Gold card membership

Dashboard supports demographic, geographic, and loan behavior analysis

Usage

Open Excel Dashboard (.xlsx) for interactive visuals

Use slicers to filter customer type, account type, loan type, region, and time period

Insights can guide business strategy and risk management

Author

Sana Shaffique – Data Analyst Portfolio Project

This is a hire-ready project demonstrating data cleaning, modeling, analysis, and dashboarding in Excel.
