# ☁️ Cloud Computing Technologies @ UCW 
![Cloud](https://img.shields.io/badge/Cloud_Computing-AWS-blue?logo=amazon-aws&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon%20Web%20Services-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon EC2](https://img.shields.io/badge/Amazon%20EC2-F58536?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=for-the-badge&logo=amazon-aws&logoColor=white)
![AWS IAM](https://img.shields.io/badge/AWS%20IAM-1F4E1?style=for-the-badge&logo=amazon-aws&logoColor=white)

This portfolio showcases two major projects completed as part of the ***Cloud Computing Technologies*** course at University Canada West (UCW), under the enthusiastic guidance of my instructor **Ph.D. Mahmood Mortazavi**. These projects reflect both theoretical understanding and hands-on practice with real-world cloud tools and data.

- **Project 1: Descriptive Analysis of City-Owned Property Distribution in Vancouver**  
  This project involved analyzing municipal property data to uncover trends and spatial distributions across Vancouver’s neighborhoods. It provided experience in data wrangling, visualization, and critical thinking about urban resource allocation.

- **Project 2: AWS Academy Cloud Foundations – Module Reflections**  
  This project offers a comprehensive summary of modules covered in the AWS Academy Cloud Foundations course. Key topics include AWS core services (EC2, S3, IAM, CloudWatch), cloud models (IaaS, PaaS, SaaS), and deployment strategies. This foundational knowledge is essential for designing secure and scalable cloud solutions.

These projects strengthened my technical understanding of cloud systems while also developing my problem-solving and data analysis skills in a professional context.

## Table of Content

- [Project 1 - Descriptive Analysis of City-Owned Property Distribution in Vancouver](#project-1---descriptive-analysis-of-city-owned-property-distribution-in-vancouver)
  - [Project Description](#project-description)
  - [Dataset Description](#dataset)
  - [Methodology](#methodology)
    - [Data Collection & Ingestion](#1-data-collection--ingestion)
    - [Data Profiling & Cleaning](#2-data-profiling--3-cleaning)
    - [Data Cataloging](#4-data-cataloging)
    - [Data Summarization](#5-data-summarization)
    - [Data Security](#6-data-security)
    - [Data Governance](#7-data-governance)
    - [Data Monitoring](#8-data-monitoring)
  - [Key Insights & Findings](#key-insights--findings)
  - [Tools & Technologies](#tools--technologies)
  - [Deliverables](#deliverables)
  - [Conclusion](#conclusion)

- [Project 2 - Understanding Modules in AWS Academy Cloud Foundations](#project-2---understanding-modules-in-aws-academy-cloud-foundations)
  - [AWS Deployment and Service Models](#aws-deployment-and-service-models)
    - [Case Study #1: Traditional Computing Model vs Cloud Computing Model](#case-study-1-traditional-computing-model-vs-cloud-computing-model)
    - [Case Study #2: Cloud Deployment Models](#case-study-2-cloud-deployment-models)
    - [Case Study #3: Cloud Service Models](#case-study-3-cloud-service-models)
    - [AWS Knowledge Check - Module 1: Cloud Concepts Overview](#aws-knowledge-check---module-1-cloud-concepts-overview)
  - [AWS Cost Analysis](#aws-cost-analysis)
    - [Case Study #4: Total Cost Of Ownership - Delaware North](#case-study-4-total-cost-of-ownership---delaware-north)
    - [Case Study #5: AWS Pricing Calculator](#case-study-5-aws-pricing-calculator)
    - [Case Study #6: Support Plan](#case-study-6-support-plan)
    - [AWS Knowledge Check - Module 2: Economics and Billing](#aws-knowledge-check---module-2-economics-and-billing)
  - [AWS Global infrastructure](#aws-global-infrastructure)
    - [Case Study #7: AWS Global Infrastructure](#case-study-7-aws-global-infrastructure)
    - [AWS Knowledge Check - Module 3: AWS Global Infrastructure Overview](#aws-knowledge-check---module-3-aws-global-infrastructure-overview)
  - [AWS IAM](#aws-iam)
    - [Case Study #8: Who is responsible](#case-study-8-who-is-responsible)
    - [Case Study #9: IAM practice: Lab 1](#case-study-9-iam-practice-lab-1)
    - [AWS Knowledge Check - Module 4: AWS Cloud Security](#aws-knowledge-check---module-4-aws-cloud-security)
  - [AWS VPC](#aws-vpc)
    - [Case Study #10: Build your VPC: Lab 2](#case-study-10-build-your-vpc-lab-2)
    - [AWS Knowledge Check - Module 5: Networking and Content Delivery](#aws-knowledge-check---module-5-networking-and-content-delivery)
  - [AWS Lambda](#aws-lambda)
    - [Case Study #11: Create an AWS Lambda function](#case-study-11-create-an-aws-lambda-function)
    - [AWS Knowledge Check - Module 6: Compute](#aws-knowledge-check---module-6-compute)
  - [AWS EBS](#aws-ebs)
    - [Case Study #12: Working with Amazon EBS: Lab 4](#case-study-12-working-with-amazon-ebs-lab-4)
    - [AWS Knowledge Check - Module 7: Storage](#aws-knowledge-check---module-7-storage)

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

<img width="500" alt="image" src="https://github.com/user-attachments/assets/6a4a8cb9-e285-4df1-a81e-b9b9bd937076" />

## Methodology
- Data pipeline and DAP architecture (draw.io diagrams)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/9955b72b-7ce8-49e4-ab95-15092628c744" />

### 1. Data Collection & Ingestion
- Data analysis with fishbone diagram
- Used **AWS S3** to store raw dataset (`realestate-raw-mya`)

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/4775462c-589a-4de1-9547-38b242eea709" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/d1ebe88d-86c4-4372-a2af-0703b6dbdd21" />
</p>

### 2. Data Profiling & 3. Cleaning
- **AWS Glue DataBrew** used for:
  - Profiling dataset
  - Cleaning and renaming fields
- Cleaned data stored in `realestate-cln-mya`

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/79998792-b153-456c-b8a4-b28522f7b9a2" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/a4b3353a-680f-4b73-a9c8-c2e22ae24dbd" />
</p>

### 4. Data Cataloging
- Structured using **ETL process in AWS Glue**
- Metadata stored in **AWS Data Catalog**
- Output data stored in `realestate-cur-mya`

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/14d6d497-929b-4a8c-b8ba-c7525b9fbd7b" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/cce3c2d9-ad1a-4957-89d0-0ce89b420391" />
</p>

### 5. Data Summarization
- SQL queries run in **Amazon Athena** to:
  - Count properties by `Geometry_Local_Area`
  - Identify zones with highest and lowest city-owned property counts

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/724258bd-a38a-4b31-b551-776fe7d7e8e8" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/a0f88953-074c-43c3-92ee-f5ce1706ab67" />
</p>

### 6. Data Security
To ensure data confidentiality, integrity, and availability:
- **Encryption:** A symmetric key (`realestate-adm-key-mya`) was created using AWS KMS for securing raw, clean, and curated S3 buckets.
- **Configuration:** Bucket versioning and default encryption were enabled in all three buckets.
- **Replication:** A replication rule was added to each S3 bucket to copy data to backup buckets for disaster recovery.

**Tools Used:**  
`AWS S3`, `AWS KMS`, `S3 Replication Rules`

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/8bb66812-9bd7-46b8-8844-2336e5694aaf" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/12ab4c18-a4e4-4e16-bb68-34d5fa01d9de" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/3c4f6e35-bd70-4277-8f2d-5351dae446c7" />
</p>

### 7. Data Governance
Data quality was enforced using a custom ETL pipeline in AWS Glue:
- Rules were defined for **building number** and **geographic area** fields to check completeness and uniqueness.
- Passed and failed records were separated using conditional routing.
- Clean data was saved to the quality check folder in the clean bucket.

**Tools Used:**  
`AWS Glue`, `S3`, `ETL Visual Interface`

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/871d92b8-5166-45a7-8561-84e7d405c9f5" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/fe6b58fb-7c77-4c83-a8d2-822591227d94" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/c95fe5b6-ac39-4b18-ab23-3412e46080b4" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/a32e436c-15d6-4c19-94bc-d878e07fa757" />
</p>

### 8. Data Monitoring
Real-time monitoring and user activity tracking:
- **CloudWatch Dashboard:** Monitors S3 bucket growth, job performance, and triggers alarms for thresholds.
- **CloudTrail Logs:** A dedicated trail (`realestate-adm-tra-mya`) tracks user actions on the platform.

**Tools Used:**  
`AWS CloudWatch`, `AWS CloudTrail`, `S3 Logging`

<p float="left">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/19037f5f-5e2d-4939-aff5-659b2e0297f9" />
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/9f7a28cf-3e29-4ba5-b222-9503262830a5" />
</p>

## Key Insights & Findings
- Uneven distribution of city-owned properties across local areas
- Certain areas show high concentration due to policy, zoning, or infrastructure demands
- Supports visual-based decision-making for city asset planning

## Tools & Technologies
- AWS S3
- AWS Glue (Crawler, DataBrew, ETL)
- Amazon Athena (SQL)
- draw.io (for architecture diagrams)
- AWS CloudWatch, AWS CloudTrail

## Deliverables
- ETL workflow for property dataset in AWS
- Data analysis report with visualizations and query results
- Cleaned and cataloged dataset ready for future analytics

## Conclusion
This cloud-based descriptive analysis project illustrates how serverless tools on AWS can be used to explore urban infrastructure datasets. It enables city officials and data teams to make informed planning decisions based on accurate geographic property distribution.

# Project 2 - Understanding Modules in AWS Academy Cloud Foundations

## AWS Deployment and Service Models
- This module introduces the core concepts of cloud computing, including its service models, deployment models, and comparison with traditional computing environments. It also provides practical insights into AWS services through the following case studies.

### Case Study #1: Traditional Computing Model vs Cloud Computing Model
- The table below compares the Traditional Computing Model and Cloud Computing Model through the management of expense claim datasets in UCW’s Finance Operational Environment.

| Dataset: Expense Claims | Traditional Computing Model | Cloud Computing Model |
| :---: | :---: | :---: |
| Dataset - Location | Path: UCWDataCenter-Vancouver-FOE-GPS-RAM-HDD  <br>Stored in RAM and HDD in a physical server at UCW Data Center, Vancouver. |  Path: AWSDataCenter-UCW-Virginia-FOE-GVS-EBS <br>Stored in RAM and HDD of a virtual server in the AWS Virginia Region.|
| Dataset - Access | Access is **internal and on-site**, it is limited to UCW Finance Operational network users in Vancouver. | Access is **remote and cloud-based** for UCW Finance Operational network users from multiple locations in AWS Virginia Regions.|
| Dataset - Privacy | Privacy is managed internally with internal UCW policies in Vancouver. | Privacy is managed through AWS cloud policies, encryption, and cloud provider compliance such as AWS IAM.|

<img width="640" alt="image" src="https://github.com/user-attachments/assets/26629267-578f-4a9e-90d9-739a0fd3ffe9" />

### Case Study #2: Cloud Deployment Models
- The table below compares the Private Cloud, Public Cloud, Hybrid Cloud, and Multi Cloud Model through the management of expense claim datasets in UCW’s Finance Operational Environment.

| Dataset: Expense Claims | **Private Cloud** | **Public Cloud** | **Hybrid Cloud** | **Multi Cloud** |
|-------------------------|-------------------|------------------|------------------|-----------------|
| **Dataset - Location** | Path: UCWDataCenter-Vancouver-FOE-GVS-RAM-HDD<br>Dataset is stored in RAM and HDD of a Finance Operational Environment virtual server at UCW Data Center, Vancouver. | Path: AWSDataCenter-UCW-Virginia-FOE-GVS-EBS<br>Dataset is stored in EBS of a Finance Operational Environment virtual server in the AWS Virginia Region. | The dataset is stored in two locations:<br>Path1: UCWDataCenter-Vancouver-FOE-GVS-RAM-HDD<br>Dataset is stored in RAM and HDD of a Finance Operational Environment virtual server at UCW Data Center.<br><br>Path2: AWSDataCenter-UCW-Virginia-FOE-GVS-EBS<br>Dataset is also stored in EBS of a Finance Operational Environment virtual server under UCW's AWS account, in Virginia. | The dataset is stored in two different cloud providers:<br>Path1: AzureDataCenter-UCW-FOE-GVS-RAM-HDD (Azure Service)<br>Dataset is stored in RAM and HDD (Azure Service) of a Finance Operational Environment virtual server under UCW's Azure account.<br><br>Path2: AWSDataCenter-UCW-Virginia-FOE-GVS-EBS<br>Another copy of the dataset is stored in EBS of a Finance Operational Environment virtual server under UCW's AWS account, in Virginia. |
| **Dataset - Access** | Access is internal, it is limited to UCW Finance Operational network users in Vancouver | Access is broadly available online and public for UCW Finance Operational network users from multiple locations in AWS Virginia Regions. | Access is split, sensitive data on private cloud (UCW Data Center), general data on public cloud (AWS Data Center).<br>The dataset access level is for UCW Finance Operational network users | Access is distributed across different providers but managed by a unified UCW system.<br>The dataset access level is for UCW Finance Operational network users. |
| **Dataset - Privacy** | UCW has full control over data protection and compliance, which is very high privacy. | Although data is in shared environments, it uses the encryption and IAM policies. The privacy is low. | Because the data is stored in private cloud, so sensitive data remains private, and less critical data can be public. The privacy is balanced. | The privacy can be varied by multiple providers, so it requires strong governance to ensure consistent privacy standards for all providers. |

<p float="left">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/eff90273-7ff7-444e-8838-d6007ccb1a3b" />
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/91a23a2c-939e-4520-ba38-07c67278b6db" />
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/28976b93-2fa0-44ea-a009-aa30a195288a" />
</p>

### Case Study #3: Cloud Service Models
- The table below compares the IaaS, PaaS, SaaS Model through the management of expense claim datasets in UCW’s Finance Operational Environment.

| Dataset: Expense Claims | **IaaS** | **PaaS** | **SaaS** |
|-------------------------|----------|----------|----------|
| **Dataset - Location** | Path: AWS Data Center → UCW Account → Virginia → Availability Zone 1-a → FOE → EBS<br><br>The dataset is stored in EBS of a Finance Operational Environment in the AWS Virginia Region. | Path: AWS Data Center → UCW Account → Virginia → Availability Zone 1-a → FOE → Platform<br><br>The dataset is logically stored by the platform, which uses EBS in the background but Finance Operational team do not manage EBS. | AWS Data Center → UCW Account → Virginia → Availability Zone 1-a → FOE → SaaS Software<br><br>The dataset is stored within the SaaS software but managed and protected by the SaaS provider, not by UCW. |
| **Dataset - Access** | Finance Operation Team has full access to EC2 and EBS, they can manage OS, storage, and dataset. | Finance Operation Team has access through platform tools like database query interface.<br><br>AWS Operation Team mainly manages EC2, EBS. | Finance Operation Team has access only via software interface such as web dashboard, forms, reports.<br><br>AWS Operation Team can manage both infrastructure and software updates. |
| **Dataset - Privacy** | Full responsibility of the Finance team.<br>The team must implement all privacy controls, including data encryption, access policies, and compliance. | It is a shared responsibility:<br><br>Finance team controls data inputs, users, permissions inside platform.<br>AWS Operation team secures underlying infrastructure, backups. | Users in this structure has limited control.<br><br>Privacy relies on the SaaS provider’s compliance while the Finance team manages user permissions like access roles within the software. |

<img width="952" alt="image" src="https://github.com/user-attachments/assets/83ba378f-5c83-465a-8179-3f0faaaa0846" />

### AWS Knowledge Check - Module 1: Cloud Concepts Overview
<img width="500" alt="image" src="https://github.com/user-attachments/assets/e732c9ea-789a-44bd-b062-56bee321b120" />

## AWS Cost Analysis 
- This module focuses on AWS cost optimization, pricing models, and financial management tools. It also explores total cost of ownership (TCO), AWS Organizations for account structuring, billing and cost tracking, and the available technical support plans for effective cloud operation.

### Case Study #4: Total Cost Of Ownership - Delaware North
- This case study demonstrates how migrating to AWS and using EC2 Reserved Instances helped a large enterprise reduce infrastructure costs, improve operational efficiency, and accelerate time to market.

| **Section** | **Details** |
|-------------|-------------|
| **Background** | A fast-growing company with over 200 locations<br>500 million customers and $3 billion yearly revenue. |
| **Challenge** | Needed to launch new solutions quickly<br>Had to replace old equipment often |
| **Criteria** | - Wanted one solution for all workloads<br>- Needed to improve processes and cut costs<br>- Aimed to remove tasks like software updates<br>- Wanted a good return on investment (ROI) |
| **Solution** | Moved data center to AWS: shut down 205 servers (90%) and moved most apps to the cloud.<br>Used 3-year Amazon EC2 Reserved Instances to save money |
| **Result** | **Enhanced 24/7 Business Efficiency**<br>• **Resource Optimization**: Strong security, better disaster recovery, more computing power<br>• **Speed to Market**: new business setup in one day, launch a service in minutes<br>• **Operational Efficiency**: ongoing cost saving and control |

### Case Study #5: AWS Pricing Calculator
- This case study evaluates the estimated AWS costs for implementing a basic data pipeline, including data storage, data profiling/cleaning, and data analysis. Using Amazon S3, AWS Glue DataBrew, and Amazon Athena respectively, the estimated total annual cost is $145.78 USD, demonstrating how AWS enables low-cost, pay-as-you-go solutions for end-to-end data processing in the cloud.

<p float="left">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/e864416f-8cc3-4af1-b894-1c843d6670de" />
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/cc3ccecf-ec41-4edd-acbd-dac760407d4d" />
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/07a8a232-d49c-4f60-a83b-e0108d832030" />
</p>

### Case Study #6: Support Plan
- This case study highlights the importance of selecting the Business Support Plan for finance departments that require high availability, fast issue resolution, and ongoing access to AWS technical expertise.

| **Department** | **Support Plan**          | **Justification** |
|----------------|----------------------------|-------------------|
| Finance        | Business Support Plan      | Finance teams often handle sensitive data and must comply with high availability and security standards. Therefore, the Business Plan supports multiple services, ideal for databases, automation, and reporting tools.<br><br>For example, assuming that my team runs a finance dashboard on AWS that uses EC2 and S3. If an issue occurs, Business Support Plan gives my team 24/7 access to engineers and faster response times, so finance reports and payroll systems will not go down during critical hours. |

### AWS Knowledge Check - Module 2: Economics and Billing
<img width="500" alt="image" src="https://github.com/user-attachments/assets/02997527-8099-46f8-adf4-3b7ea9236410" />

## AWS Global infrastructure 
- This module introduces the structure of AWS’s global infrastructure, including key components such as regions, availability zones, and data centers.

### Case Study #7: AWS Global Infrastructure
- This case study compares how an Expense Claims dataset behaves across different AWS infrastructure layers such as Regional Edge Cache, Edge Location, and AWS Region in terms of location, access, and privacy, highlighting the trade-offs between performance, control, and data protection.

| **Dataset: Expense Claims** | **Regional Edge Cache** | **Edge Location** | **Region** |
|-----------------------------|--------------------------|-------------------|------------|
| **Dataset - Location** | The Expense Claims is not stored in Seattle Regional Edge Cache because the dataset need to be updated frequently for ClaimDate feature. Caching is not suitable. | Path: Vancouver Edge Location<br><br>Student accesses content through the nearest Vancouver Edge Location, which holds a short-term cached copy of the dataset. | Path: UCW → FOE → AWS Region (Virginia/Oregon) → Availability Zone (1-a) → AWS Data Center → EBS<br><br>The student’s request first goes through the Edge Location to check for cached content. If not found, the request continues to the main AWS Region (Virginia/Oregon), where the full dataset is stored in EBS storage inside UCW’s Finance Operational Environment (FOE). |
| **Dataset - Access** | Not used due to frequent updates and caching is not suitable.<br>No access control is applied. | Student only read access to cached content. | Finance Operational Team has full access read/write.<br>Students has no access to directly manage the dataset, they can access indirectly through dashboard or portal only. |
| **Dataset - Privacy** | Not used due to frequent updates and caching is not suitable.<br>No privacy control is applied. | Moderate privacy because data is cached temporarily with encryption, but no updates or personal records are stored. | High privacy because full control, encryption, access control, and compliance are handled by UCW and AWS provider (example EBS encryption, IAM roles). |

<img width="500" alt="image" src="https://github.com/user-attachments/assets/dd9e8468-ac9b-4c86-bf9f-c194292e3b75" />

### AWS Knowledge Check - Module 3: AWS Global Infrastructure Overview
<img width="500" alt="image" src="https://github.com/user-attachments/assets/fd18e50f-36e8-4b4a-9728-74fbd2f99fd0" />

## AWS IAM 
- This module explains the AWS Shared Responsibility Model and dives into Identity and Access Management (IAM), how security tasks are divided between AWS and customers, and how to manage user authentication, authorization, and permissions effectively.

### Case Study #8: Who is responsible
- This case study outlines the division of responsibilities between UCW and AWS across different layers of the cloud stack (EC2, platform, software, and dataset). The results show that while AWS ensures infrastructure and platform availability, UCW is responsible for software operations and securing finance datasets (Expense Claims).

|                          | **UCW Responsibility**                                                                 | **AWS Responsibility**                                                                 |
|--------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **EC2**                  | **No control**                                                                         | **Fully responsible** for creating, processing and security of EC2 instances           |
| **Platform**             | **No control**                                                                         | **Fully responsible** for maintaining the platform service and ensuring it runs properly |
| **Software**             | **Fully responsible** for managing and operating finance software (example Expense Claims app) | **No responsibility** in software management                                           |
| **Dataset (ExpensesClaims)** | Responsibility for **entering, using, and securing** the dataset                        | **No control**                                                                         |

<img width="500" alt="image" src="https://github.com/user-attachments/assets/72847c02-bb25-49af-9187-61fbde465313" />

### Case Study #9: IAM practice: Lab 1
- This case study provides hands-on experience with AWS Identity and Access Management (IAM), where it explores the structure and function of IAM users, groups, and policies in a real-world cloud environment. The case study involves adding users to different IAM groups (S3-Support, EC2-Support, EC2-Admin), logging in as those users, and verifying access permissions by attempting EC2 stop instance actions (Image below).

<img width="500" alt="image" src="https://github.com/user-attachments/assets/33851d39-280d-43e6-ac28-94d33ed01a39" />

✅ Tasks Completed
- Explored pre-created **IAM users and groups** in an AWS account.
- Inspected **IAM policies** tied to each group (`EC2 Admin`, `EC2 Support`, `S3 Support`).
- Assigned users (`user-1`, `user-2`, `user-3`) to groups based on their required access levels.
- Used the **IAM sign-in URL** to log in as each user and verify their permissions.
- Tested permissions to confirm **group-specific access**:  
  - `user-3`: full EC2 access (start/stop)  
  - `user-2`: EC2 read-only access  
  - `user-1`: S3 read-only access

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e672eff6-242d-4e4c-945d-1c3247586970" />

### AWS Knowledge Check - Module 4: AWS Cloud Security

<img width="500" alt="image" src="https://github.com/user-attachments/assets/fae6b1eb-9d0e-4833-9204-2a67231fbfc6" />

## AWS VPC
- This module provides a comprehensive overview of AWS networking, covering fundamental concepts, Virtual Private Cloud (VPC) configurations, advanced networking options, and security controls such as security groups and network ACLs.

### Case Study #10: Build your VPC: Lab 2
- In this lab, the learner used Amazon Virtual Private Cloud (VPC) to build a custom network environment, including subnets and security settings, and launched an EC2 instance running a web server. The exercise demonstrated practical skills in deploying foundational cloud networking components, reinforcing concepts of VPC design, routing, security groups, and compute instance provisioning.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b10889b7-943c-44fa-8996-54faebca2fff" />

✅ Tasks Completed
- Created a custom VPC.
- Created and configured new subnets.
- Associated subnets with a custom route table.
- Created a security group with appropriate rules.
- Launched an EC2 instance in the VPC.
- Verified web server accessibility from the EC2 instance.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4dad3c1d-f8c1-4117-8696-9a7887551aef" />

### AWS Knowledge Check - Module 5: Networking and Content Delivery

<img width="500" alt="image" src="https://github.com/user-attachments/assets/088a7ae9-07a3-4b9f-bf7b-d6c4faa683c4" />

## AWS Lambda 
- This module introduces AWS Lambda and AWS Elastic Beanstalk, focusing on their core concepts, configurations, event sources, and deployment benefits for running serverless and managed application environments.

### Case Study #11: Create an AWS Lambda function
- In this hands-on lab, the task is to create an AWS Lambda function triggered by an Amazon EventBridge rule to stop an EC2 instance on a scheduled basis. The function should be configured with an IAM role to securely perform EC2 operations, simulating a real-world server automation use case using serverless architecture. This case study illustrates the power of event-driven automation in managing cloud infrastructure efficiently and securely.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/5bcbe386-a2f3-416e-ad5c-9fb0d8499963" />

✅ Tasks Completed
- Created an AWS Lambda function.
- Configured a scheduled EventBridge rule to trigger the function every minute.
- Assigned an IAM role with permissions to stop EC2 instances.
- Verified Lambda function successfully stopped an EC2 instance.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b02de286-d334-4153-98b4-f8c9a84ec06b" />

### AWS Knowledge Check - Module 6: Compute

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7be2d0aa-3c31-4063-a4fc-8c93ac5a4d76" />

## AWS EBS
- This module introduces AWS storage services, including Amazon EBS, S3, EFS, and S3 Glacier, it focuses on their features, architectures, pricing models, and use cases for scalable, durable, and secure data storage solutions in the cloud.

### Case Study #12: Working with Amazon EBS: Lab 4
- In this lab, the task is to practice using Amazon Elastic Block Store (EBS) by creating and attaching a volume to an EC2 instance, mounting and writing to it, then taking a snapshot and restoring that data onto a new volume. The activity emphasized backup, persistence, and recovery of block-level storage in a real-world cloud environment.

<img width="508" alt="image" src="https://github.com/user-attachments/assets/05bcc6ac-b222-4593-835a-e884dd15d3f5" />

✅ Tasks Completed
- Created an Amazon EBS volume.
- Attached the volume to an EC2 instance.
- Mounted the volume and applied a file system.
- Created and saved a file to the volume.
- Took a snapshot of the volume.
- Created a new volume from the snapshot.
- Attached and mounted the new volume to the EC2 instance.
- Verified that the file created earlier was present in the restored volume.

<img width="508" alt="image" src="https://github.com/user-attachments/assets/daeeb67f-0f9b-4c5c-93d8-6044e1a8bba9" />

### AWS Knowledge Check - Module 7: Storage

<img width="508" alt="image" src="https://github.com/user-attachments/assets/acbc1fdb-0e36-4a0b-8a60-082be383727c" />
