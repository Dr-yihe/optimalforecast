# optimalforecast
Optimal Forecast with Large Dimensional Regression
===========================================================================
DESCRIPTION
This zip file contains MATLAB code for the simulations and data analysis in 
the paper 'Optimal Forecast with Large Dimensional Regression' by Yi He

Last updated: April 3, 2019

===========================================================================
LIST OF FILES

This zip file contains two folders

- simulation: MATLAB codes for the simulation study,
- dataanalysis: MATLAB codes and datasets for empirical analysis.

Each folder contains a main MATLAB script and a set of auxiliary files that are called from the main script. The auxiliary functions should be saved in the same folder as the main script.

---------------------------------------------------------------------------
MAIN SCRIPT

The main scripts in each folder are:

- simulation: simulationmain.m
- dataanalysis: dataanalysis.m

---------------------------------------------------------------------------
AUXILIARY FILES IN THE FOLDER 'SIMULATION'

- rMAP.m
	Generate a correlation matrix  with a fixed set of eigenvalues by the method of alternating projections based on the R code by Niel Waller, October 27, 2016

- IID_set1.m
	The first set of simulations in the IID model. Generate Figures 2 and 3.

- IID_set2.m
	The second set of simulations in the IID model. Generate Figures 4 and 5.

- AR_set1.m
	The first set of simulations in the autoregressive model. Generate Figures 6 and 7.

- AR_set2.m
	The second set of simulations in the autoregressive model. Generate Figures 8 and 9.

- tls.m
	Tikhonov estimation: including optimal ridge and optimal linear shrinkage estimations.

- `savefig' package
	A toolbox for exporting figures from MATLAB to standard image and document formats licensed by Oliver J. Woodford, Yair M. Altman. The main function is export_fig.m

- calibratedata.mat
	the calibrated spectral distribution from the empirical dataset

---------------------------------------------------------------------------
AUXILIARY FILES IN THE FOLDER 'DATAANALYSIS'

- current.csv
	Monthly observations of 128 macroeconomic variables from Jan 1959 to Jan 2019

- INDPRO.csv
	Monthly observations of US industrial production index from Jan 1959 to Feb 2019

- fredfactors.m     
	This is the main MATLAB script from FRED-MD website: we only run the PARTS 1 and 2 in the script

- prepare_missing.m           
	FRED-MD MATLAB function that transforms the raw data into stationary form . 

- remove_outliers.m            
	FRED-MD MATLAB function that removes outliers from the data. A data point x is 
    considered an outlier if |x-median|>10*interquartile_range. 

- ARforecast.m
	Autoregression forecasts: select number of lags up to 4 by BIC

- datacalibration.m
	Calibrate the spectral distribution of the population correlation matrix used in the simulation study. Generate Figure 1.


- RWforecast.m
	Main script for performing rolling-window forecasting

- tls.m
	Tikhonov estimation: including optimal ridge and optimal linear shrinkage estimations.

- FRED-MD readme.txt
	The readme file from FRED-MD



