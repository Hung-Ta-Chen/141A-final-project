
##Clustering
#3.1Agglomerative Hierarchical Clustering
3.1.1 General introduction to Hierarchical Clustering
Hierarchical clustering is an unsupervised clustering algorithm used to create clusters with a tree-like hierarchy. In this clustering method, there is no need to give the number of clusters to the algorithm.  In contrast to this, the other algorithm like K-Mean produces flat clusters where there is no hierarchy and we also have to choose the number of clusters, to begin with.

Here, we first draw a Hierarchical Dendrogram to have a general overview of the ufc data to decide the number of clusters we need for the K-Mean clustering algorithm.

The hierarchical clustering algorithm can be of two types –
Divisive Clustering – It takes a top-down approach where the entire data observation is considered to be one big cluster at the start. Then subsequently it is split into two clusters, then three clusters, and so on until each data ends up as a separate cluster.
Agglomerative Clustering – It takes a bottom-up approach where it assumes individual data observation to be one cluster at the start. Then it starts merging the data points into clusters till it creates one final cluster at the end with all data points.



3.1.2 Method
Parameters of Agglomerative Clustering
The agglomeration hierarchical clustering can have multiple variations depending on affinity and linkage.
Affinity
Affinity denotes the method using which the distance or similarity between data points or clusters is calculated. Which include –

Euclidean-straight line distance between 2 data points in a plane:
Manhattan-distance between two strings, a and b is denoted as d(a,b).
Cosine-Cos θ distance between the two data points
The equation is:
$$\left( \sum_{i=1}^{n}|x_{i}-y_{i}|^{p} \right)^{\frac{1}{p}}$$
Where: 
p = 1, Manhattan Distance
p = 2, Euclidean Distance
p = infinity, Chebychev Distance

Linkage
The clusters are formed by using different types of criteria or known as linkage functions. Linkage methods use the affinity that we discussed above.

The different linkage methods produce different results of hierarchical clustering, they are listed below :

Single-merge in each step the two clusters whose two closest members have the smallest distance 
Complete-merge in each step the two clusters whose merger has the smallest diameter
Average-compromise between the sensitivity of complete-link clustering to outliers and the tendency of single-link clustering to form long chains that do not correspond to the intuitive notion of clusters as compact, spherical object
Wards-increase in the "error sum of squares" (ESS) after fusing two clusters into a single cluster
Error Sum of Squares: $$ESS=\sum_{i}^{}\sum_{j}^{}\sum_{k}^{}|x_{ijk}-\bar{x}_{i\cdot k}|^{2}$$

3.1.3 Application
In this case we are interested in the fighter style of each boxer. So we use these four variables as our input, we generate a Hierarchical Dendrogram which is show below:

In the above dendrogram graph, such a vertical line. We now draw a horizontal line across this vertical line as shown below. This horizontal line cuts the vertical line at two places, and this means the optimal number of clusters is 4.

We are then able to run the AgglomerativeClustering module of sklearn.cluster package to create flat clusters by passing no. of clusters as 4 (determined in the above section). Again we use euclidean and ward as the parameters.

By the cluster method stated as above , we are able to obtain the four clusters from the Agglomerative Clustering as below:

3.1.4 Interpretation:
From the above Clusters we are able to identify few thing:
	1.
K-nearest neighbor (KNN) 
K-nearest neighbor (KNN) is a non-parametric classifier. The prediction of the label of a test point is assigned according to the vote of its K nearest neighbors’ labels, where K is a user-defined parameter. KNN is a simple technique, and could work well when given a good distance metric and sufficient training dataset. It can be shown that the KNN classifier can come within a factor of 2 of the best possible performance if N → ∞ . For a test point x, the probability that its class label y=c is defined as

$$p\left( y=c|x,D,K \right)=\frac{1}{K}\sum_{_{i\in }N_{k}\left( x,D \right)}^{}\left( y_{i} \right) = c_{i}$$

Where $N_{k}\left( x,D \right)$ are the K nearest neighbors of the test point. The estimate class label would then be defined as $\hat{y}\left( x \right)=argmax_{c}p(y=c|x,D,K)$

## 3.2 Principal component analysis (PCA)

Principal component analysis (PCA) is a popular technique for analyzing large datasets containing a high number of dimensions/features per observation, increasing the interpretability of data while preserving the maximum amount of information, and enabling the visualization of multidimensional data. Formally, PCA is a statistical technique for reducing the dimensionality of a dataset. This is accomplished by linearly transforming the data into a new coordinate system where (most of) the variation in the data can be described with fewer dimensions than the initial data.

The principal components of a collection of points in a real coordinate space are a sequence of p unit vectors, where the i-th vector is the direction of a line that best fits the data while being orthogonal to the first i-1 vectors. Here, a best-fitting line is defined as one that minimizes the average squared perpendicular distance from the points to the line. These directions constitute an orthonormal basis in which different individual dimensions of the data are linearly uncorrelated. Principal component analysis (PCA) is the process of computing the principal components and using them to perform a change of basis on the data

$$ w_{(1)} =\arg\max_{\Vert w \Vert = 1} \,\left\{\sum_i(t_1)^2_{(i)}\right\}= \arg\max_{\Vert w \Vert = 1} \,\left\{ \sum_i \left(x_{(i)} \cdot w \right)^2 \right\}$$

The k-th component can be found by subtracting the first k − 1 principal components from X:
$$\hat{\textbf{X}_{k}} = \textbf{X}-\sum_{s=1}^{k-1}\textbf{X}\textbf{w}_{\left( s \right)}\textbf{w}^{^{\textbf{T}}}_{\left( s \right)}$$
