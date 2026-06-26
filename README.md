
# NYC Utility Service Request Operations Dashboard

  <img width="786" height="442" alt="BI dashboard screenshot" src="https://github.com/user-attachments/assets/91e0ed18-a564-4b49-bfe5-f9bfa7a1ed91" />

## Quick Summary

Built an Excel and Power BI dashboard using NYC 311 utility-related service request data to analyze request volume, open backlog, closure rate, borough-level workload, and average resolution days.

Key findings:
- Water had the highest request volume at approximately 16,000 requests.
- Street Lighting had the longest average resolution time at 19.6 days.
- Queens and Brooklyn had the highest borough-level request volume.
- The overall closure rate was 95.9%.

## Project Overview

I built this project to practice turning raw operational data into a dashboard that could be useful for a service or operations team.

The project uses NYC 311 utility-related service request data to track request volume, open backlog, closure rate, borough-level workload, and average resolution time by category.

The main goal was to create a clean reporting workflow using Excel, Power Query, Pivot Tables, and Power BI.


## Business Objective

The main business question for this project was:

**How can an operations team monitor service request volume, resolution performance, and backlog trends across utility-related complaint categories?**

This dashboard focuses on utility-related request categories, including:

* Street Lighting
* Traffic Signals
* Sewer
* Water System

## Dataset

The dataset comes from NYC 311 public service request data.

This project uses a **50,000-row sample** of utility-related service requests from **September 2025 through December 2025**.

Because this is a sample, the dashboard should not be interpreted as a full-year analysis of all NYC 311 service requests. Instead, it is intended to demonstrate an operations reporting workflow using real public data.

## Tools Used

* Excel
* Power Query
* Pivot Tables
* Power BI Desktop
* GitHub

## Data Cleaning Process

The raw CSV data was cleaned in Excel using Power Query. The cleaning process included:

* Importing the raw CSV into Power Query
* Setting proper data types for dates, IDs, categories, and numeric fields
* Creating a `Resolution Days` field
* Creating a `request_month` field
* Creating an `is_closed` flag
* Creating backlog aging logic
* Grouping complaint types into utility categories
* Exporting a cleaned CSV for dashboard use

The cleaned dataset was then used to create pivot summaries in Excel and an interactive dashboard in Power BI.

## Dashboard Features

The Power BI dashboard includes:

* Total service requests
* Open requests
* Closure rate
* Average resolution days
* Request volume by borough
* Request volume by utility category
* Average resolution days by category
* Backlog aging
* Interactive slicers for borough and utility category

## Key Insights

Street Lighting had the longest average resolution time at **19.6 days**, making it the slowest category to resolve in this sample.

Water had the highest request volume, with approximately **16,000 requests**.

Queens and Brooklyn carried the largest borough-level workload, with each borough accounting for over **14,000 requests**.

The overall closure rate was **95.9%**, showing that most requests in the sample were closed.

The remaining open requests were aged **61+ days**, suggesting a long-tail backlog that could require operational follow-up.

## Limitations

This project uses a 50,000-row sample from September 2025 through December 2025, not the complete full-year NYC 311 dataset.

Backlog aging was calculated based on the date the data was processed, so open request aging may change depending on when the dataset is refreshed.

The dashboard is intended for portfolio and learning purposes and should not be used as an official NYC operations report.

## Repository Structure

```text
nyc-utility-service-dashboard/
│
├── data/
│   ├── raw/
│   └── cleaned/
│
├── docs/
│
├── excel/
│   └── nyc_utility_service_analysis.xlsx
│
├── images/
│   └── dashboard_screenshot.png
│
├── powerbi/
│   └── nyc_utility_service_dashboard.pbix
│
└── README.md
```

## How to View the Project

Open the Power BI file located in the `powerbi/` folder to explore the dashboard interactively.

A static dashboard screenshot is also available in the `images/` folder for quick review.


## Project Takeaway

This project helped me practice the full reporting workflow: importing raw data, cleaning it in Power Query, creating calculated fields, summarizing the data in Excel, and building a Power BI dashboard around operational KPIs.

The final dashboard gives a quick view of request volume, backlog aging, closure rate, and resolution delays by borough and utility category.

