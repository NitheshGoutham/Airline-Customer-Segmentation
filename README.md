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

RFMC analysis consists of 5 aspects:

L : The number of months since the member’s joining time from the end of the observation time. => LOAD_DATE - FFP_DATE
R : Number of months since the member’s last flight from the end of observation time. => LAST_TO_END
F : The total number of times the member has flown during the observation period. => FLIGHT_COUNT
M : Miles accumulated during member observation time. => SEG_KM_SUM
C : The average value of the discount factor used by the member during the observation period. => avg_discount


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

## Analysis    
-> Cluster summary statistic:   


  



## Business Recommendation   




## Contact

LINKEDIN: https://www.linkedin.com/in/nithesh-goutham-m-0b0514205/   
WEBSITE: https://digital-cv-using-streamlit.onrender.com/   
EMAIL : nitheshgoutham2000@gmail.com   


