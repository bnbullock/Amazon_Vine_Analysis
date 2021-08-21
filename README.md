# Amazon_Vine_Analysis


## Project Overview

Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

- Deliverables:
  1. Using Python, update the CSV bike trips CSV file.
  2. Create 5 different visualizations in Tableau

------------------------------------------------------------------------------------------------------------

## Resources
- Software: Visual Studio Code 1.56.2, Python 3.7.10, 
- Libraries: PySpark
- Browser : Google Chrome v91.0.4472.124 
- Data Source: AWS Cloude DB, PostgreSQl v12.7
- Data Client: pgAdmin v5.5

------------------------------------------------------------------------------------------------------------

## Results

### Perform ETL on Amazon Products Reviews

- Extract Reviews using PySpark in Google Colab Notebooks

![Image1](images/1CreateTables_1.png)


- Transform dataframe into Functional SQL Tables

![Image2](images/2LoadedTables1.png)

- Load Tables with Data

![Image3](images/3CountTableRows1.png)


## Determination of Bias in Vine Reviews

- Is there a difference in paid Vine reviews?


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