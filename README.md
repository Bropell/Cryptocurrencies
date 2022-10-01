# Cryptocurrencies
## Project Overview
This project focuses on creating a report that includes what cryptocurrencies are on the trading market and how they
could be grouped to build a classification system for an investment portfolio. The given data needed to be processed
to fit the machine learning models used and since the desired output was unknown, unsupervised machine learning was
the best approach. Data visualizations were generated and used as the final product to share the findings.

### Preprocessing the data for PCA
There were some modifications to the data that were required before PCA (Principal Component Analysis) could be done 
in order to give the machine learning algorithm only the correct and relevant information. The data was filtered to 
include only the cryptocurrencies being traded. The "IsTrading" column was then dropped because it is no longer 
relevant. Rows with null values were removed as well as rows with the total coins mined at zero. A new DataFrame was 
made to hold only the cryptocurrency names and this column was then dropped from the original DataFrame. The get_dummies() 
method was used to create numerical variables for the text features in the "Algorithm" and "ProofType" columns. Lastly, 
the data was standardized, fit and transformed with the StandardScaler().fit_transform() method. Snippets of the outputs
are displayed below. <br>

<h4 align="center">Text Variable Dataframe</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/Text_variable%20data.png"/>
</p><br>

<h4 align="center">Prestandardized Dataframe</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/Prestandardized%20data.png"/>
</p><br>

<h4 align="center">Standardized and Transformed Data</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/Standardized_transformed%20data.png"/>
</p><br>

### Reducing Data Dimensions using PCA
PCA was used to reduce the dimensions to three principal components from five. The data once again had to be transformed
which can be seen in the first image below. A new DataFrame was created from the PCA model which is displayed in the second 
image below.<br>  

<h4 align="center">PCA Transformed Data</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/PCA_transformed.png"/>
</p><br>

<h4 align="center">PCA DataFrame</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/PCA_DataFrame.png"/>
</p><br>

### Clustering Using K-Means
The first thing done in this section was to find the best k-value by creating and using an elbow curve. The sharpest point
of inflection, or the elbow of the curve, is the desired value. As seen in the elbow curve image below, a k-value of 4 was
found meaning a K-Means model with 4 clusters needed to be used. The model was fit and subsequent cluster predictions were 
made which can be seen in the second image below. Lastly, a new DataFrame was made to include the predicted clusters and 
cryptocurrency features.<br>

<h4 align="center">Elbow Curve</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/Elbow_Curve.png"/>
</p><br>

<h4 align="center">Prediction Clusters</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/Prediction_Clusters.png"/>
</p><br>

<h4 align="center">Clustered DataFrame</h4>
<p align="center">
    <img src= "https://github.com/Bropell/Cryptocurrencies/blob/main/Resources/Clustered_DataFrame.png"/>
</p><br>

### Visualizing the Results
