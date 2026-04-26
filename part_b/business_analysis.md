# Business Analysis - Part B

## Overview

This section of the analysis focuses on examining the customer dataset along with the retail promotions dataset. The main goal is to group customers using unsupervised learning techniques and assess how effective different promotions are based on the number of items sold. These findings help guide decisions related to targeted marketing and promotional planning.

## Customer Segmentation (KMeans Clustering)

KMeans clustering was applied to the customer dataset using these features: age, annual spend, monthly visits, basket size, days since the last visit, and number of product categories purchased. A total of three clusters were defined.

### Cluster Summary

-    **Cluster 0**: 170 customers; average attributes:
    - age = 24.68, annual_spend = 14847.37, visits_per_month = 14.34, basket_size = 558.97, days_since_last_visit = 9.08, num_categories_purchased = 2.11

- **Cluster 1**: 165 customers; average attributes:
    - age = 56.77, annual_spend = 89413.33, visits_per_month = 2.53, basket_size = 5530.55, days_since_last_visit = 105.36, num_categories_purchased = 7.52

- **Cluster 2**: 165 customers; average attributes:
    - age = 40.39, annual_spend = 43340.73, visits_per_month = 8.19, basket_size = 2021.68, days_since_last_visit = 35.19, num_categories_purchased = 4.42
  

## Promotion Effectiveness Analysis

We analyzed how many items were sold under various promotion types, comparing weekends versus weekdays, festival periods versus regular days, and different store sizes. The tables below present the mean, median, and count of items sold.

### Promotion Type

  promotion_type   mean     median   count
  ---------------- -------- -------- -------
  bogo             293.42   293.5    260
  category_offer   256.33   251.5    218
  flat_discount    282.85   281.5    304
  free_gift        269.07   268.0    216
  loyalty_points   251.51   254.0    202

### Weekend (0 = Weekday, 1 = Weekend)

  is_weekend   mean     median   count
  ------------ -------- -------- -------
  0.0          260.77   260.0    863.0
  1.0          302.77   297.0    337.0

### Festival (0 = No, 1 = Yes)

  is_festival   mean     median   count
  ------------- -------- -------- --------
  0.0           263.26   264.0    1061.0
  1.0           343.58   342.0    139.0

### Store Size

  store_size   mean     median   count
  ------------ -------- -------- -------
  large        313.51   307.0    300
  medium       276.67   271.0    539
  small        232.41   233.0    361

## Business Recommendations

-   **Customer Segments:** Adjust marketing strategies for each cluster:

    -   Cluster 0: Younger customers who spend less but visit often; focus on loyalty-based rewards.

    -   Cluster 1: Older customers with high spending but fewer visits; prioritize retention strategies.

    -   Cluster 2: Middle-aged customers with moderate spending and visit frequency; target with customized promotions.

-   **Promotions:**

    -   The **bogo** promotion achieved the highest average sales; expanding its use could be beneficial.

    -   Sales tend to increase on weekends and during festivals; plan promotions accordingly.

    -   Larger stores generate higher average sales; manage inventory based on store size.

    -   Future analysis could include factors like customer demographics, market competition, and interactions between datasets.
