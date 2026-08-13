# Airbnb Data Analysis & Performance Dashboard

## Project Overview
This project provides a comprehensive data analysis and business intelligence dashboard for Airbnb property and booking data. The goal is to analyze booking trends, revenue generation, occupancy rates, and host performance to provide actionable insights for property management and strategic decision-making. 

The analysis is built on a robust data model and features interactive dashboards that track performance across different neighborhoods, property types, and time periods.

## Data Architecture: The Star Schema Model
The foundation of this project is a Star Schema data model, which is optimized for querying large datasets and building efficient Business Intelligence dashboards. The dataset consists of one central fact table and four dimension tables:

*   **fact_bookings.csv**: The core transactional table containing every booking transaction, calculating revenue, and tracking availability. It holds the foreign keys linking to all dimension tables.
*   **dim_date.csv**: Enables time-intelligence calculations by breaking down dates to analyze seasonal trends and weekend versus weekday performance.
*   **dim_host.csv**: Contains demographic and performance attributes of the property owners, including response rates and the critical superhost flag.
*   **dim_location.csv**: Provides geographic granularity, allowing data to be sliced by country, state, city, neighbourhood, and zipcode.
*   **dim_property.csv**: Describes the physical assets being rented, including pricing structures and property features like bedrooms and accommodation capacity.

## Comprehensive DAX Measures and KPIs
To transform the raw tables into actionable insights, a suite of DAX (Data Analysis Expressions) measures was developed:

*   **Core KPIs**: Tracks overall financial health through metrics like Total Revenue, Total Bookings, and Average Nightly Rate. It also includes Revenue Per Available Room (RevPAR) to evaluate room fill rates at optimal pricing.
*   **Occupancy & Availability**: Monitors Occupancy Rate and Cancellation Rate to understand lost revenue opportunities and actual listing utilization.
*   **Time Intelligence**: Compares current performance against historical benchmarks using Year-over-Year (YoY) and Month-over-Month (MoM) revenue growth calculations.
*   **Host Performance & Quality**: Quantifies the value of the platform's top earners by separating Superhost Revenue and Average Review Scores from standard hosts.

## Key Business Insights
Based on the dashboard visualizations (available in **end to end project.pdf**), several strategic insights can be extracted:

### Market Demand and Preferences
*   **Top Neighbourhoods**: The Bronx leads significantly in booking volume with **4.1K** bookings, followed closely by the East Village and Harlem at **2.5K** bookings each. 
*   **Accommodation Types**: Guests strongly prefer booking an "Entire home/apt," which accounts for **55.97%** (**18K**) of all bookings. Private rooms make up a secondary market at **31.54%** (**10K**).
*   **Property Categories**: Studios, Hostels, and Lofts are the most frequently booked property types, suggesting a market driven by travelers looking for specific, cost-effective spaces.

### Financial Performance and Seasonality
*   **Revenue Stability**: The platform shows strong overall performance with a Total Revenue of **$56.50M** and an Average Nightly Rate of **$234.28**.
*   **Occupancy Consistency**: The Occupancy Rate remains remarkably steady throughout the year, averaging **50.48%** month-over-month.
*   **Rate Fluctuation**: While occupancy is stable, the Revenue Per Available Room (RevPAR) and Average Nightly Rate show seasonal peaks (notably in May and August), indicating periods where hosts successfully command higher premiums.

### The Superhost Advantage
*   **Revenue Dominance**: Superhosts are the primary financial driver for the platform. They account for **71.07%** (**71K**) of all bookings and command a massive **69.3%** (**$122.02M**) share of total revenue, compared to regular hosts at **30.7%** (**$54.06M**).
*   **Quality Consistency**: Individual top-performing hosts manage high booking volumes while maintaining highly consistent Average Review Scores between **3.93** and **3.94**, proving that scale does not degrade the guest experience.

## Tech Stack
*   **Tool**: Power BI 
*   **Data Modeling**: Star Schema 
*   **Calculations**: DAX (Data Analysis Expressions) 

## How to Use
1.  Download the raw CSV datasets provided in the repository.
2.  Import the files into your preferred relational database or directly into Power BI/Tableau.
3.  Refer to the included **end to end project.pdf** document to view the final dashboard layouts and visualization structure.
