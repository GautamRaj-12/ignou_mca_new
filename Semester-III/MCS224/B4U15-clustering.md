# Clustering

## Introduction to Clustering

- **Definition**: 
  - Clustering or cluster analysis is a method for dividing a group of data objects into subgroups based on a single observation.
  - Each cluster is a subset of data where objects with resemblance or similar properties are grouped together.
  - Objects in the same cluster are similar to each other but differ from objects in other clusters.

- **Purpose**: 
  - The effort of dividing a population into multiple groups so that data points of one group can be easily compared with data points of another group.
  - To separate groups with identical features and assign them into clusters.

- **Process**:
  - Performed by machines, not humans.
  - Known as unsupervised learning because clustering is a form of learning by observation.

- **Difference from Classification**:
  - Classification involves the separation of data based on class labels.
  - Clustering involves partitioning of large data sets into groups based on similarity.

### Example

- **Scenario**: 
  - Suppose you are the head of a rental store and wish to understand the preferences of your customers to scale up your business.
  - It is not feasible to look at the details of each customer and devise a unique business strategy for each one of them.
  
- **Solution**: 
  - Cluster all customers into groups based on their purchasing habits.
  - Use separate strategies for customers in each of these groups.
  
- **Result**:
  - This method of grouping customers based on their habits is known as clustering.


**“Clustering is the process of dividing the entire data into groups (also known as clusters) based on the patterns in the data.”**

### Applications of Clustering

- **Prominent Technique**: 
  - Data clustering is a prominent technique in data analysis.
  - Applied in various research areas including:
    - Data mining
    - Data statistics
    - Machine learning for analysis

- **Industry Applications**:
  - **Financial Services**: 
    - Used for monitoring credit card fraud and criminal activities (outlier detection).
  - **Health Information Systems**
  - **Web Mining**
  - **Financial Sectors**
  - **Image Recognition**:
    - Finds clusters or patterns in image or text recognition systems.
  - **Web Search**:
    - Helps manage the enormous quantity of online pages by clustering search results for better relevance.

- **Research Significance**:
  - Cluster analysis is a recent area of research in data analysis.
  - Driven by the massive volumes of data produced in databases.

- **Use Case Example**:
  - **Outlier Detection**: 
    - Monitoring credit card fraud and criminal activities.
  - **Image Recognition**: 
    - Finding clusters or patterns in image or text recognition systems.
  - **Web Search**:
    - Keyword search may produce a huge number of hits; clustering helps manage and group relevant pages.

### Real World Example:
A bank can potentially have millions of customers. Would it make sense to look at the details of each customer separately and then decide? Certainly not! It is a manual process and will take a huge amount of time. So, what can the bank do? Clustering comes to the rescue in these situations where the banks can group the customers based on their income: *High Income*, *Average Income*, *Low Income*.

### Applications of Clustering in Real-World Scenarios

Clustering is a widely used technique in the industry. It is being used in almost every domain, ranging from banking to recommendation engines, document clustering to image segmentation.

- **Customer Segmentation**: Customer segmentation is one of the most common applications of clustering. And it isn’t just limited to banking. This strategy is across functions, including telecom, e-commerce, sports, advertising, sales, etc.
- **Document Clustering**: Document Clustering is another common application of clustering. Let’s assume that you have multiple documents, and you need to cluster similar documents together. Clustering helps us group these documents such that similar documents are in the same clusters.
- **Image Segmentation**: We can also use clustering to perform image segmentation. Here, we try to club similar pixels in the image together. We can apply clustering to create clusters having similar pixels in the same group.

## Partition Based Clustering

- **Overview**:
  - Partition algorithm is one of the most applied clustering algorithms.
  - Widely used due to its simple structure and easy implementation compared to other clustering algorithms.

- **Clustering Method**:
  - Classifies information into multiple groups based on characteristics and similarities of the data.
  - When a database (D) contains multiple (N) objects, the partitioning approach divides the data into user-specified (K) partitions.
  - Each partition represents a cluster and a specific region.

- **Partitioning Process**:
  - Data is divided into K groups or partitions.
  - Each group must have at least one object from the existing data.
  - Splits data items into non-overlapping subsets (clusters).
  - Ensures each data object fits perfectly into one of the clusters.

- **Starting Seeds**:
  - Requires a set of starting seeds (or clusters).
  - Enhanced iteratively by transferring objects from one group to another to improve partitioning.

- **Cluster Characteristics**:
  - Objects in the same cluster are "near" or related to one another.
  - Objects in different clusters are "far apart" or significantly distinct.

- **Popular Partitioning Algorithms**:
  - **K-Means**:
    - Commonly used partitioning algorithm.
  - **PAM (K-Medoids)**:
    - Partitioning Around Medoids.
  - **CLARA (Clustering Large Applications)**:
    - Designed for large datasets.

## Hierarchical Based Clustering

