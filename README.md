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
