**Project Summary**

This project performs a SQL-based analysis of high-growth “unicorn” companies to understand which industries created the most new unicorns between 2019 and 2021, and how their valuations compare.

The objectives were to:

- Identify the three best-performing industries based on the number of new unicorns created in 2019, 2020, and 2021 combined

- For those industries, calculate the number of unicorns per year and their average valuation in billions of dollars, rounded to two decimal places

- These insights help an investment firm see which industries are producing the most high-value companies and where future opportunities may lie.

**What This Project Achieved**

- Joined the industries, dates, and funding tables to combine industry, unicorn year, and company valuation

- Filtered companies that became unicorns in 2019, 2020, or 2021

- Identified the top three industries by count of new unicorns across those years

- Counted the number of unicorns per industry–year combination

- Calculated the average valuation per industry–year, converted it to billions of USD, and rounded to two decimal places

- Generated a final summary table with industry, year, num_unicorns, average_valuation_billions ordered by year and number of unicorns in descending order

**Files Included**

- notebook.ipynb → SQL notebook containing the analysis

- README.md → Project documentation

- SQL Queries → Raw SQL Queries used for generating the outputs

- unicorn_industry_trends.csv → Export of the final SQL result

**Dataset Structure (SQL Tables)**

The analysis uses four related SQL tables from the unicorns database:

dates → company_id, date_joined, year_founded

funding → company_id, valuation, funding, select_investors

industries → company_id, industry

companies → company_id, company, city, country, continent

**SQL Query Used in the Analysis**

- A single SQL query (using CTEs) was used to obtain the required output; it is included inside the project notebook and saved into a pandas DataFrame called df.

- top_industries → finds the three industries with the most new unicorns created between 2019 and 2021

- yearly_rankings → computes the number of unicorns and average valuation per industry and year

- Final SELECT → filters to the three top industries and the years 2019–2021, converts valuations to billions, and returns the final summary table

**Results Overview**

The final table (and exported CSV) contains:

industry, year, num_unicorns, average_valuation_billions

Each row represents one industry in one year among the top three industries, with:

the number of new unicorns created in that year, and

their average valuation, expressed in billions of USD.
