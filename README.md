# Ahomagai.github.io

The repository for my personal website that showcases (some) of my projects that I've done so far. 

Link for full website with (more!) details: https://ahomagai.github.io/

### Highlights of my work:

## COVID 19 and Mortality (R & Forecasting time-series data )

### Did states that had more people travel during the pandemic also coincide with more deaths? 
<br> </br>
![Alt text](https://github.com/Ahomagai/Ahomagai.github.io/blob/main/images/US%20State%20Mortality%20Rates%20across%20Normalized%20Avg%20Number%20of%20Trips.png)

<br> </br>
<p>Not really but this data takes into account all of the COVID 19 mortality from the beginning to end of 2023. Plenty of health policy and protective measures such as masking, physical distancing, air purification and the distribution of the vaccines in early 2021 may have an impact on this. </p>
<p> But what about if we limit to just the 2020 year? </p>

<br> </br>
![Alt text](https://github.com/Ahomagai/Ahomagai.github.io/blob/main/images/2020_US_State_Mortality_Rates_by_Normalized_Average_Trips.png)

<p> Now a more interesting story emerges, although the relationship is weak, r=0.34, p<0.05, there is some significant correlation between mortality rates and number of trips taken in 2020. Red dots represents states where mortality rate was >400 deaths per 100,000 and green dots represent mortality rates <200 per 100,000. Population density could for sure have played a role in these results but it is interesting that it isn't just more population / higher density -> higher deaths, as was the case with North Dakota being high in deaths with less than 1,000,000 in population. </p>

<br> </br>
### Forecasting Covid 19 cases using autoregressive models 
<br> </br>
<p> Let's look at some time-series forecasting data using an AutoRegressive Integrated Moving Average (ARIMA). Here I'm using the NYT Covid Cases Dataset. Data was split into test and training set with prediction of the last 7 days of COVID-19 cases being the objective.  </p>

![Alt text](https://github.com/Ahomagai/Ahomagai.github.io/blob/main/images/Forecasted%20COVID%20Cases.png)

<br></br>
<p> With the seasonal (I assumed seasonality here with COVID cases rising and falling in conjunction with the geographic seasons) ARIMA model, we see that while the model tends to overestimate the actual cases (see table below) it is still within the 80th and 90th percentile bounds with a large deviation in accuracy in the 3rd day. </p>

| Predicted Cases     | Actual Cases    | Accuracy |
| --------- | ---------- |--------- |
| 148970.475| 113283     | 1.3150294| 
| 83257.077	|78852	     | 1.055865 |
| 49906.312	| 14171	     | 3.521722 | 
| 3492.481	| 2200	     | 1.587491 |
| 5437.599	| 4424	     | 1.22911  |
| 21686.059	| 30449	     | 0.71220  |
| 45567.099	| 31067	     | 1.46673  |

<br></br>


## Geospatial Data analysis (Tableau, Python) 
<br></br> 
Link to full analysis: https://ahomagai.github.io/Ont_Prov_Election_Insight.html

<p>I think these two following graphs is really all you need to look at to get a sense of how different parties performed in the 2022 Provincial Election compared to the 2018 Election. (2025 election data is in development, don't you worry). P.S. on the full analysis website both of these graphs are interactable. </p>

### Who took from who? 

<br></br>

<p> This a nice way to showcase how each party performed overall in the 2022 election compared to 2018. Rows represent ridings won in 2018 & columns represent ridings won in 2022 by different parties in their corresponding colors (Red=Liberal, Orange = NDP, Green = Green, Blue = Conservatives). Points outside the part diagonal represent losses or gains in ridings from each party from another. For example, if we look at the LIB row and NDP column, we see the Liberals lost 1 district they'd won in 2018 to NDP in 2022 while the NDP lost 2 districts in 2022 to Liberals that they had won in 2018. </p>

![Alt text](https://github.com/Ahomagai/Ahomagai.github.io/blob/main/images/Who%20took%20from%20who.PNG)
<br></br> 



<br></br>
<p>Suffice to say, the biggest losers were the NDP; when they lost ridings, it was mostly to the PCP. The PCP managed to gain even more ground, recouping in 2022 many districts they'd lost in 2018 to NDP. </p>

### Change in %votes gathered from each party from 2018 - 2022 
<br></br>
![Alt text](https://github.com/Ahomagai/Ahomagai.github.io/blob/main/images/Voting%20Changes%20across%20Ontario's%20Election%20Districts.PNG)
<br></br>

<p> Point colors represent districts won by each party according to their respective colors. Values below 0 indicate reduction in votes 2022 compared to 2018 as a percentage of total votes cast in that riding. Lower is worse, higher is better. Green vertical bars represent ridings that switched winners from 2018 to 2022. <br> 

  Overall, the NPD once again lost votes across a wide range of ridings with only a few being above 0 (gaining votes). Even in the ridings they'd won in 2022, their vote percentage compared to 2018 was lower. What the NDP lost, the LIB and PCP gain. However, with the performance of the LIB party in 2018, their 2022 results seem more like a regression to the mean rather than a substantial comeback. Finally, the PCP ride strong with most of their voting % teetring just above the 0% mark, showing an even stronger performance in 2022 compared to 2018.  </p>
