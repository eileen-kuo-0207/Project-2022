## Total Taiwan Coronavirus Cases Forecasting
<p>Using raw data from <a href="https://github.com/CSSEGISandData/COVID-19" title="">Johns Hopkins University</a> to predict exponential growth with data through <strong>September 30</strong> for total cases in Taiwan.</p>

## Model: Simple exponential function

$𝑓(𝑥)= 𝑎𝑏^{𝑥}$ 

<strong>a</strong> - initial value
<br>
<strong>b</strong> - growth rate (b > 1, growth to infinity ; b < 1 declines to 0)
<br>
<strong>𝑥</strong> - time (b > 1, growth to infinity ; b < 1 declines to 0)

## Set Arguments
<strong>x-values</strong> as time
<br>
<strong>y-values</strong> as cases

## Data Cleaning
1. Download Data from John Hopkins github 
2. Group by Country/Region
3. Transpose data to time series
4. check and handle bad data (data that is not cummulative)
<br>

<img src="https://github.com/eileen-kuo-0207/Project-2022/blob/4d86746a758fb3c6c1b2a27fd84d3bed3a317552/taiwan%20data%20from%20march%20to%20sep.png" alt="GitHub" title="width='800'" height="300"/>
<br>
<img src="https://github.com/eileen-kuo-0207/Project-2022/blob/4d86746a758fb3c6c1b2a27fd84d3bed3a317552/taiwan%20data%20from%20march%20to%20sep.png" alt="GitHub" title="width='800'" height="300"/>


## Create model using `least_squared` function 


>Step 1 - Create simple exponential function

>Step 2 - Create a function that return errors between actual data and model 

>Step 3 - Set initial guess for <strong>a</strong> and <strong>b</strong>

>Step 4 - Set arguments to pass into error function

>Step 5 - Set lower and upper bounds 
1. set `lower bound` as `1` 
2. set `upper bound` as infinity for <strong>a</strong> , and `10` percent for <strong>b</strong>

>Step 6 - Return model `least_squared` errors





