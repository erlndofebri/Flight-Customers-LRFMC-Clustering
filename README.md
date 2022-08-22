# Flight Customers LRFMC Clustering
The goals of this project are to cluster flight customers and make recommendation how to deal with each cluster Using LRFMC clustering method
## LRFMC
We will analyze flight customer using LRFMC analysis. LRFMC analysis is an extended version of RFM analysis that has been used in the aviation industry for years to divide customers into segments. Based on LRFMC analysis we will need 5 variables:

- L : The number of months since the member’s joining time from the end of the observation time. => LOAD_DATE - FFP_DATE

- R : Number of months since the member’s last flight from the end of observation time. => LAST_TO_END

- F : The total number of times the member has flown during the observation period. => FLIGHT_COUNT

- M : Miles accumulated during member observation time. => SEG_KM_SUM

- C : The average value of the discount factor used by the member during the observation period. => avg_discount

After implementing elbow method, we decided to cluster these customers into 4 clusters. 

## Clustering Analysis LRFMC Summary 

1. Cluster 0

- (L) Length of joining member: Medium member, higher than 2 and 3. it can be considered as old customer

- (R) Recent Flight: Shortest recency between the other cluster, mostly have flight in recent time

- (F) Flight Count: Customer with the highest flight count

- (M) Miles Accumulated: Has the highest sum of flight distance

- (C) Discount used: the difference is not too significant between the other cluster

2. Cluster 1:

- (L) Length of joining member: senior member, highest than other clusters.

- (R) Recent Flight: short recency (similar with cluster 3), mostly have flight in recent time

- (F) Flight Count: Medium flight frequency (similar with cluster 3)

- (M) Miles Accumulated: Has the second highest sum of flight distance (similar with cluster 3)

- (C) Discount used: the difference is not too significant between the other cluster

3. Cluster 2:

- (L) Length of joining member: junior member, higher than cluster 3, but its considered as junior member

- (R) Recent Flight: Haven't flight for the longest time.

- (F) Flight Count: lowest flight frequency

- (M) Miles Accumulated: the lowest miles accumulated flight

- (C) Discount used: the difference is not too significant between the other cluster

4. Cluster 3:

- (L) Length of joining member: junior member, the newest member who regeistered their name as a customers

- (R) Recent Flight: short recency (similar with cluster 1), mostly have flight in recent time

- (F) Flight Count: Medium fligh frequency (similar with cluster 1)

- (M) Miles Accumulated: Has the second highest sum of flight distance (similar with cluster 1)

- (C) Discount used: the difference is not too significant between the other cluster


## Business Recomendation
- Among 4 type of clusters, cluster 3 shows highest unique customer value since it is dominated by newest member who has flight in recent time.
- Suggest discount voucher to be implemented and maximized for cluster 3 since we want to grab this new customers and engage them to become loyal customer by getting more and more flights
- To minimize the risk of losing customers, we have to pay attention to cluster 2 since they haven't flight for the longest time and we need special care using CRM either email promotion or push notification if they install our airline apps. The kind of promotion that might work for cluster 2 might local or domestic vacation since they consider as the lowest miles accumulated.
- Suppose we want to offer loyalty membership, we can refer to this clustering so that it is targeted properly with classification such as Bronze, Silver, Gold and Platinum (based on accumulated airline miles earning by each of customer)


