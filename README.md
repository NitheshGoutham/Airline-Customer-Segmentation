# Airline-Customer-Segmentation
K-Means Clustering: Airline-Customer-Value-Analysis   

## Introduction

This project, Airline Customer Value Analysis, aims to identify distinct customer groups based on key behavioral factors such as flight frequency, travel spending, loyalty status, and other relevant features. By leveraging K-Means clustering, airlines can better understand the value each customer segment brings and tailor their marketing and operational strategies accordingly.


## Domain : Airline Industry

## Technology and Skills Takeaway

-> Basic Python   
-> Data Visualization   
-> Data Cleaning   
-> EDA   
-> Clustering   


## Packages and Libraries   

!pip install numpy     
!pip install pandas   
!pip install scikit-learn      
!pip install matplotlib        
!pip install seaborn   


## Overview

The goal of this project is to divide airline customers into segments and to make business recommendation from the clustering model. The model itself will be built based on LRFMC anaylis that have been used in aviation industry to analyze customer value.
   


## Exploratory Data Analysis (EDA)   

## A. Descriptive analysis   
-> The dataset consists of 5 categorical columns and 18 numerical columns.   
-> Missing values found in feature: Age, Revenue (SUM_YR_1, SUM_YR_2), WORK_CITY, WORK_PROVINCE, WORK_COUNTRY.   
-> 0 duplicate rows found.   

## B. Univariate Analysis   
-> Most of the features have outliers and right-skew distribution.   
-> Most of the customers are 26-60 years old.   
-> Discount feature has some strange values, there are some rows with discount above 100%.   
-> Age has strange maximum values, there is someone 110 years old.   


## Data Pre-Processing   

## A. Missing values handling:   
-> age columns are filled by median value.   
-> Revenue (SUM_YR_1 & SUM_YR_2) are filled by 0.   
-> WORK_CITY, WORK_PROVINCE, and WORK_COUNTRY are dropped because they have too many unique values.   

## B. Remove outlier with z-score   

## C. Feature Engineering Select 5 feature from dataset that will be used for LRFMC analysis:   
-> L : The number of months since the member’s joining time from the end of the observation time. => LOAD_DATE - FFP_DATE   
-> R : Number of months since the member’s last flight from the end of observation time. => LAST_TO_END   
-> F : The total number of times the member has flown during the observation period. => FLIGHT_COUNT   
-> M : Miles accumulated during member observation time. => SEG_KM_SUM   
-> C : The average value of the discount factor used by the member during the observation period. => avg_discount   

## Modelling   

-> Clustering model algorthm: K-Means Clustering   
-> Number of clusters after practicing Elbow Method: 4.   
-> Visualize the cluster model with PCA   
![elbow cluster](https://github.com/NitheshGoutham/Airline-Customer-Segmentation/blob/9ebdac55aee1f729dc3554c576b2e1cad903f711/cluster.jpg)

## Analysis    
-> Cluster summary statistic:   

![cluster statistics](https://github.com/NitheshGoutham/Airline-Customer-Segmentation/blob/9ebdac55aee1f729dc3554c576b2e1cad903f711/statics.jpg)
  

-> Cluster Characteristics :    

Cluster 0 (The Most Loyal Customer)   

Loyalty: The second-oldest members (mean L = 1226.97).   
Recency: The shortest recency (mean R = 437.81), meaning these customers have flown recently.   
Frequency: Highest flight frequency (mean F = 4.64).   
Distance: Highest accumulated flight distance (mean M = 7281.61).   

Cluster 1 (New Customer but Fly Often)   

Loyalty: The newest members (mean L = 2442.08).   
Recency: 2nd most recent (mean R = 110.17), indicating flights occurred not too long ago.   
Frequency: Medium flight count (mean F = 9.06).   
Distance: Medium distance flown (mean M = 12809.19).   

Cluster 2 (Potential Churned Customer)   

Loyalty: The second-newest members (mean L = 872.36).   
Recency: Haven't flown recently (mean R = 99.89), suggesting flights occurred over a year ago.   
Frequency: Lowest flight frequency (mean F = 8.71).   
Distance: Second lowest accumulated miles (mean M = 12477.69).    

Cluster 3 (Casual Customer)   

Loyalty: The oldest members (mean L = 1658.17).    
Recency: Longest recency (mean R = 45.92), with flights spread out over time.   
Frequency: Highest flight frequency (mean F = 27.82).   
Distance: The highest accumulated flight distance (mean M = 39383.89).   


## Business Recommendation   

### 1. Tailor Loyalty Programs:   

Gold: Assign Cluster 0 as Gold members. They exhibit balanced engagement and frequent moderate-distance travel. Offer personalized rewards for consistent usage, such as additional discounts or exclusive benefits for frequent travelers.   

Silver: Assign Clusters 1 and 3 as Silver members. Cluster 1, with high engagement and frequent travel, should receive benefits that emphasize their high activity, such as priority boarding or premium services. Cluster 3, despite being less frequent, should be valued for their long-term loyalty with benefits like anniversary rewards or special offers for long-distance travel.   

Bronze: Assign Cluster 2 as Bronze members. Provide targeted incentives to increase their engagement, such as introductory offers or limited-time discounts, to encourage more frequent travel and longer-term membership.   


### 2. Prevent Churn for Cluster 2:   

Engagement Campaigns: Since Cluster 2 has long flight recency and lower activity, implement campaigns to re-engage them. Use personalized push notifications and special promotions to encourage bookings and prevent them from becoming inactive.   

Special Offers: Offer attractive discounts or deals specifically for Cluster 2 members when they make a booking, to incentivize them to return to active travel.   

### 3. Increase Engagement for Cluster 2:   

Incentives for Activity: Introduce rewards for frequent bookings to motivate Cluster 2 members to travel more often. Consider loyalty points or tiered rewards that increase with the number of flights.   

Personalized Communication: Use data insights to send tailored offers and promotions that match their past behavior and preferences. Engage them with targeted email campaigns and special promotions.   

### 4. Enhance Benefits for Cluster 1 and 3:   

Cluster 1: With high flight count and engagement, offer perks such as additional miles, exclusive access to lounges, or priority services to reinforce their loyalty and encourage continued engagement.   

Cluster 3: Focus on long-term benefits and exclusive rewards that acknowledge their senior status, such as special anniversary offers or enhanced benefits for their travel frequency and distance.   

### 5. Optimize Discount Strategies:   

Across All Clusters: Although discount usage is consistent, ensure that the discount strategies are optimized for each cluster's characteristics. Tailor discounts to align with the clusters’ flight recency, count, and distance to maximize their effectiveness.   

### 6. Monitor and Adjust:   

Regular Analysis: Continuously monitor the performance of loyalty programs and engagement strategies. Adjust based on changes in customer behavior and cluster dynamics to ensure ongoing relevance and effectiveness.   



## Contact

LINKEDIN: https://www.linkedin.com/in/nithesh-goutham-m-0b0514205/   
WEBSITE: https://digital-cv-using-streamlit.onrender.com/   
EMAIL : nitheshgoutham2000@gmail.com   


