# CryptoClustering
The CryptoClustering project aims to predict if cryptocurrencies are affected by 24-hour or 7-day price changes using unsupervised machine learning techniques, specifically K-means clustering. Additionally, the project explores the impact of dimensionality reduction using Principal Component Analysis (PCA) on clustering.


## Installation and Run Instructions:
You may need to install the **scikit-learn** and **hvPlot** packages before commencing:

### scikit-learn:
1. Open **Gitbash** and activate your virtual environment.
2. Run **conda list scikit-learn**. If the response includes a version number for scikit-learn, then the library is already installed and you can safely skip the following steps. Otherwise:
3. Run **pip install scikit-learn** in the terminal.
4. Confirm installation by running **pip show scikit-learn**.

### hvplot:
1. Open **Gitbash** and activate your virtual environment.
2. Run **conda list hvplot**. If the response includes a version number for hvplot, then hvplot is already installed and you can safely skip the following steps. Otherwise:
3. Run **conda install -c pyviz hvplot** in the terminal.
4. Confirm installation by running **conda list hvplot**.


## Usage Instructions:
This repo contains the following:
1. **crypto_market_data.csv:** data on percentage change in trading prices over 24 hour, 7 day, 14 day, 30 day, 60 day, 200 day, and 1 year intervals for 41 different cryptocurrencies, and
2. **Crypto_Clustering.ipynb:** a python script, executed in JupyterLab, to reproduce the analyses.

Executing the script provided in the **Crypto_Clustering.ipynb** file will:
1. Read the data in from the **crypto_market_data.csv**, converting this to a DataFrame;
2. Scale the numeric data using the **StandardScaler()** module from **scikit-learn**;
3. Create an elbow plot to visually represent the optimal number of data clusters for k-means clustering;
5. Initalise a k-means clustering model based on the optimal number of data clusters identified from the elbow plot;
6. Predict class membership and produce a plot of cryptocurrencies based on these;
7. Use a Principal Components Analysis (PCA) model to reduce the number of features within the original **crypto_market_data.csv** dataset;
8. Estimate the percentage of variance explained by the principal components;
9. Create an elbow plot to visually represent the optimal number of data clusters for based on the PCA;
10. Initalise a k-means clustering model based on the optimal number of data clusters identified from the elbow plot based on the PCA;
11. Predict class membership and produce a plot of cryptocurrencies based on the PCA predictions.


## Credits:
This code was compiled and written by me for the CryptoClustering challenge project in the 2024 Data Analytics Boot Camp hosted by Monash University. Additional credits are declared below:

### Creating composite plots using the '+' function:
https://hvplot.holoviz.org/user_guide/Plotting.html (accessed 7 July 2024).
