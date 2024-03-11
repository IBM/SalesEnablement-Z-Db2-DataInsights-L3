## What is covered in the workbook

**Hands-on demonstration architecture**

![](_attachments/AI%20at%20scale%20on%20IBM%20Z%20using%20Db2%20for%20zOS%20SQL%20Data%20Insights%20Workbook%20-%202024-Feb-26.jpg)

## Using SQL Data Insights to execute AI-enabled SQL queries scenario

In this demonstration scenario, the client’s operational data is stored in Db2 for z/OS, and they wish to take advantage of machine learning techniques to gain better insights into their customer’s needs by learning from patterns in the data that they already possess. They plan to develop predictive models in due course to assist with customer care and the point of interaction, but they wish to start by using AI to gain better insights into their customers’ patterns of activities. You will demonstrate how SQL Data Insights builds an unsupervised Deep Learning model of the clients’ data, so that they may perform simple SQL analysis to take advantage of AI insights for the analytics phase of their journey to AI.

In this demonstration you will be using a Db2 dataset from a telecommunications company (telco), containing 7,043 customer records, of which 1,869 have cancelled their contracts (Churn = Yes). Clients that have a lot of churn going on, may want to identify patterns in the data for customers that haven't yet canceled their accounts, to try retaining them.

Another dataset, the penguin dataset, which is used as a sample dataset for learning data science, will also be used, where the challenge is to use several penguin measurements to build a classification model to determine what species they are. This dataset will be used to validate the ability of SQL Data Insights in finding similarities and differences between records.

### Tasks

**Database Administrator persona**

- Manage the SQL Data Insights Service and enable AI for selected Db2 tables and views.
- Verify the trained SQL Data Insights model with SQL queries.

**Business Analyst persona**

- Refine business data insights requirements.
- Develop SQL queries to address those requirements.

