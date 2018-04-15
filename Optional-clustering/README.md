Optional-Clustering
===========

Descriptions
-------
First we merged the given train.csv and test.csv to get full data set, then we cluster this set of full data (not using the labels), with Mini Batch K-Means Clustering. As the ground truth is known here, we also apply different cluster quality metrics to judge the goodness of fit of the cluster labels to the ground truth. Specifically, homogeneity score, completeness score and V-measure are applied here.

Methods
-------
* **Mini Batch K-Means Clustering**  
Same as the K-means clustering, the Mini Batch K-Means Clustering also aims to choose centroids that minimise the within-cluster sum of squared criterion, but it uses mini-batches to reduce the computation time. Mini-batches are subsets of the input data, randomly sampled in each training iteration. These mini-batches drastically reduce the amount of computation required to converge to a local solution. In contrast to other algorithms that reduce the convergence time of k-means, mini-batch k-means produces results that are generally only slightly worse than the standard algorithm.
 
* **Homogeneity Score, Completeness Score and V-Measure**  
A clustering result satisfies homogeneity if all of its clusters contain only data points which are members of a single class. A clustering result satisfies completeness if all the data points that are members of a given class are elements of the same cluster. The V-measure is the harmonic mean between homogeneity and completeness:  
`v = 2 * (homogeneity * completeness) / (homogeneity + completeness)`  
These scores range from 0 to 1 with perfect labelings having score 1.0.

Difficulties
-------
As shown in the output, the scores we used to measure the accuracy of clustering are around 0.38, which is not so satisfactory. In mini batch k-means clustering, the within-cluster sum of squared criterion (inertia) we use is not a normalized metric: we just know that lower values are better and zero is optimal. But in very high-dimensional spaces (like the data space in our example), Euclidean distances tend to become inflated (this is an instance of the so-called “curse of dimensionality”). Running a dimensionality reduction algorithm such as PCA (we will do this in milestone 3) prior to mini batch k-means clustering can alleviate this problem and speed up the computations.

Resources
-------
The resources we used are: 
* Python 3 
* pandas package 
* numpy package 
* sklearn package 
* Scikit-learn

Files
-------
* "Mini Batch K-Means Clustering.ipynb" is for importing data, running and evaluating mini batch k-means clustering on the full dataset.

Each file is a markdown file that includes both code and result. The code included is intended to be run in Python 3
