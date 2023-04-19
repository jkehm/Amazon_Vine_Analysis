# Amazon_Vine_Analysis
### Overview
The purpose of this analysis is to see if the Amazon reviews written by members of the paid "Amazon Vine" program is causing the reviews to be skewed in any way when compared to people that are not part of the Vine program. 

In this challenge we will pick a dataset of our choosing, and perform an ETL process. we will extract the dataset, transform the data so it can be easily used, connect to an AWS RDS instance, and load the transformed data into pgAdmin. From there we will use PySpark to determine if there was any bias in the reviews from the Vine members in the data we looked at. 

Due to my interest in cars and motorcycles I chose the Automotive dataset, which can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Automotive_v1_00.tsv.gz)
### Results
Below is a screenshot of the code as well as the output for our Results required in this analysis.
![Here's to hoping this image shows up](https://github.com/jkehm/Amazon_Vine_Analysis/blob/main/Images/Screenshot%202023-04-19%20183621.png)

* How many vine reviews and non-Vine reviews were here
There were a total of 82 Vine reviews, compared to 24,723 reviews for non-Vine members.
* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
Of the Vine reviewers, 33 of them were 5 star reviews. Compared to 12,795 5 star reviews from the non-Vine members.
* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
For vine members, 40.24% of all of the reviews were 5 stars. While for the non-Vine members 51.75% of reviews were 5 stars.
### Summary
Based off of our data, it does not seem that there is any sort of positivity bias for reviewers in the Vine program. Vine-members reviewed 5 stars 40.24% of the time, while non-Vine members were more than 10% more likely to review 5 stars at 51.75%. In fact, the data suggests that Vine members are perhaps more critical than non-Vine members. It could also be worthwhile to run this analysis again. But this time without performing some of the cleaning and filtering that we performed in this analysis. 

Another analysis to do would be to look into the review_id, and see if there are specfic people that may be only reviewing at a certain star rating. If I was a stakeholder at SellBy, that is information I would like to know. 
