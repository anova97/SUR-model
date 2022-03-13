# SUR-model

The purpose of this project is to build a SUR model, a system of seemingly unrelated regression equations. 
The model will be built for stock market index returns of sectors such as:
-banks
-construction
-chemistry
-energy
-info
-media
-real estate
-fuels
-grocery
-telkom

All of the indices are based on the Polish stock market, so the random factors of the regression equations may be correlated. The sectoral index returns will be explained using the returns for the WIG index. 

## Dataset
Data downloaded from (https://stooq.pl). Monthly historical index data from January 2010 to December 2019 were downloaded. 
The indices include the WIG and 10 sector indices.

## Methodology
Logarithmic rates of return were calculated for the closing values.

The returns were then adjusted - risk free rate (3%).

The next step is to create MNK models in which the returns of sectoral indices are explained by the returns of the main index (WIG).

The GRS statistic will be computed for the asestimated models. To calculate its value, you will need:

sigma matrix - variance-covariance matrix,
vector of alpha coefficients, and
mean and variance of the WIG index return values. 
The values of residuals, which are the difference between the empirical value and the theoretical value of the explained variable, as well as the values of alpha coefficients were written in the matrix. 
The mean and inverse of variance for wig index returns were calculated.

The ADF test was used to verify that the rest of the models were stationary. 
