# Customer Analytics

* Data fragmented into 4 Segments using a combination of **Principal Component Analysis** (4 Components) and **K-Means Clustering**.
  1. Career-focused - Young group of high-income and well-qualified people.
  2. Well-off - Mid-Age wealthy group in a big city.
  3. Standard - Average Population. (Middle Class)
  4. Few opportunities - Customers from small cities with mediocre income and not highly qualified.   
* A Descriptive Analysis of the Number of purchases, Brand choice, and Revenue generated per segment.
* Price Elasticities (Modeled the elasticities for each price point starting 0.5 to 3.5, for 300 values.)
  * Purchase Probability - 
    * Customers from Well-off & Career-Focused segments are less elastic.
    * Customers are less sensitive to price changes when there are promotions.
    * Beneficial to have a higher original price and constant promotions.
  * Brand Choice Probability (cross-brand) - 
    * Brand 5 can reduce its price by 1% to gain its market share from Well-off segments.
    * Career-Focused Segment are loyal customers of Brand 5.
    * Brand 1 has to reduce its price by 2% to gain some market share from Brand 2 in the Standard and Few Opportunities Segments.
* Building black-box algorithms to improve prediction accuracy to 90% **Future Work**

## Resources
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, scipy  
**Visualizations:** matplotlib, seaborn   
**Techiques:** Linear Regression, Logistic Regression, K-Means Clustering, Principal Component Analysis
**References:** https://learn.365datascience.com/

## Data Cleaning and Preprocessing
* The data collected was already cleaned.
* Standardized the data using Standard Scaler.

## Segmentation

* Hierarchical clustering and K-means clustering with within-cluster sum squared (WCSS) used for determining the number of clusters.

![Screenshot 2021-05-08 at 10 29 18 PM](https://user-images.githubusercontent.com/39771193/117558610-e4f1ff80-b04c-11eb-8785-09c1dadcfacd.png)

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


## Descriptive Analysis 

* Purchases per segment

![Screenshot 2021-05-06 at 6 46 37 PM](https://user-images.githubusercontent.com/39771193/117374574-66a22b80-ae9b-11eb-8f50-196356992ae9.png)

* Brand choice by segment

![Screenshot 2021-05-06 at 6 44 49 PM](https://user-images.githubusercontent.com/39771193/117374447-2642ad80-ae9b-11eb-8642-2d6fb74d8481.png)

* Revenue per segment

|       Segment       | Rev_Brand_1 | Rev_Brand_2 | Rev_Brand_3 | Rev_Brand_4 | Rev_Brand_5 | Total_Revenue | Seg_proportions |
|:-------------------:|:-----------:|:-----------:|:-----------:|:-----------:|:-----------:|:-------------:|:---------------:|
|    Career-Focused   |    705.96   |   1151.70   |    650.32   |   2301.70   |   20251.43  |    25061.11   |      0.212      |
|       Standard      |   2490.83   |   4140.54   |   3909.17   |    628.74   |   1479.29   |    12648.57   |      0.186      |
|       Well-off      |    699.47   |   1298.23   |    731.35   |   14185.57  |   5509.69   |    22424.31   |      0.196      |
| Fewer Opportunities |   2409.39   |   15177.84  |    730.68   |   1924.09   |   2380.59   |    22622.59   |      0.406      |

Insights:
  1. Career-focused segment generates the most revenue, majority from brand 5
  2. Standard segment spend their money on lower-end brands 1,2,3
  3. Well-off customers are hooked on brand 4 and somewhat to brand 5
  4. The last segment customers spend most of their money on Brand 2

## Predictive Analytics

### Purchase Probability

* Price points at which customers behaviour change from inelastic to elastic:
    1. Mean Elasticity = 1.25
    2. Career-Focused = 1.42
    3. Standard = 1.21
    4. Well-off = 1.46
    5. Few-Opportunites = 1.26
   
![Screenshot 2021-05-06 at 9 27 55 PM](https://user-images.githubusercontent.com/39771193/117384881-ee933000-aeb1-11eb-9160-caa20cbfe295.png)

* Price points at which customers behaviour change from inelastic to elastic
  1. No Promotion = 1.27
  2. Promotion = 1.46

### Brand Choice Probability

![Screenshot 2021-05-08 at 9 52 36 AM](https://user-images.githubusercontent.com/39771193/117541727-34034a80-afe3-11eb-94cf-c6ad51337ccc.png)

![Screenshot 2021-05-08 at 9 52 50 AM](https://user-images.githubusercontent.com/39771193/117541731-382f6800-afe3-11eb-89ec-eb2e9b8c6191.png)


### Purchase Quantity

* No concrete findings in purchase behaviour for customers.
* Might narrow is down to per brand/per segment for accurate behaviour of purchase quantity.
