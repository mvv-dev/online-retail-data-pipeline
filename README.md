# Online Retail Data Pipeline

A portfolio project that transforms raw retail transactions into a relational database for sales analysis. The project covers data modeling, data quality checks, ETL with Python, and analytical queries in SQL.

## Dataset

This project uses the [Online Retail dataset](https://archive.ics.uci.edu/dataset/352/online+retail) from the UCI Machine Learning Repository. Each source row represents a product recorded on an invoice.

## Data model

The relational model separates the source data into four tables:

- **Customer:** customer ID and country.
- **Invoice:** invoice number, date, and customer reference.
- **Product:** stock code and description.
- **Invoice_Item:** products and quantities recorded on each invoice, including the unit price at the time of the transaction.

`Invoice_Item` uses `(invoice_no, stock_code)` as a composite primary key. Under this model, a product appears at most once on an invoice. The ETL will check whether the source data satisfies this rule and report exceptions.

<img width="781" height="440" alt="image" src="https://github.com/user-attachments/assets/42998a40-1408-4b0e-966e-30d860aeb30e" />


## Project workflow

1. Explore the source data and define data quality rules.
2. Create the relational schema in PostgreSQL.
3. Build a Python ETL pipeline to clean and load the data.
4. Validate the loaded tables against the source.
5. Write SQL queries to answer sales and customer questions.

## Questions to explore

- How does sales revenue change over time?
- Which products generate the most revenue?
- Which customers make repeat purchases?
- How do sales vary by country?
- How do cancellations affect reported sales?

## Status

- [x] Initial entity relationship diagram
- [ ] Source data profiling and modeling validation
- [ ] PostgreSQL schema
- [ ] Python ETL pipeline
- [ ] Data validation
- [ ] Analytical SQL queries and findings

## Tools

Python, PostgreSQL, SQL, and MySQL Workbench for the ER diagram.
