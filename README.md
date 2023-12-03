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

Snowflake editions:
* Standard - 2 USD per credit
* Enterprise - 3 USD per credit
* Business Critical (advanced security and protection) - 4 USD per credit
* Virtual Private Snowflake (VPS) - isolated Snowflake environment for superb protection. - price TBD
