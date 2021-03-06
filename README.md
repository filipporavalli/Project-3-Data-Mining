# Project 3 Data Mining Final Report
Our project examines the relationship between perceived health and actual health based on income levels. Using 2019 data from the CDC's Natinoal Health Interview Survey and weights data from the 2019 Global Burden of Disease, we engineered a composite health score as a proxy for actual health and then ran a linear regression algorithm to identify any patterns of interest. We found that higher income was associated with increased accuracy for individuals in identifying better health, while also reducing accuracy in identifying poorer health. For lower income, the opposite was found to be true, with accuracy increasing as actual health decreased. Our findings were corroborated with existing literature and model validation showed 66.67% accuracy.

Link for NHIS Data (Demographic data, perceived health, medical conditions): https://www.cdc.gov/nchs/nhis/2019nhis.htm

Link for Global Burden of Disease Data (Weights): http://ghdx.healthdata.org/record/ihme-data/gbd-2019-disability-weights

Link for Written Report: https://github.com/filipporavalli/Project-3-Data-Mining/blob/main/fr2420%20nrr2121%20Project%203%20Report.pdf

To reproduce:
Our RMD file contains the necessary variables that overlapped between both datasets that have been hardcoded in. The NHIS dataset used was the 2019 "Sample Adult Interview" and the corresponding CSV file was downloaded. The weights data was obtained from the IHME website. The imputed health score weights have also been hard coded. To reproduce, downloading both datasets and subsetting income and perceived health in addition to the medical conditions which overalpped in the NHIS dataset will result in creating the processed dataset, before score creation. To create the health score, use the estimated weight data from the IHME dataset for each overlapping condition. If a condition had multiple weights (Eg. Different weights for different disease severity stage), averages were taken and used as the weight for the corresponding condition in the NHIS data. Our code lists these steps and all code used for the algorithm and visualization creation can be found in the RMD file.
