# K_mean-Clustering
project assigned to work on as part of the course 

Clustering is a type of Unsupervised Machine learning i.e. it needs no training data, it performs the computation on the actual dataset. This should be apparent from the fact that in K Means, we are just trying to group similar data points into clusters, there is no prediction involved. K-means clustering aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean, serving as a prototype of the cluster.

Basic K-Means Algorithm:
K-Means algorithm works as follows, assuming we have inputs x1, x2, x3, ..., xn and value of K

▪ Step 0 – Extract/Load data set.
Given data is in .mat file. Extracting that data to numpy array.

▪ Step 1 - Pick K random points as cluster centres called centroids.
Two different Strategies are used while selecting centroids:

1. Selecting all the centroids randomly: We randomly pick K cluster centres(centroids). Let’s assume these are c1, c2..., ck, and we can say that;
      C = {c1, c2..., ck}
      C is the list of all centroids.

2. Choosing the point furthest from the previous centres: pick the first centre randomly; for the i-th centre (i>1), choose a       sample (among all possible samples) such that the average distance of this chosen one to all previous (i-1) centres is maximal.

▪ Step 2 - Assign each Xi to nearest cluster by calculating its distance to each centroid.
In this step we assign each input value to closest centre. This is done by calculating Euclidean(L2) distance between the point and each centroid. arg𝑚𝑖𝑛𝐶𝑖𝜖𝐶𝑑𝑖𝑠𝑡(𝐶𝑖,𝑋)
Where dist(.)is the Euclidean distance.

▪ Step 3 - Find new cluster centre by taking the average of the assigned points.
In this step, we find the new centroid by taking the average of all the points assigned to that cluster. 𝐶𝑖=1|𝑆𝑖|Σ𝑋𝑖𝑋𝑖𝜖𝑆𝑖
Si is the set of all points assigned to the ith cluster.

▪ Step 4 - Repeat Step 2 and 3 until none of the cluster assignments change.
In this step, we repeat step 2 and 3 until none of the cluster assignments change. That means until our clusters remain stable, we repeat the algorithm.

Then We Calculated Objective Function Value and plotted it against the number of clusters.
