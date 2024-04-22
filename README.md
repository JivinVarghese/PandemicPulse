<!-- # NetSocket -->

<!-- ![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Sockets](https://img.shields.io/badge/Sockets-007396?style=for-the-badge&logo=socket.io&logoColor=white)
![Graphana](https://img.shields.io/badge/Graphana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Influx DB](https://img.shields.io/badge/Influx%20DB-22ADF6?style=for-the-badge&logo=influxdb&logoColor=white)
![Redpanda](https://img.shields.io/badge/Redpanda-000000?style=for-the-badge&logo=apachekafka&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) -->

# PandemicPulse

![Snowflake](https://img.shields.io/badge/Snowflake-3793D2?style=for-the-badge&logo=snowflake&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white)
![PowerBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=white)

## Overview

#### Pandemic Pulse: Data-driven Healthcare Optimization

Project Description: CSSE Covid19 Daily Reports - Healthcare Case Study

Project Overview:
In response to the global Covid-19 pandemic, healthcare management has emerged as a critical area of focus. Leveraging data science methodologies, this project aims to extract meaningful insights from the vast repository of Covid-19 data provided by the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University. Specifically, the project targets patient length of stay as a crucial parameter for enhancing healthcare efficiency within hospital settings.

Problem Statement:
The Covid-19 pandemic has underscored the importance of effective healthcare management. Understanding and predicting patient length of stay is essential for optimizing healthcare operations. This project seeks to address this challenge by employing data science techniques to analyze and interpret the extensive Covid-19 dataset provided by CSSE.

Dataset:
The dataset comprises historical and current Covid-19 data, spanning from January 2nd, 2021 to June 1st, 2021. It includes various attributes such as FIPS codes, county names, confirmed cases, deaths, recoveries, and more. The dataset is sourced from the CSSE GitHub repository and is available in CSV format.

Project Development Steps:

Database and Schema Creation: Establishes the 'Covid_db' database and 'covid_schema' schema to organize the project data effectively.

File Format Creation: Defines a file format for the CSV data to facilitate seamless data loading and processing.

Historical Data Processing:
Creates the 'COVID_HISTORY' table for storing historical data.
Loads historical data into the table and performs clustering to enhance query performance.

Current Data Loading:
Sets up an external stage to store current data from an AWS S3 bucket.
Integrates storage and creates the 'COVID_CURRENT' table for current data.
Establishes a snowpipe for continuous data loading from the external stage to the staging table.

Change Data Capture (CDC) and Slowly Changing Dimension (SCD) Implementation:
Creates a stream ('covid_stream') to capture data changes in the 'COVID_CURRENT' table.
Implements a task to append streamed data to the 'COVID_HISTORY' table, enabling historical tracking.

Data Sharing:
Sets up reader accounts to facilitate data sharing with non-Snowflake users, ensuring accessibility and collaboration.
Time Travel and Zero Copy Cloning:
Utilizes zero-copy cloning to create a clone of the table for historical data analysis.
Implements Snowflake Time Travel to access historical data snapshots for analysis and backup purposes.

Stored Procedure Creation: Develops a stored procedure in JavaScript to insert data into tables, ensuring data integrity and consistency.

Data Visualization:
Creates tables for easy data visualization, including populations, initial confirmed cases, final Covid status, etc.
Utilizes PowerBI for generating insightful visualizations and dashboards to address key business queries.
Business Queries and Visualizations:

## Screenshots

<img src="./screenshots/1.png" width="60%" /> <br>

<img src="./screenshots/2.png" width="60%" /> <br>

1.Daily number of confirmed cases in May for India.

<img src="./screenshots/3.png" width="60%" /> <br>

2.Countries with the highest number of confirmed cases per capita.

<img src="./screenshots/4.png" width="60%" /> <br>

3.Regions experiencing the most rapid increase in confirmed cases.

<img src="./screenshots/5.png" width="60%" /> <br>

4.Trend analysis of confirmed, active, and recovered cases by month.

<img src="./screenshots/6.png" width="60%" /> <br>

## Contributions <a id="contributions"></a>

![Alt](https://repobeats.axiom.co/api/embed/8f067b3de758710566b9d73f68f1778424ce633d.svg "Repobeats analytics image")

## Contributors <a id="contributors"></a>

-  [Jivin Varghese Porthukaran](https://jivin.co.in/)<br>
   [![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/JivinVarghese/)
   [![Github](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JivinVarghese)
