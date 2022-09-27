# Amazon_Vine_Analysis Overview
In this module, we are working with Jennifer on the SellBy project. We will be analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.  We will have access to approximately 50 datasets. Each one contains reviews of a specific product. Then we will pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. We’ll finish by writing a summary of the analysis for Jennifer to submit to the SellBy stakeholders.
## Deliverable 1
- We first reviewed An Amazon dataset for toys then extracted as a DataFrame 
- We use extracted dataset to transform into four DataFrames with the correct columns(review_id_table, product_table, vine_table and customers_table)
The 4 dataframes were loaded in PGAdmin then export to github.
## Deliverable 2
- We create a DataFrame for the vine_table data 
- We filtered to create a DataFrame <= 20 total votes
- We created a DataFrame where the percentage of helpful_votes is =< 50%
- We filtered to create a DataFrame where there is a Vine review
- Then we filtered to create a DataFrame where there isn’t a Vine review
- We determined the total number of reviews, the number of 5-star reviews, and the percentage 5-star reviews are calculated for all Vine and non-Vine reviews.
