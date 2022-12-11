## Total Taiwan Coronavirus Cases Forecasting
<p>Using raw data from <a href="https://github.com/CSSEGISandData/COVID-19" title="">Johns Hopkins University</a> to predict exponential growth with data through <strong>September 30</strong> for total cases in Taiwan.</p>

### Simple Function for model

$𝑓(𝑥)= 𝑎𝑏^{𝑥}$ 

<strong>a</strong> - initial value
<br>
<strong>b</strong> - growth rate (b > 1, growth to infinity ; b < 1 declines to 0)
<br>
<strong>𝑥</strong> - time

### Step1 Data Cleaning
1. Download Data from John Hopkins github 
2. Group by Country/Region
3. Transpose data to time series
4. check and handle bad data (data that is not cummulative)

### Step2 Find optimal values that are close to actual values
1. Create a function that returns the error from model to actual value 
2. Find the optimal values of <strong>a</strong> and <strong>b</strong>
3. Guess upper and lower bounds to <strong>1</strong> 


Original data


### Dependencies


