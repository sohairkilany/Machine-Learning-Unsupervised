## **Unsupervised Learning, Clustering Algorithms**

  ## Goal:
       Finding structure (pattern) within the data, usually by dividing it into cluster (collection of data objects).
       
  ## Here is my implementation.
  
  ## 1- K-Means
        1-1 implement K-Means from scratch.
        1-2 implement K-Means from sklearn.
            1-2-1 Evaluating a clustering.
            1-2-2 How many clusters of grain? (using elbow draw figure between number of clustering and interia)
            1-2-3 Using pipeline to apply StandardScaler then KMeans. 
        1-3 Image Compression with K-means.


 ## 2- Agglomerative clustering (Hierarchical_Clustering).
        Agglomerative clustering is a general family of clustering algorithms that build nested clusters by merging data points successively. This hierarchy of clusters can be represented as a tree diagram known as dendrogram.The top of the tree is a single cluster with all data points while the bottom contains individual points.

       2-1 yielding a tree visualization of the resulting cluster hierarchy.
       2-2 Use Different linkage (Single linkage, Complete or Maximum linkage, Average linkage, centroid linkage).
       2-3 measure performance by Silhouette_Score.


 ## 3- Implement PCA 
      Benefits of using PCA,
          •	It compresses the data and thus reduces the storage space requirements.
          •	It reduces the time required for computation since less dimensions require less computation.
          •	It eliminates the redundant features.
          •	It improves the model performance.

         used countries of the world dataset, select 11 features from 18 columns, carry 95% information about data.

## 4- DBSCAN 
    DBSCAN groups together points that are closely packed together while marking others as outliers which lie alone in low-density regions.
    There are two key parameters in the model needed to define 'density': minimum number of points required to form a dense region (min_samples) 
       and distance to define a neighborhood (eps).

     DBSCAN classify point as Core point or Border point or Noise point.

      1- Core Point: If the number of points in the neighbourhood is at least equal to the min_samples parameter then it 
           called a core point and a cluster is formed around x.
      2- Border Point: x is considered a border point if it is part of a cluster with a different core point but number of points 
          in it’s neighbourhood is less than the min_samples parameter. Intuitively, these points are on the fringes of a cluster.
      3- Noise Point: If x is not a core point and distance from any core sample is at least equal to or greater thaneps, 
          it is considered an outlier or noise.

   For tuning the parameters of the model, 
       1- determine the number of minimium points, then use the 
           NearestNeighbours function to get the minimum distance.
       2- Draw elbow curve to find density of the data points and optimal eps 
            value can be found at the inflection point.

       
    
