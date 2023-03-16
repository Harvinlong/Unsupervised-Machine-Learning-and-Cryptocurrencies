# Unsupervised-Machine-Learning-and-Cryptocurrencies

## The purpose of the project:
The purpose of this project was to create a report for our client, who was interested in offering a new cryptocurrency investment portfolio for its customers. The goal was to analyze the cryptocurrency market and create a classification system to aid in their investment decisions. The task was to process data, use unsupervised learning techniques to cluster the cryptocurrencies, and create data visualizations to share our findings with the board. Applying the knowledge of unsupervised learning, data processing, clustering, and dimensionality reduction using PCA to provide our clients with actionable insights for their new investment portfolios.

## Step 1: Preprocessing the Data for PCA 
1. Preprocessing the cryptocurrency data for use in a clustering algorithm.

2. Reading through a CSV file containing cryptocurrency data into a Pandas DataFrame, filtering the DataFrame to only include actively traded cryptocurrencies with no null values, and removing unnecessary columns. 

3. The text features Algorithm and ProofType are converted into binary variables using the get_dummies() method and the resulting DataFrame is standardized using the StandardScaler fit_transform() function.

![data-18-challenge-crypto-df-DataFrame-shows-four-columns](https://user-images.githubusercontent.com/111480084/225489033-9ed73c71-754d-4780-b4ec-68d721e596f0.png)

## Step 2: Reducing Data Dimensions Using PCA and Clustering Cryptocurrencies Using K-means
This step is to analyze a cryptocurrency dataset using the K-means clustering algorithm. 

First read through the dataset to a Pandas DataFrame, filtering and cleaning the data, reducing the dataset to three dimensions. 

Then create an elbow curve to find the optimal number of clusters, and run the K-means algorithm to make predictions of the K clusters for the cryptocurrencies’ data.

After that, concatenate the necessary DataFrames, and add columns for the names of the cryptocurrencies and the predicted cluster labels. Finally, the results are visualized using hvPlot.

![data-18-challenge-dataframe-clustered-df-visualizing-results](https://user-images.githubusercontent.com/111480084/225489670-6e63ca11-58df-4caa-a8b6-04b91b65786a.png)

## Step 3: Visualizing Cryptocurrencies Data
Create a table with tradable cryptocurrencies using the hvplot.table() function and print the total number of tradable cryptocurrencies in the DataFrame.
![data-18-challenge-hvplot-table-showing-all-tradable-cryptocurrencies](https://user-images.githubusercontent.com/111480084/225490402-3179fe91-8cbf-4a9f-b276-e9698ec751c1.png)

Scale the TotalCoinSupply and TotalCoinsMined columns between the given range of zero and one using the MinMaxScaler().fit_transform method.

Create an hvplot scatter plot with x="TotalCoinsMined", y="TotalCoinSupply", and by="Class", and have it show the CoinName when you hover over the data point.
![data-18-challenge-hvplot-scatter-plot](https://user-images.githubusercontent.com/111480084/225490409-2d035582-c487-4e66-a681-9b8bac6eb36b.png)
