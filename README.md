# Amazon_Vine_Analysis
Module 17: Big Data

## Overview

We've been tasked with analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program facilitates manufacturers and publishers in receiving reviews of their products. Companies like SellBy can pay a fee to Amazon and provide products to Amazon Vine Members. In return, those members are required to publish a review of the products. To complete our analysis, we'll use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. We can then use PySpark to determine if there is any bias toward favorable reviews from Vine members(paid) in the dataset.

This assignment consists of two technical analysis deliverables and a written report:
- Deliverable 1: Perform ETL on Amazon Product Reviews
- Deliverable 2: Determine Bias of Vine Reviews
- Deliverable 3: A Written Report on the Analysis (README.md)

## Resources
- Data Source: [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) --> [Pet Products Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz)
- Sofrware: [Google Colaboratory](https://colab.research.google.com), [PySpark 3.2.3](https://spark.apache.org/docs/3.2.3/api/python/getting_started/install.html), [Visual Studio Code 1.70.2](https://code.visualstudio.com), [pgAdmin 4](https://www.pgadmin.org/download/) / [PostgreSQL 15.1](https://www.postgresql.org/docs/current/release-15-1.html)

## Results 
- To view our ETL process --> [Click Here](https://github.com/abrodyyy/Amazon_Vine_Analysis/blob/main/Amazon_Reviews_ETL.ipynb)
- To view our Vine Review Analysis process --> [Click Here](https://github.com/abrodyyy/Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb)


Review Type       | Total Reviews | 5 Star Reviews | % of 5 Star Reviews
----------------- | ------------- | -------------- | -------------------
Vine (paid)	      | 4,103         | 1,704          | 41.5305873750914
Non-Vine (unpaid) |	816,463       | 46,8620        | 57.396354764392264

- From the table above, we can see that there is a total of 820,566 reviews between vine and non-vine members. 
    - Total Paid Reviews: 4,103
    - Total Unpaid Reviews: 816,463
    - 99.5 % of the reviews are unpaid, with only 0.5% of the reviews being from Amazon Vine Members (paid). 
- There were a total of 1,704 5 star reviews from Amazon Vine Members, making up roughly 41.52 % of the distribution. 
- There were a total of 46,8620 5 star reviews from Non-Amazon Vine Members, making up roughly 57.4 % of the distribution. 

## Summary
After completing our analysis, it appears that there is no bias present towards favorable reviews in the Amazon Vine Program. In fact, the total percentage of 5 star reviews is approximatley 15.87% higher in unpaid reviews. With that being said, there are 50 other datasets that may provide additional insights before we can completley rule out any bias. For this reason, I would reccomend further analysis of additional data sets in unique sectors to reach a final conclusion. Additionally, we might want to expand our analysis to include all reviews between 1 and 5 stars for a complete picture of the review distribution. 