Hierarchical Clustering analysis is an algorithm that groups the data points with similar properties and these groups are termed “clusters”. As a result of hierarchical clustering, we get a set of clusters, and these clusters are always different from each other. Clustering of this data into clusters is classified as:

- **Agglomerative Clustering** (involving decomposition of cluster using bottom-up strategy)
- **Divisive Clustering** (involving decomposition of cluster using top-down strategy)

Hierarchical clustering helps in creating clusters in the proper order (or hierarchy). 

**Example**: The most common everyday example we see is how we order our files and folders in our computer by proper hierarchy.

As mentioned, Hierarchical clustering is classified into two types i.e., Agglomerative clustering (AGNES) and Divisive Clustering (DIANA).

### Hierarchical clustering Technique in terms of space and time complexity:
- **Space complexity**: When the number of data points is large, the space required for the Hierarchical Clustering Technique is large since the similarity matrix must be stored in RAM. The space complexity is measured by the order of the square of n. Space complexity = O(n²) where n is the number of data points.
- **Time complexity**: The time complexity is also very high because we have to execute n iterations and update and restore the similarity matrix in each iteration. The order of the cube of n is the time complexity. Time complexity = O(n³) where n is the number of data points.

### Limitations of Hierarchical Clustering Technique:
1. Hierarchical clustering does not have a mathematical goal.
2. All the methodologies applied for calculating the similarity index between clusters does not apply fully in every situation, each technique has its own merits and demerits.
3. Due to high space and time complexity. This clustering algorithm is not applicable for huge data.

## Density Based Clustering Technique

Clusters are formed in the Density Depending Clustering Technique based on the density of the data points represented in the data space. Those locations that become dense as a result of the large amount of data points that reside there are termed as clusters.

### How it works:
1. It starts with a random unvisited starting data point. All points within a distance ‘Epsilon’ – Ɛ classify as neighborhood points.
2. We need a minimum number of points within the neighborhood to start the clustering process. In this scenario, the current point of data turns into the first point in the cluster. Else, the point is regarded as ‘Noise.’ In either case, the current point becomes a visited point.
3. All points within the distance (Ɛ) become part of the same cluster. This process is repeated for all the newly added data points in the cluster group.
4. Continue with the process until you visit and label each point within the ‘noise’ or cluster point.


## Clustering Algorithms

### K-Means
K-means is an iterative clustering algorithm that helps to find the highest value for every iteration. It uses mean as a distance measuring method. It is an unsupervised iterative clustering method. It works in the following steps:

1. Select K value.
2. Initialization of centroids.
3. Assignment of data points to clusters based on distance of centroids.

#### Real World Example:
You might have visited a book store or shopping mall. What are the different ways the store owner is arranging items in the store? 
1. Fiction
2. Non-Fiction
3. Biography
4. Self-Help
5. Children
6. Poetry
This helps the customer to easily search for the required items and purchase them.

### Practice Problem:
Use K-means clustering to cluster the given data points into a specified number of clusters. 

### Agglomerative Clustering
Agglomerative Hierarchical Clustering uses a bottom-up strategy to create a hierarchy of clusters. Initially, each data point is considered as a single cluster and then they are iteratively combined to form larger clusters. The algorithm stops when all points belong to a single cluster.

1. Calculate the proximity matrix for the data points.
2. Assume that each data point forms a cluster.
3. Combine the closest pair of clusters, and update the proximity matrix.
4. Repeat step 3 until all points are in a single cluster.

### Divisive Clustering (DIANA)
Divisive Hierarchical Clustering uses a top-down approach. It begins with the whole dataset and splits it into smaller clusters. The algorithm continues to split the clusters until each data point is in its own cluster.

### DBSCAN
DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is a density-based clustering algorithm that can discover clusters of different shapes and sizes from a large amount of data, which is noisy and contains outliers.

1. It starts with an arbitrary point that has not been visited.
2. This point's epsilon-neighborhood is retrieved, and if it contains sufficiently many points, a cluster is started.
3. Otherwise, the point is labeled as noise. If a point is found to be a dense part of a cluster, its epsilon-neighborhood is also part of that cluster.
4. This process continues until all points have been visited.


## Check Your Progress - 1
1. What do you understand by the term “Clustering”?
2. Where is Clustering used in present day scenario?
   
## Check Your Progress - 2
1. Briefly explain how Partition Based Clustering works.
2. Name three Partition Based Clustering methods.

## Check Your Progress - 3
1. Differentiate between Hierarchical Clustering and Partition Based Clustering.
2. What are sub-types of Hierarchical Clustering and what is the difference between them?
3. What is the space and time complexity of Hierarchical clustering?
4. List some of the limitations of Hierarchical clustering.

### Check Your Progress - 4
1. What do you understand by the term “Density Based Clustering”?
2. How is “Density Based Clustering” performed?
