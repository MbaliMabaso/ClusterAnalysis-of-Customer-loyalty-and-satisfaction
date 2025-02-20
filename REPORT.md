# Cluster Analysis Report

## Objective
The goal of this analysis was to identify distinct customer segments based on their loyalty and satisfaction levels using K-Means clustering. This segmentation helps to uncover patterns in customer behavior, providing valuable insights for strategic decision-making.

## Methodology
### Data Preprocessing
- **Customer Loyalty**: This variable was already standardized with a mean of 0 and standard deviation of 1. No further transformation was required.
  ![image_url](https://github.com/MbaliMabaso/ClusterAnalysis-of-Customer-loyalty-and-satisfaction/blob/9d822a1d1979f9edb16e7bcb73504192f4897bc1/MeanAndSDofLoyalty.png)
- **Customer Satisfaction**: Standardized using `StandardScaler` to ensure comparability with the loyalty variable.
  ![image_url](https://github.com/MbaliMabaso/ClusterAnalysis-of-Customer-loyalty-and-satisfaction/blob/37c90917655000dcb1b4e80abaa8fac5284d663f/StandardizeSatisfaction.png)


### Clustering Algorithm
1. **K-Means Clustering**:
   - The optimal number of clusters was determined by analyzing the Within-Cluster Sum of Squares (WCSS).
   - The WCSS values for increasing cluster counts was 4 clusters (WCSS = 4.1), indicating that **4 clusters** best fit the data.
     ![image_url](https://github.com/MbaliMabaso/ClusterAnalysis-of-Customer-loyalty-and-satisfaction/blob/d6d7a9ea0aadaf6782fbc2871aa79fe0a05b8b4e/WCSS.png)
2. **Cluster Formation**:
   - K-Means was implemented with `n_clusters=4`.
   - Centroids and cluster labels were computed.

### Visualization
The resulting clusters were visualized using a scatter plot:
- **Axes**:
  - X-axis: Customer Satisfaction
  - Y-axis: Customer Loyalty
- **Colors**:
  - Each cluster is represented by a unique color.
  - Cluster centroids were highlighted to indicate the cluster centers.

### Key Visual Insights
- Four distinct clusters are observed:
  - High loyalty, high satisfaction (e.g., red cluster)
  - Moderate satisfaction with varying loyalty levels (e.g., yellow cluster)
  - Low loyalty, moderate satisfaction (e.g., cyan cluster)
  - Mixed satisfaction and loyalty (e.g., purple cluster)

![Cluster Visualization](CustomerLoyaltyandSatisfactionClusters.png)

## Results
The 4 identified clusters reveal the following patterns:
1. **Cluster 1 (Red)**: Customers with high satisfaction and high loyalty. Likely the most valuable segment for retention.
2. **Cluster 2 (Green)**: Customers who are dissatisfied but still loyal. Engagement strategies could improve loyalty here.
3. **Cluster 3 (Blue)**: Customers who are disloyal and unsatisfied. Focused efforts are needed to understand and address dissatisfaction.
4. **Cluster 4 (Purple)**: High satisfaction low loyalty. Strategies should address specific needs in this segment.

## Recommendations
**Cluster-Specific Strategies**:
- Cluster 1 (Red)**: Customers with high satisfaction and high loyalty. Use information about these customers to try and recruit similar people who haven't heard of
   this company.
- Cluster 2 (Green)**: Customers who are dissatisfied but still loyal. Investigate dissatisfaction and improve satisfaction levels to increase loyalty.
- Cluster 3 (Blue)**: Customers who are disloyal and unsatisfied. Investigate dissatisfaction and improve satisfaction levels.
-  Cluster 4 (Purple)**: High satisfaction low loyalty. Introduce loyalty programs to keep them coming back. For example, rewards and points for buying, special discounts etc.
- 
**Future Analysis**:
- Incorporate demographic and transactional data to refine segmentation.

## Conclusion
This analysis successfully segmented customers into 4 clusters based on loyalty and satisfaction. These insights can inform targeted engagement strategies, improving overall customer experience and business outcomes.

