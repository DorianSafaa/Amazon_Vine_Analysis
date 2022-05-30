# Amazon_Vine_Analysis

## Overview of the analysis

In this project, we are analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
We used PySpark to perform the ETL process to extract a dataset about baby products and connect to an AWS RDS instance. Then, the transformed data was loaded into pgAdmin. Next, we used Pandas to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

## Results

We filtered the vine data to retrieve all the rows where the total votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors later. From the filtered, data we retrieved all the rows where the number of helpful votes divided by total votes is equal to or greater than 50%. As a result we got: 

•	We have 463 Vine reviews and 25094 non-Vine reviews.

•	The Vine reviews had 202 5 star ratings and the non-Vine reviews had 12033 5 star ratings.

•	Nearly 44% of Vine reviews were 5 stars, and 48% of non-Vine reviews were 5 stars.

![Capture](https://user-images.githubusercontent.com/66279829/170939494-cb682b69-7440-4397-996e-445d8c05b2b4.PNG)

## Summary

The percentage of the 5 stars reviews for Vine members is 44% and 47% for the non-Vine members. Considering that the percentages are close, we can conclude that there is no bias in the reviews. The majority of the members who gave the product 5 stars were honest in their reviews. Additionally, we can conduct a statistical test to confirm whether the percentages of 5 stars reviews from Vine and non-Vine members are equal. The test statistic for testing the difference in two population proportions is the z test. the result of the test will help us in conforming whether there are any positive bias in the Vine reviews. 
