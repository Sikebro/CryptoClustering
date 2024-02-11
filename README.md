# CryptoClustering
Module 19 Challenge

<h2>Instructions</h2>
<ol>1. Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.</ol>
<ol>2. Load the crypto_market_data.csv into a DataFrame.</ol>
<ol>3. Get the summary statistics and plot the data to see what the data looks like before proceeding.</ol>

<h2> Prepare the Data </h2>
<ol>Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.</ol>

<ol>Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.</ol>

<ul>The first five rows of the scaled DataFrame should appear as follows:</ul>

![image](https://github.com/Sikebro/CryptoClustering/assets/89745480/b762906a-1979-413a-a055-557e04aa3c5a)

<h2>Find the Best Value for k Using the Original Scaled DataFrame</h2>
Use the elbow method to find the best value for k using the following steps:

<ol>Create a list with the number of k values from 1 to 11.</ol>
<ol>Create an empty list to store the inertia values.</ol>
<ol>Create a for loop to compute the inertia with each possible value of k.</ol>
<ol>Create a dictionary with the data to plot the elbow curve.</ol>
<ol>Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.</ol>
<ol>Answer the following question in your notebook: What is the best value for k?</ol>

<h2>Cluster Cryptocurrencies with K-means Using the Original Scaled Data</h2>
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

<ol>Initialize the K-means model with the best value for k.</ol>
<ol>Fit the K-means model using the original scaled DataFrame.</ol>
<ol>Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.</ol>
<ol>Create a copy of the original data and add a new column with the predicted clusters.</ol>
<ol>Create a scatter plot using hvPlot as follows:</ol>
<ul>Set the x-axis as "PC1" and the y-axis as "PC2".</ul>
<ul>Color the graph points with the labels found using K-means.</ul>
<ul>Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.</ul>

<h2>Optimize Clusters with Principal Component Analysis</h2>
<ol>Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.</ol>

<ol>etrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:</ol>
<ul>What is the total explained variance of the three principal components?</ul>

<ol>Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.</ol>
<ul>The first five rows of the PCA DataFrame should appear as follows:</ul>

![image](https://github.com/Sikebro/CryptoClustering/assets/89745480/8fa218e7-747e-409c-b0be-b6ad39b00fe2)


<h2>Find the Best Value for k Using the PCA Data</h2>
Use the elbow method on the PCA data to find the best value for k using the following steps:
<ul>
<li>Create a list with the number of k-values from 1 to 11.</li>
<li>Create an empty list to store the inertia values.</li>
<li>Create a for loop to compute the inertia with each possible value of k.</li>
<li>Create a dictionary with the data to plot the Elbow curve.</li>
<li>Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.</li>
<li>Answer the following question in your notebook:</li>
</ul>
<li>What is the best value for k when using the PCA data?</li>
<li>Does it differ from the best k value found using the original data?</li>
</ul>
</ul>

<h2>Cluster Cryptocurrencies with K-means Using the PCA Data</h2>
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
<ul>
<li>Initialize the K-means model with the best value for k.</li>
<li>Fit the K-means model using the PCA data.</li>
<li>Predict the clusters to group the cryptocurrencies using the PCA data.</li>
<li>Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.</li>
<li>Create a scatter plot using hvPlot as follows:</li>
<ul>
<li>Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".</li>
<li>Color the graph points with the labels found using K-means.</li>
<li>Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.</li>
</ul>
<li>Answer the following question:</li>
<ul>
<li>What is the impact of using fewer features to cluster the data using K-Means?</li>
</ul>
</ul>
