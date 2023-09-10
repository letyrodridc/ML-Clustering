## Machine Learning Practices - Leticia L. Rodriguez - August 2023

# Clustering Methods

## KMeans

Try to separate in K groups of equal variance. Requires the number of clusters.
First select randoms K centroids and then move the centroids minimizing the inertia or within-cluster 
sum-of-squares-criterion

_Inertia is not a normalized metric: we just know that lower values are better and zero is optimal. But in very high-dimensional spaces, Euclidean distances tend to become inflated (this is an instance of the so-called “curse of dimensionality”). Running a dimensionality reduction algorithm such as Principal component analysis (PCA) prior to k-means clustering can alleviate this problem and speed up the computations._

Kmeans is also referred as Lloyd's algorithm . It's equivalent to the expectation-maximitazion algorithm with a small, all-equal, diagonal covariance-matrix.

_This is highly dependent on the initialization of the centroids. As a result, the computation is often done several times, with different initializations of the centroids. One method to help address this issue is the k-means++ initialization scheme, which has been implemented in scikit-learn (use the init='k-means++' parameter). This initializes the centroids to be (generally) distant from each other, leading to probably better results than random initialization, as shown in the reference._

Pros:
Can be used in large datasets

### Additional Resources
Sklearn - K-means
https://scikit-learn.org/stable/modules/clustering.html#k-means

## Affinity Propagation

### Description

The algorithm creates the clusters by sending messages between pair of samples until it converges. It chooses the cluster numbers from the data provided.

Cons:
It has a high algorithm complexity O(N^2T) where N is the number of samples and T the number of iterations until convergence
Memory complexity is also high around O(N^2)

It's more appropriate for small datasets.

### Additional Resources
Sklearn AffinityPropagation class 
https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AffinityPropagation.html

Sklearn Affinity Propagation description
https://scikit-learn.org/stable/modules/clustering.html#affinity-propagation


## Resources
https://machinelearningmastery.com/clustering-algorithms-with-python/
