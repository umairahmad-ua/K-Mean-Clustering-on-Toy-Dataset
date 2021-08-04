# K-Mean-Clustering-on-Toy-Dataset
This project has been given a Toy data set of items, with features of City, Gender, Age,  Income and Illness. We categorize those items into groups. For that we use the KMeans  algorithm and categorize the items into k groups of similarity by calculating Euclidean distance  as measurement.
 
 # Selection of Cluster Numbers
 
 The basic goal behind k-means consists of defining k clusters such that total within-cluster 
variation (or error) is minimum. A cluster center is the representative of its cluster. The squared 
distance between each point and its cluster center is the required variation. The aim of k-means 
clustering is to find these k clusters and their centers while reducing the total error.

So for this dataset and problem we calculate all the possibilities on train and test by selecting 
the value of K between 2-9. For selection of best k value, we follow two approaches first is 
silhouette score mention below and second is Elbow criterion. Here is the Elbow Evaluation, The best value of K for this dataset is 5. 

#  Evaluation matrix

For this problem we use the silhouette score as the evaluation matrix as we don’t have any 
labels. The best value is 1 and the worst value is -1. Values near 0 indicate overlapping 
clusters. Negative values generally indicate that a sample has been assigned to the wrong 
cluster, as a different cluster is more similar.
As we can see through silhouette score the best cluster or the value of k is 5.

#   Model Improvement
As we can see in the dataset there is irrelevant feature or noncontributing feature name 
“Numbers” we need to drop this for better results all after label encoding all the feature values 
are less than 100 but the values of income are in thousands so we need to scale the data. 
After applying these changes, we will get the value of k=4 and the elbow are here below

In the notebook we will see the impact if ignore the scaling so this is how our clusters may look.

After these observing these examples we will suggest some implementation that can be made 
KMean more efficient

 Remove irrelevant Column like “Numbers”

 Scale the features

 Try to fit on few instances after getting desired results then trained to all the data

 You can apply KMean++ for solving the problem of local minima by selecting the best 
centroids

