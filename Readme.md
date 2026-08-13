# Airbnb Data Analysis & Performance Dashboard

## Project Overview
This project provides a comprehensive data analysis and business intelligence dashboard for Airbnb property and booking data spanning from 2023 into early 2026. The goal is to analyze booking trends, revenue generation, occupancy rates, and host performance to provide actionable insights for property management and strategic decision-making. 

The analysis is built on a robust data model and features interactive dashboards that track performance across different neighborhoods, property types, and time periods. The final visual report is available in the **end to end project_3.pdf**.

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
Based on the dashboard visualizations spanning 2023-2026, here are the major findings and performance metrics:

### Financial Performance and Seasonality
*   **Revenue Growth**: The platform generated a massive Total Revenue of **$176.08M** over the four-year period. Given that 2026 only contains January data, the platform averages roughly $50 million in revenue annually.
*   **Stable Rates**: The Average Nightly Rate sits at **$235.56**, and the overall Cancellation Rate is **19.95%**.
*   **Occupancy Consistency**: The Occupancy Rate remains remarkably steady throughout the year, averaging **50.47%**.
*   **Rate Fluctuation**: While the nightly rate remains mostly stable between **$232** and **$238**, the Revenue Per Available Room (RevPAR) experiences notable seasonal spikes, peaking around January (**$128**) and later in the year.

### Market Demand and Preferences
*   **Top Neighbourhoods**: The Bronx leads significantly in booking volume with **12.6K** bookings. It is followed by Crown Heights at **7.6K** bookings, and Harlem, Chelsea, and the East Village each at **7.5K** bookings.
*   **Accommodation Types**: Guests strongly prefer booking an "Entire home/apt," which accounts for **56.16%** (**56K**) of all bookings. Private rooms make up a strong secondary market at **31.22%** (**31K**). Hotel rooms make up **6.39%** (**6K**) of the bookings.
*   **Property Categories**: Studios (**16.2K**), Hostels (**13.7K**), and Lofts (**12.6K**) are the most frequently booked property types.

### The Superhost Advantage
*   **Revenue Dominance**: Superhosts are the primary financial driver for the platform. They account for **71.07%** (**71K**) of all bookings and command a massive **69.3%** (**$122.02M**) share of total revenue. By comparison, regular hosts brought in **$54.06M** (**30.7%**) from **29K** bookings.
*   **Quality Consistency**: Individual top-performing hosts manage high booking volumes while maintaining highly consistent Average Review Scores between **3.91** and **3.94**, proving that scale does not degrade the guest experience.

## Tech Stack
*   **Tool**: Power BI 
*   **Data Modeling**: Star Schema 
*   **Calculations**: DAX (Data Analysis Expressions) 

## How to Use
1.  Download the raw CSV datasets provided in the repository.
2.  Import the files into your preferred relational database or directly into Power BI/Tableau.
3.  Refer to the included **end to end project_3.pdf** document to view the final dashboard layouts and visualization structure.
