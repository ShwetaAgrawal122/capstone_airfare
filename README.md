### Airfare forcast 

#### Flow of the project
1 Problem Statement
2 Data Collection and Cleaning
3 EDA & Pre-Processing 
4 Modeling 
5 Evaluation
6.Web Application and deployment
7.Conclusion

#### Data directory 
(https://data.transportation.gov/Aviation/Consumer-Airfare-Report-Table-1a-All-U-S-Airport-P/tfrh-tu9e)

description : Data provides information for airport pair markets rather than city pair markets. This table only lists airport markets where the origin or destination airport is an airport that has other commercial airports in the same city. Midway Airport (MDW) and O'Hare (ORD) are examples of this.  All records are aggregated as directionless markets.  The combination of Airport_1 and Airport_2 define the airport pair market.  All traffic traveling in both directions is added together.



Column_name             Description                                                                              Data Type

Year            Year 1993-2020                                                                                  Number

quarter         Quarter 1-4                                                                                      Number                                      
city1           City1 is used to consolidate airports serving the same city market for airport1(origin)                                 
city2           City2 is used to consolidate airports serving the same city market for airport2(destination)

airport_1       Airport code(origin airport code)

airport_2       Airport code(destination airport code)

nsmiles         Non-Stop market miles (using radian measure)

passengers      Passenger per day

fare            Overall average fare for the quater

carrier_lg      Carrier with the largest market share

large_ms        Market share for the carrier with the largest market share

fare_low        Average fare for the lowest carrier

carrier_low     Carrier with the lowest fare

lf_ms           Market share for the lowest carrier




(https://www.infoplease.com/math-science/weather/climate-of-100-selected-us-cities)
1. Based on 30-year period 1971 - 2000.
2. city - weather data

(https://www.eia.gov/opendata/qb.php?sdid=PET.EER_EPJK_PF4_RGC_DPG.M)
1. monthly jet fuel data for year 1990 to 2021


### 1. Problem statement
Based on a comparison of a online airfare quote vs. models airfare prediction, a user can make a decision if he/she book the ticket right away or later for that certain route.

### 2. Data collection
[Monthly Jet fuel prices](https://www.eia.gov/opendata/qb.php?sdid=PET.EER_EPJK_PF4_RGC_DPG.M)
[Quaterly city pair airfair](https://data.transportation.gov/Aviation/Consumer-Airfare-Report-Table-1a-All-U-S-Airport-P/tfrh-tu9e)

Data sets can not be stored in github since they were big in size. So they in git ignaure file. 

### 3. EDA and preprocessing

1. Merged these two data sets on the same key(yearly and monthly)
2. Select unique routs for same time frame
3. creating a data frame to build model
3. Finding correlations and trends between variables
4. Few visualizations

### 4. Modeling

1. OLS model to fearure selection
2. Weighted Moving Average Model
3. SARIMEX model

### 5. Evaluation

1. Base line score for each route
2. R2 score for each rote
3. RMSE for each route

### 6. Web Application and deployment

1. Streamlit to create a web application
2. Cloudflare to deploy the application

### 7. Conclusion 

1. Got the predictions with R2 score 93%.

2. Beat the baseline R2 score 52% for NC to FL route with R2 score 93%

3. Beat the baseline R2 score 22% for TX to MS route with R2 score 88%

### 8. Nexsteps

1. Explore more routes.

2. Use graph theory to compute shortest route.

3. If I could get airfare data on dailybasis then forecasting airfare for next week and so, would be more useful.

4. Build application in a more interactive and robust.
























