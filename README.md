# Customer Analytics

* Segmented customers using a combination of Principal Component Analysis (4 components) and K-mean Clustering (4 segments).
* Price Elasticity for Purchase Probability, Brand Choice (own and cross-brand), Purchase Quantity.
* Modeled the elasticities for each price point.

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, scipy  
**Visualizations:** matplotlib, seaborn   
**References:** https://learn.365datascience.com/

## Data Cleaning and Preprocessing
* The data collected was already cleaned.
* I standardized the data using Standard Scaler.

## Segmentation

* Hierarchical clustering and K-means clustering with within-cluster sum squared (WCSS) used for determining the number of clusters.

![Screenshot 2021-05-06 at 5 45 24 PM](https://user-images.githubusercontent.com/39771193/117369432-e7105e80-ae92-11eb-9d11-c09a92311232.png)

![Screenshot 2021-05-06 at 5 45 35 PM](https://user-images.githubusercontent.com/39771193/117369426-e4156e00-ae92-11eb-83bf-4bfd623ae143.png)

* To improve segmentation and reduce the dimensionality, I used *Principal Component Analysis* to cover 90% variance. (4 components)
* The focus of Components:
  1. Component 1 - Career Focused
  2. Component 2 - Education & Lifestyle
  3. Component 3 - Experience
  4. Component 4 - Big City 

* Based on the output, the four segments were named as follows:
  1. Career-Focused
  2. Standard
  3. Well off
  4. Fewer Opportunities

![Screenshot 2021-05-06 at 5 59 04 PM](https://user-images.githubusercontent.com/39771193/117370678-c21ceb00-ae94-11eb-99f8-b423e1988629.png)


## Purchase Analytics 

## Predictive Analytics
