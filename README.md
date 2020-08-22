# Analyzing Cryptocurrencies, Using Unsupervised Learning Model.
## Purpose
The purpose of this analysis was to find Cryptocurrencies that were potential good investements. This was done by identifying patterns(using unsupervised learning model) among the current trading Cryptocurrencies and grouping them into meaningful clusters.

## Process
The process took in raw data of all the Cryptocurrencies from [Crypto_data.csv](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/crypto_data.csv) and transformed it using the following three stages:

**- Preprocessing:**
  - Removing Null Values
  - Screening for the currencies that are trading 
  - Getting dummy value for text features
  - Scaling the data using Standardsacler
  - Performing a dimension reduction using pca model, with n_components=3.
  
  **-Clustering:**
  - Elbow curve to find the best value for K clusters:
  ![](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/Elbow-Curve.png)
  
  **-Visualization:**
  
## Resources
### Data
### Software
