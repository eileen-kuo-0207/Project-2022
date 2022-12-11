## Total Taiwan Coronavirus Cases Forecasting
## 用最小平方法預測台灣疫情總確診數
<p>Using raw data from <a href="https://github.com/CSSEGISandData/COVID-19" title="">Johns Hopkins University</a> to predict exponential growth with data through <strong>September 30</strong> for total cases in Taiwan.</p>


## Data Cleaning
1. Download Data from John Hopkins github 
2. Group by Country/Region
3. Transpose data to time series
4. check and handle bad data (data that is not cummulative)
<br>

<img src="https://github.com/eileen-kuo-0207/Project-2022/blob/10f3c0832c87124756ae3d0a8f57e598e565f350/cleaning%20data.png" alt="GitHub" title="width='500'" height="200"/>

## Model: Simple exponential function

$𝑓(𝑥)= 𝑎𝑏^{𝑥}$ 

<strong>a</strong> - initial value
<br>
<strong>b</strong> - growth rate *(b > 1, growth to infinity ; b < 1 declines to 0)*
<br>
<strong>𝑥</strong> - time 

## Create model using `least_squared` function 

>Step 1 - Create simple exponential function

>Step 2 - Create a function that return errors between actual data and model 

>Step 3 - Set initial guess for <strong>a</strong> and <strong>b</strong>

>Step 4 - Set arguments: <strong>x-values</strong> as *time* , <strong>y-values</strong> as *cases* to pass into error function

>Step 5 - Set lower and upper bounds 
+ set `lower bound` as <strong>1</strong> 
+ set `upper bound` as <strong>infinity</strong> for <strong>a</strong> , and <strong>10%</strong> for <strong>b</strong>

>Step 6 - Return model `least_squared` errors

<img src="https://github.com/eileen-kuo-0207/Project-2022/blob/27e3e382a5fd6c034588413915267d5579696df1/create%20model.png" alt="GitHub" title="width='600'" height="300"/>
<br>

> <strong>This model shows the growth rate to be around 1.1% per day beginning at an initial value about 10,000.<strong>

<img src="https://github.com/eileen-kuo-0207/Project-2022/blob/a3bd13dd0fac6233b443e97fb48708479fb9e9a1/create%20model%202.png" alt="GitHub" title="width='600'" height="300"/>

## Predicting unseen data

>Stop the time at July 30 and see what the unseen model predicts
  
<img src="https://github.com/eileen-kuo-0207/Project-2022/blob/65d914c5d000be7b43dcb589cf0fccdd5913060c/predict%20unseen%20data.png" alt="GitHub" title="width='800'" height="400"/>
