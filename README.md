# Amazon_Vine_Analysis

## Overview of the analysis: 
In this project, we are analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
We used PySpark to perform the ETL process to extract a dataset about baby products and connect to an AWS RDS instance. Then, the transformed data was loaded into pgAdmin. Next, we used Pandas to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

 ## Results: 
We filtered the vine data to retrieve all the rows where the total votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors later. From the filtered, data we retrieved all the rows where the number of helpful votes divided by total votes is equal to or greater than 50%. As a result we got: 
