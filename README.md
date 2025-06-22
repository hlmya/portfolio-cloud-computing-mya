# Cloud Computing Projects
- 2 projects
- image or something ?
# Project 1 - Descriptive Analysis of City-Owned Property Distribution in Vancouver 
## Project Title: Understanding the Geographic Distribution of City-Owned Properties in Vancouver

## Project Description
Descriptive analysis of city-owned properties aimed at identifying patterns in their distribution across geographic areas. This analysis supports better urban planning and resource allocation through data-driven insights.

## Objective
The main goal of this project is to explore how city-owned properties are distributed throughout various geographic zones in Vancouver. The insights gained help city planners, real estate analysts, and municipal decision-makers better allocate resources and understand urban development trends.

## Dataset
- **Name**: City-Owned Properties
- **Publisher**: City of Vancouver Open Data Portal
- **Size**: 617 records, 7 columns
- **Key Fields**:
  - `Building_No`: City-owned building number
  - `SAP_Address`: Property address
  - `Geometry_Local_Area`: Area label (used for geographic grouping)
  - `Type`: Property type (VAHEF)
  - `Land_Coord`: Coordinates
  - `Geometry`: Spatial data
  - `Geometry_Point_2D`: 2D spatial point
- Data Source: [City-Owned Properties Dataset – City of Vancouver](https://opendata.vancouver.ca/explore/dataset/city-owned-properties/information/?refine.type=VAHEF)

![image](https://github.com/user-attachments/assets/6a4a8cb9-e285-4df1-a81e-b9b9bd937076)

## Methodology
- Data pipeline and DAP architecture (draw.io diagrams)
![image](https://github.com/user-attachments/assets/9955b72b-7ce8-49e4-ab95-15092628c744)

### 1. Data Collection & Ingestion
- Data analysis with fishbone diagram
- Used **AWS S3** to store raw dataset (`realestate-raw-mya`)

![image](https://github.com/user-attachments/assets/4775462c-589a-4de1-9547-38b242eea709)
![image](https://github.com/user-attachments/assets/d1ebe88d-86c4-4372-a2af-0703b6dbdd21)

### 2. Data Profiling & Cleaning
- **AWS Glue DataBrew** used for:
  - Profiling dataset
  - Cleaning and renaming fields
- Cleaned data stored in `realestate-cln-mya`

![image](https://github.com/user-attachments/assets/79998792-b153-456c-b8a4-b28522f7b9a2)
![image](https://github.com/user-attachments/assets/a4b3353a-680f-4b73-a9c8-c2e22ae24dbd)

### 3. Data Cataloging
- Structured using **ETL process in AWS Glue**
- Metadata stored in **AWS Data Catalog**
- Output data stored in `realestate-cur-mya`

![image](https://github.com/user-attachments/assets/14d6d497-929b-4a8c-b8ba-c7525b9fbd7b)
![image](https://github.com/user-attachments/assets/cce3c2d9-ad1a-4957-89d0-0ce89b420391)

### 4. Data Summarization
- SQL queries run in **Amazon Athena** to:
  - Count properties by `Geometry_Local_Area`
  - Identify zones with highest and lowest city-owned property counts

![image](https://github.com/user-attachments/assets/724258bd-a38a-4b31-b551-776fe7d7e8e8)
![image](https://github.com/user-attachments/assets/a0f88953-074c-43c3-92ee-f5ce1706ab67)

## Key Insights & Findings
- Uneven distribution of city-owned properties across local areas
- Certain areas show high concentration due to policy, zoning, or infrastructure demands
- Supports visual-based decision-making for city asset planning

## Tools & Technologies
- AWS S3
- AWS Glue (Crawler, DataBrew, ETL)
- Amazon Athena (SQL)
- draw.io (for architecture diagrams)

## Deliverables
- ETL workflow for property dataset in AWS
- Data analysis report with visualizations and query results
- Cleaned and cataloged dataset ready for future analytics

## Conclusion
This cloud-based descriptive analysis project illustrates how serverless tools on AWS can be used to explore urban infrastructure datasets. It enables city officials and data teams to make informed planning decisions based on accurate geographic property distribution.

# Project 2 - Understanding Modules in AWS Academy Cloud Foundations

## AWS Deployment and Service Models
### Case Study #1: Traditional Computing Model vs Cloud Computing Model
- hello

![image](https://github.com/user-attachments/assets/1a945327-ad60-47f5-9eba-dcecca5c4c87)





### Case Study #2: Cloud Deployment Models


### Case Study #3: Cloud Service Models

### Module 1 Knowledge Check



## AWS Cost Analysis 

## AWS Global infrastructure 

## AWS IAM 

## AWS VPC

## AWS Lambda 

## AWS EBS
