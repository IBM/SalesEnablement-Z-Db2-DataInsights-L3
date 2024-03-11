# AI at scale on IBM Z using Db2 for z/OS SQL Data Insights

## Demonstration using IBM Virtual Development and Test for z/OS, Db2 for z/OS V13 with SQL Data Insights.

*Gain more data insights with AI-Enabled query in Db2 for z/OS*

!!! Important "Prerequisites"

    **Before undertaking this lab, you are expected to understand:**

    - Db2 for z/OS
    - The SQL language
    - Artificial Intelligence (AI) concepts
    - Machine Learning and Deep Learning model concepts
  
## Db2 for z/OS SQL Data Insights

Artificial Intelligence (AI) has become an essential capability for enterprises to exploit and master. The data that is stored and managed in operational databases contains information that is invaluable to making informed decisions. Sometimes the insights can be extracted using conventional Structured Query Language (SQL) queries. But when the information clients seek is hidden in non-obvious patterns in the data, conventional SQL is not flexible enough to see those patterns.

Db2 for z/OS SQL Data Insights is a transformational technology, that enables Deep Learning AI models to be trained against mainframe data, so that anybody who writes SQL queries can invoke standard SQL functions to understand the data patterns without any need for data science expertise. Db2 for z/OS SQL Data Insights is also called SQL Data Insights through this document.

The illustration below represents how Db2 for z/OS SQL Data Insights would be used.

- The Clients table holds information about the clients of a business.
- The related model table is created when SQL Data Insights is instructed to Enable AI.
- The example SQL query aims to find the top 20 clients who are most similar to the client with customer ID of 3668-QPYBK. The client in question may be of interest because of good or bad outcomes to be encouraged or avoided in other clients.
- The first version of SQL Data Insights (DB2 13 FL500) provides 3 built-in functions: AI_SIMILARITY, AI_SEMANTIC_CLUSTER and AI_ANALOGY. All AI functions are based on the unsupervised neural network model that has been trained to find natural patterns in the data. In the case of the AI_SIMILARITY function, it computes a similarity score between any two records in an AI-enabled table.
- SQL queries can be submitted from anywhere with a SQL connection to Db2.

![](_attachments/AI%20at%20scale%20on%20IBM%20Z%20using%20Db2%20for%20zOS%20SQL%20Data%20Insights%20Workbook%20-%202024-Feb-26.jpg)

This demonstration will be focused on the steps that the Database Administrator takes to **Enable AI** against Db2 tables and views, and the SQL query patterns that business users need to adopt to perform **AI-Enabled queries**.

This use case applies to IBM clients that have the following environment:

^^Mandatory^^

- They are running Db2 for z/OS V13 Function Level 500 or later.
- They must have installed the optional SQL Data Insights feature of Db2.

^^Nice to have^^

- The subject data should include as many **features** as possible that describe the characteristics of the entity (for example: Client) being studied.
- Ideally, good or bad outcomes **labels** are included within the data, to provide a focus for AI enabled queries to use.
- Model training with SQL Data Insights is CPU-intensive but is almost totally zIntegrated Information Processor (zIIP) eligible. Available zIIP engines for model training help to avoid unwanted general processor CPU consumption.

^^Other considerations to be evaluated^^

- Operational databases tend to store data in multiple different tables, such as with third normal form data models. The objective of such data structures is to separate data into different entities (tables) for flexibility. This is the opposite of what is wanted for machine learning. Clients should consider using SQL views to join data from multiple tables to include all the data fields that are of interest in AI-enabled analysis.
- Data stored outside Db2 for z/OS can also be used by SQL Data Insights. For example, data in Virtual Storage Access Method (VSAM) datasets or Information Management System (IMS) databases can be references in Db2 table functions, so that they too can be **AI-Enabled**.