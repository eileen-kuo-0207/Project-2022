## Total Taiwan Coronavirus Cases Forecasting
<p>Using raw data from <a href="https://github.com/CSSEGISandData/COVID-19" title="">Johns Hopkins University</a> to predict exponential growth with data through <strong>September 30</strong> for total cases in Taiwan.</p>

### Model: Simple exponential function

$𝑓(𝑥)= 𝑎𝑏^{𝑥}$ 

<strong>a</strong> - initial value
<br>
<strong>b</strong> - growth rate (b > 1, growth to infinity ; b < 1 declines to 0)
<br>
<strong>𝑥</strong> - time

### Step.1 Data Cleaning
1. Download Data from John Hopkins github 
2. Group by Country/Region
3. Transpose data to time series
4. check and handle bad data (data that is not cummulative)

### Step.2 Find optimal values that are close to actual values using least squared function
1. set <strong>x</strong> value as <strong>time</strong>, <strong>y</strong> value as <strong>cases</strong>
2. Create a function `optimize_func` that minimize squared distance between model and actual data and return the errors
3. Set `optimize_func` as the first argument of the least squared method
4. set initial guess `p0` as `1` for a and b
5. set `lower bound` as 1 for both <strong>a</strong> and <strong>b</strong>
6. set `upper bound` a infinity `np.inf` for <strong>a</strong> , and `10` percent for <strong>b</strong>


*Actual data*
<br>
![alt text](https://github.com/eileen-kuo-0207/Project-2022/blob/4d86746a758fb3c6c1b2a27fd84d3bed3a317552/taiwan%20data%20from%20march%20to%20sep.png)

### Dependencies


