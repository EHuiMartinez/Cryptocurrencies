# Cryptocurrencies

## Overview of the analysis: 
This analysis uses a cryptocurrency dataset from ![CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist) and applied data preprocessing methods before running through the data using unsupervised machine learning methods.  In Python, we used scikit-learn libraries such as Principal Component Analysis (PCA) and KMeans with Elbow Curve to create predictions, then graph with 2D and 3D scatter plots using hvplot.


## Results: 
There are 4 deliverables required for the analysis of the cryptocurrency data.  
Note: Only some images are displayed here; see crypto_clustering.ipynb file for additional details.

### Deliverable 1

1. Six data preprocessing steps were performed on the cryptocurrency data, including:
    * crytocurrencies not traded were removed
    * crytocurrencies without defined algorithms were removed
    * dropped IsTrading column
    * removed all rows that have at least one null value
    * removed all rows that do not have coins being mined
    * dropped CoinName column

2. A new datagrae is created and further transformed by converting variables from text to numbers using get_dummies() method.
3. Features were standardized using StandardScaler()


### Deliverable 2

1. The PCA algorithm was used to reduce the dimensions of the crypto_df DataFrame down to three principal components.
2. The pcs_df DataFrame was created and has PC 1, PC 2, and PC 3 columns with the index from the crypto_df DataFrame.

![Deliverable2_PCA.png](/Resources/Deliverable2_PCA.png)

### Deliverable 3
The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
1. An elbow curve is created using hvPlot to find the best value for K.
2. Predictions are made on the K clusters of the cryptocurrencies’ data.
3. A new DataFrame is created with the same index as the crypto_df DataFrame and includes the Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName and Class columns.

![Deliverable3_Kmeans_ElbowCurve.png](/Resources/Deliverable3_Kmeans_ElbowCurve.png)


### Deliverable 4
1. The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover.

![Deliverable4_3D_scatter_clusters.png](/Resources/Deliverable4_3D_scatter_clusters.png)

2. A table with tradable cryptocurrencies is created using the hvplot.table() function.  The total number of tradable cryptocurrencies is printed.

![Deliverable4_HvplotTable.png](/Resources/Deliverable4_HvplotTable.png)

3. A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns.

4. A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class".  It shows the CoinName when you hover over the data point.

![Deliverable4_2D_Scatter_cluster.png](/Resources/Deliverable4_2D_Scatter_cluster.png)


## Summary:

Unsupervised ML methods can be used when there is no specific target for prediction.  It allows the data to speak for itself when clusters or patterns develop from the dataset.  However, data preprocessing, such as selecting the relevant data, eliminating missing values, reducing dimensions or values and transforming to usable format are key.  

In "unsupervised" ML, only a "good" dataset will behave well. ;P