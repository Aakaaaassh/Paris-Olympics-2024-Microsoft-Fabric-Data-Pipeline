# Olympics 2024 Data Engineering and Analytics Pipeline

![Architecture Diagram](https://github.com/Aakaaaassh/Paris-Olympics-2024-Microsoft-Fabric-Data-Pipeline/blob/main/Olympics%202024%20Data%20Pipeline%20Architecture.png) 

This project builds a complete real-time data pipeline for the **Paris 2024 Olympics**, processing raw data from CSV files and transforming it into meaningful insights using **Microsoft Fabric**, **Apache Spark**, and **Power BI**. The pipeline follows the **Medallion Architecture** (Bronze, Silver, Gold) and incorporates advanced data modeling with **star and snowflake schemas**. The final product is an interactive dashboard with dynamic charts and tooltips providing deep insights into athletes, medals, teams, and more.

## Table of Contents
- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Data Workflow](#data-workflow)
- [Architecture](#architecture)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Dashboard](#dashboard)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project ingests **13 flat CSV files** containing Olympic data (athletes, medals, events, etc.), transforms the data using **Apache Spark**, and saves it as **Delta tables**. We model the data into **Fact** and **Dimension** tables using **star and snowflake schemas** for efficient querying. The data is visualized through **Power BI**, leveraging **DAX** to create calculated columns, measures, and interactive charts with **tooltips** for deep insights.

The pipeline supports real-time analytics with **DirectQuery**, fetching live data to visualize various aspects of the Olympics, such as athletes’ performance, medal counts, team standings, and more.

## Tech Stack

- **Microsoft Fabric**: Data Lakehouse, Synapse Data Engineering, and Power BI integration.
- **Apache Spark**: Data processing, transformation, and handling complex data types.
- **Delta Lake (Parquet format)**: Storing and querying optimized data tables.
- **Medallion Architecture**: Bronze, Silver, Gold layers for data organization.
- **Power BI**: Interactive dashboards, DAX for calculated columns and measures, tooltips, and real-time visualizations.
- **DAX (Data Analysis Expressions)**: Used for calculated columns and measures in Power BI.
- **Star and Snowflake Schema**: Data modeling for Fact and Dimension tables.

## Features

- **Real-Time Data Pipeline**: Ingests 13 CSV files and processes them using Apache Spark.
- **Medallion Architecture**: Bronze (raw), Silver (cleaned), and Gold (analytics-ready) data layers.
- **Star and Snowflake Schemas**: Fact and Dimension tables for efficient querying.
- **Delta Lake (Parquet)**: Storing data in optimized format for fast queries.
- **Power BI Dashboards**: Includes 50+ interactive charts with dynamic tooltips and rotating map charts.
- **Calculated Columns and Measures**: 20+ calculated fields using DAX in Power BI.
- **Tooltips**: Custom tooltips providing deep insights when interacting with charts.
  
## Data Workflow

1. **Data Ingestion (Bronze Layer)**: Raw data (13 CSV files) ingested into **OneLake** using Microsoft Fabric.
2. **Data Transformation (Silver Layer)**: Data cleaned, transformed, and unpivoted using **Apache Spark**; complex data types handled (e.g., arrays, special characters).
3. **Data Modeling (Gold Layer)**: Data structured using **star and snowflake schemas** into Fact and Dimension tables. Delta Lake format (Parquet) used for efficient querying.
4. **Power BI Integration**: Visualize data using **DirectQuery** in Power BI, creating interactive dashboards with DAX-based measures and calculated columns.

## Architecture

The architecture follows the **Medallion Architecture** (Bronze, Silver, Gold layers):

- **Bronze Layer**: Raw data ingested from CSVs and stored in **OneLake**.
- **Silver Layer**: Data transformation using Apache Spark, creating **Delta tables** (Fact/Dimension).
- **Gold Layer**: Data modeled with **star and snowflake schemas**, optimized for analysis.
- **Power BI**: Interactive dashboards built on real-time data using **DirectQuery**.



## Setup and Installation

### Prerequisites

- **Microsoft Fabric account** (with access to **Lakehouse**, **Synapse**, and **Power BI**)
- **Power BI Desktop** (for creating and publishing dashboards)
- **Apache Spark** (in Microsoft Fabric for data processing)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/olympics2024-data-pipeline.git
   cd olympics2024-data-pipeline
   ```

2. Upload the **raw CSV files** to **OneLake** within your Microsoft Fabric workspace.
   
3. Open the **Synapse Notebook** in Microsoft Fabric:
   - Load and clean the raw data with **Apache Spark**.
   - Unpivot and transform the data to create Fact and Dimension tables.
   
4. Save processed data in **Delta format (Parquet)** in your **Lakehouse**.

5. In **Power BI Desktop**:
   - Connect to your **Lakehouse** using **DirectQuery**.
   - Build interactive charts, applying **DAX** for calculated columns and measures.
   - Publish your report to **Power BI Service**.

## Usage

1. **Run the Apache Spark Notebook** to transform and clean the raw data.
2. **Connect Power BI** to the processed data in **OneLake** using **DirectQuery**.
3. Use the **Power BI Dashboard** to explore insights on athletes, teams, medals, events, and demographics.
   
## Dashboard

![Dashboard](https://github.com/user-attachments/assets/081504f4-7476-4983-bcd6-f87533f190bb)

The Power BI dashboard includes:
- **Interactive map charts** showing country performance with tooltips displaying report pages.
- **Medals insights** by sport, event, athlete, and team.
- **Athlete demographics** such as age, nationality, and team.
- **Team and event performance** breakdowns.







https://github.com/user-attachments/assets/8d937b10-3468-4115-b5aa-e48e997604d6



## Data Model

![Database ER diagram (crow's foot)](https://github.com/user-attachments/assets/9eed5bb8-17cb-43dc-b38a-8f0d73b76b2c)


## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements or additional features.

### To Contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Key Sections Breakdown:
1. **Project Overview**: Summarizes what the project is about.
2. **Tech Stack**: Lists all the tools and technologies used.
3. **Features**: Highlights key features like data processing, modeling, and Power BI dashboards.
4. **Data Workflow**: Describes how the data flows from raw CSV ingestion to Power BI visualizations.
5. **Architecture**: Optionally, include a diagram that visualizes your pipeline.
6. **Setup and Installation**: Provides instructions for setting up the project.
7. **Usage**: Explains how to run the pipeline and use the dashboard.
8. **Dashboard**: Includes details on the Power BI visualizations, with an image of the dashboard.
9. **Contributing**: Information for others who want to contribute to the project.
10. **License**: License details for the repository.

You can modify the links (e.g., for diagrams or dashboard images) once they are uploaded to your repository. This README will give a comprehensive overview of your project on GitHub! Let me know if you need further adjustments.
