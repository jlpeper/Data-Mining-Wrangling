# Data-Mining-Wrangling
Language: Python

Packages: Quandl, Pandas, Regular Expressions, Pickle

Dataset: Zillow Real Estate Research available from the Quandl API (https://www.quandl.com/data/ZILLOW-Zillow-Real-Estate-Research/usage/quickstart/python


The Zillow dataset contains over 1,880,000 time-series tracking over 100 real estate indicators starting in 1969.

This code ultimately extracts (from the Quandl API) the "Zillow Home Value Index" of condos (indicator code: ZHVICO) in all counties for January 2013 and 2018. This is achieved in the following step:
1. The State, County_name, and Area_Code of all counties in the dataset are extracted (using regular expressions) from the available County Code mapping file. This data is written into a workable dataframe that serves as the template for the rest of our data mining. 
2. The Zillow Home Value Index of condos on January 2013 and 2018 for each available county is retrieved from quandl. The resulting datafame is joined (on "Code") with the dataframe (step 1) containing State and County_name information.

