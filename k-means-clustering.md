# K-Means Clustering

The idea behind clustering data is pretty simple: partition a dataset into groups of similar data observations. How we go about finding these clusters is a bit more complex since there are a number of different methods for clustering datasets.

The most well-known clustering method is [K-means clustering](https://en.wikipedia.org/wiki/K-means\_clustering). The K-means clustering algorithm will separate the data into K clusters (the number of clusters is chosen by the user) using cluster means, also known as centroids.

![The Algo behind K-Means Clustering](<.gitbook/assets/image (12).png>)

&#x20;The K-means clustering algorithm is an iterative process. Each iteration, the algorithm will assign each data observation to the cluster with the closest centroid to the observation (using the regular [distance](http://mathworld.wolfram.com/Distance.html) metric).

![](<.gitbook/assets/image (13).png>)

### Elbow Method to Determine best K&#x20;

Head over This [Link](https://www.kaggle.com/arishalam/the-knn-algorithm), a very good introduction to KNN and scratch implementation of that.&#x20;

![The Elbow method for best K ](<.gitbook/assets/image (14).png>)

Click [Here](https://www.analyticsvidhya.com/blog/2017/09/30-questions-test-k-nearest-neighbors-algorithm/?utm\_source=facebook.com\&utm\_medium=social\&fbclid=IwAR0JgeXKfyLGndL2\_eMX7R6HLVY9la97V6QMIYb\_4LnG56N-x1Oe5DsdhqE) for MCQ Interview Questions for KNN.

### Advantages

1. Used in Unsupervised Learning, for recommendation Engines(Collaborative Filtering).
2. When you have no info about the data you can draw inferences from this type of algorithm.
3. Visulizable and intuitive algorithm.&#x20;
4. Used in Image segmentation, spam detection, and color quantization.

### Disadvantages

1. Outliers can distort the centroids.&#x20;
2. It says nothing about the contribution of different clusters, no percentage indication about being in a cluster.&#x20;
3. Random Initialization might cause some problems in the K-Means Algorithm therefore a smart initialization technique was developed called kmeans++.
