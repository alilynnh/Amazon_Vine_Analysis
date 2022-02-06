# Amazon Vine Analysis
## Project Overview
The Amazon Vine program is a service that allows manufacturers and publishers to generate reviews for their products. The companies involved pay a small fee to Amazon, and Amazon then provides the companies' products to Amazon Vine members. These Vine members are then required to publish a review on the products. The purpose of this project was to determine if there is any bias toward positive reviews from Vine members. The data set analyzed for this project included Amazon reviews for pet products. 

### Resources 
- Data: [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), [Pet Product Review Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz)     
- Software: Google Colab Notebook, PostgreSQL, pgAdmin, AWS

## Results
- The number of non-Vine reviews far exceeded the number of Vine reviews.  
<p align="center" width="100%">
    <img src="Resources/paid_total.png" width="50%" height="50%">    
    <img src="Resources/unpaid_total.png" width="50%" height="50%">  
</p>

- The number of 5-star non-Vine reviews greatly exceeded the number of 5-star Vine reviews.
<p align="center" width="100%">
    <img src="Resources/paid_5star.png" width="75%" height="75%">   
    <img src="Resources/unpaid_5star.png" width="75%" height="75%">  
<p/>

- The non-Vine reviews had a higher percentage of 5-star reviews than the Vine reviews. 
<p align="center" width="100%">
    <img src="Resources/paid_percentage.png" width="50%" height="50%">    
    <img src="Resources/unpaid_percentage.png" width="50%" height="50%">   
</p>

## Summary
Unexpectedly, there does not appear to be a positivity bias for Vine reviews in this data set, as 54% of the non-Vine reviews were 5-star and only 38% of the Vine reviews were 5 star. However, it may be worthwhile to examine the median and standard deviation of the reviews for each group, as it's possible that the Vine group may have less 1 and 2-star reviews than the non-Vine group. In addition, it would be interesting to determine how much of an effect the Vine reviews have on the average rating of a products. This could be evaluated by selecting a specific product which has a large number of reviews, getting the average rating with and without Vine reviews included, and then comparing the two averages using a t-test. 