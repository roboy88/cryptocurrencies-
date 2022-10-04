# Cryptocurrencies
### An analysis using unsupervised Machine Learning algorithm to discover unknown patterns.

![bannerimage](https://github.com/amylio/Cryptocurrencies/blob/main/Resources/Images/BannerImage.jpeg)

## Overview

The purpose of this analysis was to use data from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist) to provide a report and visualization of currently traded cryptocurrencies that can be grouped together to create a new classification system. This report would be used to help **Accountability Accounting** offer a new investment portfolio in the exciting world of cryptocurrency to its customers. 

Since the data does not have any known outcome, we needed to preprocess it to fit an unsupervised `Machine Learning` model that will enable us to run a clustering algorithm that will allow us to group the cryptocurrencies.

In this analysis we learned and applied:

* **Data Preprocessing** (Selection, Transformation, Scaling) - the process of helping to prepare data for `Machine Learning` Algorithms.
* **Elbow Curve** - method to determine the best number of clusters needed for the algorithm to group the objects by.
* **Principal Component Analysis (`PCA`)** - statistical technique to speed up machine learning algorithms when the number of features is too high.
* **Clustering Algorithms (`KMeans`)** - the process of grouping similar objects/data points into clusters.
* **Visualization (`hvPlot`, `Plotly`)** - graphic libraries that allows us to create 2D and 3D graphs such as, scatter plots.

## Results

The original dataset contained 1,252 entries, however only 1,144 cryptocurrencies were currently trading. The data was further munged to remove `null values` and only leave cryptocurrencies that had a total number of mined coins greater than 0. The final results identified 532 tradable cryptocurrencies. 

![cryptotable](https://github.com/amylio/Cryptocurrencies/blob/main/Resources/Images/CryptoTable.png)

The **Elbow Curve** method showed the slope at 4. This is the number of clusters that was used for the `KMeans` algorithm.

![Elbow](https://github.com/amylio/Cryptocurrencies/blob/main/Resources/Images/ElbowCurve.png)

The clusters are plotted in a 3D scatter plot for visualization.

![3D](https://github.com/amylio/Cryptocurrencies/blob/main/Resources/Images/3DGraph.png)

## Resources
* Dataset from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)
* Software: Python 3.7.9, Anaconda 4.9.2 and Jupyter Notebooks 6.1.4
* Libraries: `Scikit-learn`, `Plotly`, `hvPlot`, `Pandas`
