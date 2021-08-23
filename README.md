# Amazon_Vine_Analysis

## Project Overview

We have been tasked by a client with analysing differnet Amazon reviews that have been written by members of the paid Amazon Vine program. This service allows manufactures and publishers to receive reviews for their products directly from Amazon Vine members. The clients pay a fee to Amazon and provide products directly to Amazon Vine members who are then required to publish a related product review.

Amazon has provided access to approximately 50 different datasets, each one contains specific reviews for specific product categories. We are asked to  select a dataset specifically relevant to our client which contains reviews and feedback specific to one of their products. Once we have selected the client-spefic dataset, we will use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Secondly, we have the choice of using PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in the dataset. In our case, we will be using PySpark for this section of the data analysis and then annotating a summary of the results for our client to review along with their stakeholders. The dataset we will be using from Amazon are the "Digital Software" reviews recorded by both Vine and non-Vine members.

- Deliverables:
  1. Peform an ETL function using Amazon AWS, Google Colab Notebooks and pgAdmin.
  2. Calculate matrics to determine if a paid Vine review make a difference in the percentage of 5-star reviews.

------------------------------------------------------------------------------------------------------------

## Resources
- Software: Visual Studio Code 1.56.2, Python 3.7.10, Google Collab Notebook
- Libraries: PySpark, OJS v11, PySpark v3.0.3
- Browser : Google Chrome v91.0.4472.124
- Data Source: AWS Cloude DB, PostgreSQl v12.7
- Data Client: pgAdmin v5.5
- Data : https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Digital_Software_v1_00.tsv.gz
------------------------------------------------------------------------------------------------------------

## Results

### Perform ETL on Amazon Products Reviews

- The Digital Software dataset was loaded into a singular dataframe directly from Amazon. From this master dataframe, four additional distinct dataframes were generated and loaded into 4 different SQL tables. Each table was created using a schema that matched the corresponding dataframe exactly as extracted using Google Collab notebook and PySpark.

![Image1](images/1CreateTables_1.png)

- Likewise to above, each dataframe was transformed into the correct format with duplicated data removed, dates re-formatted and values aggregated as necessary. Below we can see an example of the different fields associated with the vine_table and the related data.

![Image2](images/2LoadedTables1.png)

- Finally each transformed dataframe was loaded into the corresponding postgreSQL database table. We can see the vine_table below containing 102084 data records of reviews.

![Image3](images/3CountTableRows1.png)


## Determination of Bias in Vine Reviews

- For the second part of this task we are challenged to validate if there is bias associated with 

![Image4](images/3VineSummary1.png)

------------------------------------------------------------------------------------------------------------

## Overall Summary

For this part of the Challenge, you’ll write a report that summarizes the analysis you performed in Deliverable 2.

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists and images of DataFrames as support, address the following questions:

How many Vine reviews and non-Vine reviews were there?
How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use 
the results of your analysis to support your statement. Then, provide one additional analysis that you 
could do with the dataset to support your statement.