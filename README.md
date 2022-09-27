# Amazon_Vine_Analysis Overview
In this module, we are working with Jennifer on the SellBy project. We will be analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.  We will have access to approximately 50 datasets. Each one contains reviews of a specific product. Then we will pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. We’ll finish by writing a summary of the analysis for Jennifer to submit to the SellBy stakeholders.
## Deliverable 1
1- We first reviewed An Amazon dataset for toys then extracted as a DataFrame 

![dataset](https://user-images.githubusercontent.com/103543959/192582654-0b3fef20-83bc-45b4-9533-e86721923897.png)

2- We use extracted dataset to transform into four DataFrames with the correct columns: 
- review_id_table
- product_table
- vine_table
- customers_table)
The 4 dataframes were loaded in PGAdmin then export to github.
## Deliverable 2
1- We create a DataFrame for the vine_table data 

![vine_df](https://user-images.githubusercontent.com/103543959/192584627-30c77bd8-e24d-466b-8dc1-f23a3482026c.png)

2- We filtered to create a DataFrame <= 20 total votes

![total_votes_filter](https://user-images.githubusercontent.com/103543959/192584703-16afc953-e54f-411d-9e58-51bc29d90bb1.png)

3- We created a DataFrame where the percentage of helpful_votes is =< 50%

![votes_filter2_df](https://user-images.githubusercontent.com/103543959/192584758-92f2d637-96f0-4a66-8a64-20a581fd88b3.png)

4- We filtered to create a DataFrame where there is a Vine review for paid

![review_filter_df](https://user-images.githubusercontent.com/103543959/192585082-c0b44456-fc48-49a1-bfce-fc9ed3cbca26.png)

5- Then we filtered to create a DataFrame where there isn’t a Vine review

![review_filter2_df](https://user-images.githubusercontent.com/103543959/192585108-64ff63d4-75f8-4c7f-b501-cc9cfc2d5fe7.png)

6- We determined: 
- the total number of reviews

![Total_review](https://user-images.githubusercontent.com/103543959/192583470-4e20e069-931f-4a64-ba09-69416c9dc2df.png)

- the number of 5-star reviews

![five_star](https://user-images.githubusercontent.com/103543959/192584064-858da0a0-b4d6-40e1-a2d7-9023381067a6.png)

- the percentage 5-star reviews for all Vine 

![Percentage_paid](https://user-images.githubusercontent.com/103543959/192584374-f831609b-c402-4148-8262-3f5c636833a0.png)

- the percentage 5-star reviews for all non-Vine reviews

![Percentage_unpaid](https://user-images.githubusercontent.com/103543959/192585854-33dbf483-08ae-4dd3-b769-23c8846fbd32.png)

### Summary
To resume, we think there is not much positivity bias state for five star reviews in the Vine program. The percentage of five reviews is only 48 %. The unpaid Five star review is 55% which still remain unpaid. Then another analysis, we could do with is to calculate the five star percentage of helpful votes. 
