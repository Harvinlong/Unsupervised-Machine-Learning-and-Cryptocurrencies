# Unsupervised Machine Learning and Cryptocurrencies

## Project Overview
This project applies **unsupervised machine learning** to analyze the cryptocurrency market, classify different cryptocurrencies, and generate insights to support investment decisions. Unlike **supervised learning**, where models learn from labeled data, **unsupervised learning** identifies patterns in **unlabeled data**, extracting features and structures without predefined categories. This method is particularly useful when we **don't know the exact question to ask** the data.

The project consists of four key tasks:
- **Data preprocessing** to clean and prepare cryptocurrency data for analysis.
- **Dimensionality reduction using Principal Component Analysis (PCA)**.
- **Clustering cryptocurrencies using K-means** to identify distinct groups.
- **Data visualization** to present the results in an interpretable manner.

This analysis provides **a classification system for a client** interested in launching a new cryptocurrency investment portfolio.

## Step 1: Data Preprocessing for PCA
![data-18-challenge-crypto-df-DataFrame-shows-four-columns](https://user-images.githubusercontent.com/111480084/225489033-9ed73c71-754d-4780-b4ec-68d721e596f0.png)
To ensure high-quality input for clustering algorithms, the cryptocurrency dataset undergoes preprocessing:
- **Data Cleaning**: 
  - Load the cryptocurrency dataset into a **Pandas DataFrame**.
  - Filter out cryptocurrencies that are no longer actively traded.
  - Remove unnecessary columns and ensure there are no missing values.
- **Feature Engineering**:
  - Convert categorical features (**Algorithm, ProofType**) into numerical binary variables using **`get_dummies()`**.
  - Standardize numerical features using **`StandardScaler().fit_transform()`** to normalize data for clustering.

## Step 2: Dimensionality Reduction and Clustering
![data-18-challenge-dataframe-clustered-df-visualizing-results](https://user-images.githubusercontent.com/111480084/225489670-6e63ca11-58df-4caa-a8b6-04b91b65786a.png)
### **Principal Component Analysis (PCA) for Dimensionality Reduction**
- Reduce the dataset from **multiple dimensions to three principal components** while retaining significant variance.
- This step simplifies the clustering process and improves visualization.

### **K-Means Clustering**
- Create an **elbow curve** to determine the optimal number of clusters.
- Apply **K-means clustering** to group cryptocurrencies into distinct categories.
- Append cluster labels to the dataset to facilitate further analysis.
- A **3D scatter plot** (`scatter_3d() in Plotly Express`) is created to visualize the three clusters from the clustered dataset.

## Step 3: Data Visualization
![data-18-challenge-hvplot-table-showing-all-tradable-cryptocurrencies](https://user-images.githubusercontent.com/111480084/225490402-3179fe91-8cbf-4a9f-b276-e9698ec751c1.png)
To better interpret the clustering results, multiple visualizations are generated:
- **Cryptocurrency Classification Table**:
  - Use `hvplot.table()` to display the list of tradable cryptocurrencies.
- **Feature Scaling**:
  - Normalize **TotalCoinSupply** and **TotalCoinsMined** using **`MinMaxScaler()`** to scale values between 0 and 1.
- **Cluster Visualization**:
  - Create a **scatter plot** (`hvplot.scatter`) with:
    - **X-axis:** TotalCoinsMined
    - **Y-axis:** TotalCoinSupply
    - **Color-coded by cluster**
    - Coin names displayed upon hover.
![data-18-challenge-hvplot-scatter-plot](https://user-images.githubusercontent.com/111480084/225490409-2d035582-c487-4e66-a681-9b8bac6eb36b.png)
## Results
- The initial dataset was **not ideal** for machine learning models and required preprocessing.
- Since no predefined outputs existed, **unsupervised learning** was applied to explore patterns.
- The **elbow curve** helped determine the **optimal cluster count** for K-means.
- Clustering successfully categorized cryptocurrencies into **distinct investment groups**.
- The **3D scatter plot** visualized the cluster distribution.
- MinMax scaling standardized features for better comparison.
- Final scatter plots provided insights into **cryptocurrency supply and mined coins distribution**.

## Conclusion
This analysis provides key insights into the cryptocurrency market by:
- **Identifying distinct clusters of cryptocurrencies** based on market characteristics.
- **Reducing dataset complexity** through PCA while preserving essential variance.
- **Generating data visualizations** to facilitate investment decisions.

By leveraging **unsupervised learning**, this project equips investors with a **data-driven classification system** to enhance portfolio management and optimize cryptocurrency investment strategies.
