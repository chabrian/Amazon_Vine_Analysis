# Amazon_Vine_Analysis

## Overview of Vine Review Analysis

In this project, I have been tasked with analyzing Amazon product reviews for items under the shoes category. The intent of the analyze was to determine any bias towards reviews that were written as part of the Vine program. The metric being used for this analysis is the percentage of 5-star reviews for a product. The process involved filtering the data using PySpark and creating dataframes showing the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for paid vs unpaid reviews. The full set of resources and analysis results are shown below.

## Resources

- Data Sources: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Shoes_v1_00.tsv.gz
- Software: Google Colaboratory, PySpark v3.2.1

## Analysis Results

The set of results were derived using the Amazon reviews dataset and transforming the tables to create the summary table displayed below. The data was filtered with the criteria that the total vote count is greater than or equal to 20 and the proportion of helpful votes is greater than or equal to 50%.

<img width="333" alt="Total_Reviews" src="https://user-images.githubusercontent.com/95327115/162653427-ad72fcac-7cf0-4ee5-b950-262e763558a2.png">
<img width="492" alt="5Star_Reviews" src="https://user-images.githubusercontent.com/95327115/162653425-44ab9cfb-6272-4164-b390-d3b471fcec03.png">
<img width="333" alt="5Star_Percent" src="https://user-images.githubusercontent.com/95327115/162653424-7e6b0b3a-7c9b-4a1c-baa0-d87eb4bdfbb9.png">

The following points can be made about the results above:

- In this filtered dataset, there were 20 total Vine (paid) reviews and 25,116 total non-Vine (unpaid) reviews.
- Out of the 20 Vine reviews, 12 were 5-star reviews. 13,479 of 25,116 non-Vine reviews were 5-stars.
- 60% of Vine reviews were 5 stars and 53.6% of non-Vine reviews were 5 stars.

## Summary Statistics on Suspension Coils

The summary table shows evidence of positivity bias for reviews in the Vine program. The Vine program is a minority of the total reviews but yielded an increase of 6.4% more five star reviews. Based on this information we cannot conclude that positivity bias exists for paid reviews compared to unpaid reviews due to the small smaple size of the paid reviews after filtering for relevant reviews.
For a more robust analysis, we could perform an additional query on the dataset that looks at the average star rating for the Vine and non-Vine programs. If positivity bias exists, we should see a greater average star rating for Vine reviews. We would also need to gather more data on the paid reviews in order to gain confidence in our analysis results.
