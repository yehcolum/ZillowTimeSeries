# Overview
<br>

Managers at a real estate investment firm seek the top 5 zip codes to invest in. This analysis seeks to identify those top 5 zip codes based on size, return on investment, and Sharpe ratio.
<br>

# Business Problem

The firm requires insight on the best zip codes to invest in. The following time series analysis will identify the top 5 zip codes based on ROI. These top 5 will be analyzed and modeled in order to draw accurate forecasts of the future. The models will forecast over a 3 year investment horizon. Each forecasted zip code will be evaluated on a risk adjusted basis to provide a recommendation on where to invest.

# The Data

Analyzed data of 14,723 zip codes in the United States from Zillow.com. Included monthly data of housing prices across each zip code, along with size rank.

# Modeling and results

Modeling criteria:
<br>

Size Rank: zip code must be in the top 50 size rank.
<br>
Larger size accounts for qualitative factors such as job opportunities, population, and other drivers of demand that fall outside the scope of this model
<br>

Return on Investment
<br>
Measures return relative to cost of the investment
<br>

Sharpe Ratio
<br>
An investment's sharpe ratio reveals the investment's return per unit of risk. It allows investors to evaluate returns on a risk adjusted basis. 


<br>
<br>
I sampled the top 50 zip codes according to size rank, then calculated ROI in each zip code over the historical period.
<br>
Revealed the top 5 Zip codes:
<br>
“Region 1” → 66126: Washington DC
<br>
“Region 2” → 66133: Washington DC
<br>
“Region 3” → 62037: Kings County, New York
<br>
“Region 4” → 96027: Long Beach/Anaheim, California
<br>
“Region 5” → 62040: Kings County, New York

# AutoArima Forecasting

The autoarima package enables a stepwise search of the best parameters of an ARIMA model. Autoarima was applied to each of the 5 identified regions. Next, each model forecasted a 3 year investment horizon:

<img width="377" alt="Screen Shot 2022-08-14 at 2 33 37 PM" src="https://user-images.githubusercontent.com/87211473/184564516-6fb6da6e-fcea-42af-a2fb-21f54df027fb.png">
<img width="408" alt="Screen Shot 2022-08-14 at 2 35 56 PM" src="https://user-images.githubusercontent.com/87211473/184564769-94f2f1ef-b56a-4709-9c3c-b81c509d8286.png">
<img width="402" alt="Screen Shot 2022-08-14 at 2 39 57 PM" src="https://user-images.githubusercontent.com/87211473/184564793-6aa52632-5dcc-4941-add6-7866fd81330d.png">

<img width="435" alt="Screen Shot 2022-08-14 at 2 39 20 PM" src="https://user-images.githubusercontent.com/87211473/184564813-1c379562-3e8f-4394-a1cb-beff312e40cb.png">
<img width="403" alt="Screen Shot 2022-08-14 at 2 37 49 PM" src="https://user-images.githubusercontent.com/87211473/184564827-58f45f31-bcd1-4311-8312-165365c36ae9.png">

# Interpretation

Returning to our modeling criteria, each regions return on investment and sharpe ratio was calculated and evaluated.
<br>

<img width="181" alt="Screen Shot 2022-08-14 at 2 41 53 PM" src="https://user-images.githubusercontent.com/87211473/184565063-aee92dcc-762d-4c88-92ac-374d65940187.png"><img width="130" alt="Screen Shot 2022-08-14 at 2 42 14 PM" src="https://user-images.githubusercontent.com/87211473/184565077-a42c9ec4-6d8e-49ab-9944-cb808176c0f5.png">
<br>
# Recommendations
Analyzing the forecasted ROI and sharpe ratio, I recommend to the firm:
<br>

Invest in region 1, 2, 3, and 5.
<br>
Do not invest in region 4
<br>

Regions 1, 2, 3, and 5 forecast ROI with efficient risk adjusted return. However, region 4 does not provide efficient risk adjusted return. Moreover, region 4 showed the lowest return on investment over the forecasted period.

# Limitations

Real estate prices are not just a function of time, but a relationship between supply and demand not fully captured by this analysis. Including exogenous variables such as interest rates, housing supply, or population growth would likely yield a better forecast. However, this falls outside the scope of this project.
<br>

Sampling the top 50 zip codes by size rank during EDA allowed us to somewhat capture qualitative factors not included.


