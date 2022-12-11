## Taiwan Coronavirus Cases Forecasting 
<p>Using raw data from <a href="https://github.com/CSSEGISandData/COVID-19" title="">Johns Hopkins University</a> to predict exponential growth for total cases in Taiwan.</p>

### Functions for modeling

$𝑓(𝑥)= 𝑎𝑏^{𝑥}$ 

<strong>a</strong> - initial value
<br>
<strong>b</strong> - growth rate
<br>
<strong>𝑥</strong> - time

### Step1 Data Cleaning
1. Download Data from John Hopkins github 
2. Group by Country/Region
3. Transpose data to time series
4. check and handle bad data (data that is not cummulative)

### Step2 
1. Find optimal value of initial value and growth rate
2. Use <strong>least_square<strong> scipy function 


### Dependencies


