# Business-Insights-360

## Project Overview

AtliQ Hardware has experienced rapid growth in recent years. To analyze their business with greater accuracy, the company has decided to implement data analytics using Power BI for the first time. This will enable them to make data-driven decisions and maintain a competitive edge in the market. The project will assist stakeholders in making informed decisions across various domains such as finance, sales, marketing, and supply chain, ultimately contributing to the company's growth.
## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)

## PowerBI techniques Learnt

- questions that should be asked before staring the project
- Creating calculated columns
- creating measure using DAX language
- Data modeling
- Using divide function to prevent zero division errors
- creating date table using m language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting the values in visuals using icons or background color
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Data validation techniques
- PowerBi services
- Publishing reports to PowerBi services
- Setting up personal gateway to set up the auto refresh of data
- Collaboration, workspace, access permissions in PowerBi services


## Business related terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer

  ## Company’s back ground

AltiQ Hardware has expanded significantly in recent years, establishing a global presence. It is a company that sells computers and computer accessories through three different channels.

- Retailers
- Direct
- Distributors

Recently, the company has incurred an unforeseen loss by opening a store in America, based on surveys, intuition, and some Excel analysis. Moreover, the company's competitors have a robust analytics team to perform analyses and make data-driven decisions. Consequently, AltiQ Hardware has no choice but to build their own analytics team to glean data-driven insights and make informed decisions to better survive in the industry.

The project kick-off session is designed to gain a clear understanding of the project's objectives and rationale, as well as to address any questions related to the project..

### Questions to ask before starting with dashboard

- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be time dead-line of the project?
- do the stakeholders expecting pre-view before the actual release?
- What are all the hopes stakeholders have out of this project?
- what are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- what are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- what are all the resources/ data needed to build this dashboard?
- is there any inputs from stakeholders in terms of design and views of the dashboard?

Following the project kickoff meetings, the data engineering team has provided the data as requested by the data analytics team. Let's delve into it.

### Dataset **Understanding.**

Understanding the available data is crucial before beginning an analysis. It's important to have a thorough understanding of the data at hand prior to diving into the analysis.

Dimension table : It will have the static data like details of customer and products.

Fact table : It will have the data about the transactions.  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

## Importing data into PowerBi

- In this project, since the database is MySQL, we need to import the datasets from the MySQL database into PowerBI by supplying the database access credentials.

## Data Model

- Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.
- Poor data modeling affects the over all performance of the report.
- In this project, we have followed Snowfall data modeling method.
<img src="https://github.com/usershanks/Business-Insights-360/blob/main/data_model.png" class="center">

### Dashboard designing

Upon receiving the mock-ups as requirements, the team will begin designing the visuals and create metrics as needed.

## Home view

In Home view, all the views button will be available. User will land on specific view page by clicking the button 

- Info
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Products
- Support
  
  <img src="https://github.com/usershanks/Business-Insights-360/blob/main/home_page.png" class="center">

