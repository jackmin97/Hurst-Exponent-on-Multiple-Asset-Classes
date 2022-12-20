# Hurst-Exponent-on-Multiple-Asset-Classes
In this notebook, we will show how to calculate the Hurst values for different securities.

### 1. Read prices from CSV file
First, we will import the necessary libraries and then, we will read the csv file with the different security prices using the 'read_csv' method of pandas.

### 2. Calculate Hurst exponent
We create functions get_hurst and hurst_plot which calculate and plot the Hurst exponent of all securities. We will be using Hurst value of 0.65 as a threshold to filter the securities. We will consider the securities having Hurst value greater or equal to 0.65 as trending securities.

#### Store securities according to their classes

### 2.1 Commodities
Hurst exponent of all the commodities except Platinum is higher than our predefined threshold that is 0.65. Crude oil has the maximum Hurst value among all commodities.

### 2.2 Stock indices
Hurst exponent of all stock indices are greater than 0.65, NASDAQ being the highest among them.

### 2.3 Currencies
All currency pairs have Hurst exponent less than 0.65. Therefore, we will not consider any currency pairs in the time series momentum strategy.

### 2.4 Treasuries
Hurst exponent of all the stock indices are greater than 0.65, SHY being the highest among them.

### 3. Filter securities with high Hurst exponent
We know that Hurst exponent greater than 0.5 exhibits trending behaviour. But to find a strong trend in a time series, we set the threshold of 0.65. We will consider only these securities having Hurst exponent greater than 0.65 for momentum strategy.
