# Analyzing Cryptocurrencies, Using Unsupervised Learning Model.
## Purpose
The purpose of this analysis was to find Cryptocurrencies that were potential good investements. This was done by identifying patterns(using unsupervised learning model) among the current trading Cryptocurrencies and grouping them into meaningful clusters. the input columns were 'Algorithm',	'ProofType',	'TotalCoinsMined' and 'TotalCoinSupply'.

## Process
The process took in raw data of all the Cryptocurrencies from [Crypto_data.csv](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/crypto_data.csv) and transformed it using the following three stages:

**- Preprocessing:**
  - Removing Null Values
  - Screening for the currencies that are trading 
  - Getting dummy value for text features
  - Scaling the data using Standardsacler
  - Performing a dimension reduction using pca model, with n_components=3.
  
  **-Clustering:**
  - Elbow curve was utalized to find the best value for K clusters:
  ![](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/Elbow-Curve.png)
  _A k value of **4** was decided based on the above plot._
  
  **-Visualization:**
  - 3D Scatter plot(using hvplot) with 3 PCS as features and hover_name="CoinName" & hover_data=["Algorithm"] 
 
  ![](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/newplot-3DPlot.png)
  
  -Table visualization withe the columns;'CoinName', 'Algorithm', 'ProofType', 'TotalCoinSupply', 'TotalCoinsMined' and 'Class'(to view table click [table](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/cryptocurrencies_by_cluster.csv)
  
  
  ![](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/table.png)
  
  - 2D scatter plot with x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins.
  
  
  ![](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/2D-ScatterPlot.png)
  
## Summary and Conclusion
Looking at all the visualizations the four groups can be classified as :
1 High supply, high coins mined (BitTorrent)
2 High supply, low coins mined (Turtle Coin)
3 Low Supply, low coins mined
4 Low Supply, moderate coins mined.

## Resources
### Data
[](https://github.com/Muzznah/Cryptocurrencies/blob/master/Data/crypto_data.csv)
### Software
Python 3.7.7, Jupyter Notebook 6.0.3, scikit-learn 0.23.1, scipy 1.4.1,pandas 1.0.5, plotly 4.8.2, and hvplot 0.6.0
