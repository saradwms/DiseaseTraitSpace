# Code for the hierarchical clustering approach used to determine susceptibility group identity and Random Forest Analysis to determine most influential traits in cluster identification.

## Methods:

We used a Gower dissimilarity matrix that allows for mixed variables and variable weights when determining similarity of samples based on traits. The dissimilarity matrix is then used in the clustering step. Clustering was done using the function hclust() with Ward’s minimum variance method of hierarchical clustering. In the resultant dendrogram, the height of the fusion provided on the vertical axis indicates the (dis)similarity between two observations. The higher the height of the fusion, the less similar the observations. We identify clusters by cutting the tree, so the height of the cut is indicative of similarity within the cluster. There is no universal method for determining the best number of clusters from a dendrogram.

We used random forest analyses to determine what traits most influence the cluster structure. Random forest analysis is a machine based learning method that estimates variable importance by combining many classification trees through bootstrap sampling and model averaging. We ran 2000 iterations of a random forest analysis that computed the increase in cluster mis-classification rate for each trait when it was excluded and all other traits held constant. Traits that resulted in high mis-class rates were determined to be the most important traits.

## Data Files used
Traits by replicate: traits_loggenes_env.csv
 
 Please contact me if you need access to the files. 