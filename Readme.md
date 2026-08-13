# Airbnb Data Analysis & Performance Dashboard

## Project Overview
This project provides a comprehensive data analysis and business intelligence dashboard for Airbnb property and booking data. The goal of this project is to analyze booking trends, revenue generation, occupancy rates, and host performance to provide actionable insights for property management and strategic decision-making. 

The analysis is built on a robust data model and features interactive dashboards that track performance across different neighborhoods, property types, and time periods.

## Data Architecture
The data model follows a standard Star Schema design, optimizing query performance and simplifying DAX measure creation. The dataset consists of one central fact table and four dimension tables:

*   **fact_bookings.csv**: The core transactional table containing booking details, calculated revenue, cancellation policies, and foreign keys linking to the dimension tables.
*   **dim_date.csv**: A date dimension table used for time intelligence and trend analysis.
*   **dim_host.csv**: Contains host-specific information, including superhost status and response rates.
*   **dim_location.csv**: Provides geographical context, including neighborhoods, cities, and zip codes.
*   **dim_property.csv**: Details property characteristics such as accommodation capacity, bedrooms, and base price.

## Key Measures and KPIs
To perform in-depth analysis, several DAX measures were created and organized into logical folders:

*   **Core KPIs**: Total Revenue, Total Bookings, Average Nightly Rate, Average Revenue per Booking, and Revenue Per Available Room (RevPAR).
*   **Occupancy & Availability**: Occupancy Rate, Cancellation Rate, and Average nights per booking.
*   **Host Performance**: Superhost Revenue, Superhost Revenue %, Superhost Avg Review, and Total Active Hosts.
*   **Time Intelligence**: Year-over-Year (YoY) Revenue Growth, Month-over-Month (MoM) Revenue Growth, Previous Year (PY) Revenue, and Year-to-Date (YTD) Revenue.
*   **Review & Quality**: Average Review Score, Total Reviews, and High Rating %.

## Dashboard Highlights
The final reporting layer, as showcased in the **end to end project.pdf**, is divided into key executive views:

1.  **Executive Overview**: 
    *   Tracks high-level metrics such as Total Revenue ($56.50M) and an overall Occupancy Rate of ~50.48%.
    *   Visualizes revenue and nightly rate trends by month.
    *   Highlights top-performing neighborhoods (e.g., the Bronx leading with the highest booking volume).
    *   Breaks down popularity by room type, showing that "Entire home/apt" makes up the majority of bookings (55.97%).
2.  **Host and Property Analysis**: 
    *   Compares the performance of Superhosts versus Regular hosts, revealing that Superhosts drive a significant majority of the total revenue (69.3%).
    *   Provides a breakdown of bookings and revenue across different property types (Studios, Lofts, Townhouses, etc.).
    *   Details individual host performance to identify top revenue generators and their average review scores.

## Tech Stack
*   **Tool**: Power BI 
*   **Data Modeling**: Star Schema 
*   **Calculations**: DAX (Data Analysis Expressions) for complex time-intelligence and KPI formulation.

## How to Use
1.  Download the `.pbix` file (if applicable) or view the raw datasets provided in the repository.
2.  The raw CSV files can be imported into any relational database or directly into Power BI/Tableau.
3.  Refer to the included PDF document to see the final dashboard layouts and visualization structure.
