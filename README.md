# Snowflake Info

* Snowlake Youtube tutorial: https://youtu.be/AR88dZG-hwo?si=ooKhbVR6JLn_2aOz
* Official Snowflake Docs & Guides: https://docs.snowflake.com/

### Certification:
* SnowPro Core (Fundamentals): https://learn.snowflake.com/en/certifications/snowpro-core/
  - Registration fee: $175 USD
  - Total Number of Questions: 100
  - Passing Score: 750 + Scaled Scoring from 0 - 1000
* SnoPro Advanced Data Engineer: https://learn.snowflake.com/en/certifications/snowpro-advanced-dataengineer/
  - Total Number of Questions: 65
  - Registration fee: $375 USD
  - Passing Score: 750 + Scaled Scoring from 0 - 1000
* Sample practive exam: https://learn.snowflake.com/en/certifications/snowpro-practice-exams/
  - Total Number of Questions: 40
  - Registration fee: $50 USD

### Architecture

Snowflake architecture is a hybrid of traditional shared disk (central data repo) and shared nothing architectures (process queries using MPP - massively parallel processing)

Three layers:
* Service layer
* Compute layer
* Storage layer

![image](https://github.com/nikvolynets/snowflake-info/assets/151893648/c071cb70-5b29-43e2-b6f0-61ef5bdd3088)

Virtual warehouse is an MPP compute cluster composed of multiple compute nodes.

Services managed in Service layer include:
* Authentication
* Infrastructure management
* Metadata management
* Query parsing and optimization
* Access control

Compute pricing:
* Standard - 2 USD per credit
* Enterprise - Standard + Multi-cluster warehouse - 3 USD per credit
* Business Critical (advanced security and protection) - 4 USD per credit
* Virtual Private Snowflake (VPS) - isolated Snowflake environment for superb protection. - price TBD

Storage pricing:
* On Demand: Usage-based pricing with no long-term licensing requirements. 40 USD per TB
* Capacity: Discounted pricing based on an upfront Capacity commitment. 23 USD per TB

### Virtual Warehouses

A cluster of compute resources in Snowflake. Two types:

* Standard
* Snowpark-optimized

Warehouse uses CPU, memory, and temporary storage, to perform the following operations in a Snowflake session:

* Executing SQL SELECT statements that require compute resources (e.g. retrieving rows from tables and views).
* Performing DML operations (DELETE, INSERT, UPDATE, COPY INTO)

Warehouse sizes: X-Small (1 credit/hour), Small (2), Medium (4), Large (8), ... , 6X-Large (512)
Snowflake utilizes per second billing with minimum of 60 seconds

Multicluster WH allows to use from 1 up to 10 clusters for WH. 

Properties:
* Auto-resume
* Auto-suspend
* Scaling policy (Standard, Economy)

Scaling:
* Scaling up by resizing WH
* Scaling out by adding clusters in WH

### DDL commands for WH

```sql
CREATE (or ALTER) WAREHOUSE <name>
WITH WAREHOUSE_SIZE = 'XSMALL'

USE WAREHOUSE <name>

GRANT CREATE|MANAGE WAREHOUSES TO ROLE <role_name>
```
