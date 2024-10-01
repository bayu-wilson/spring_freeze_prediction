# Predicting spring freeze for midwestern wheat yields
### Bayu Wilson 



#### Overview
In this project I leverage the XGBoost machine learning library and publically available weather data to forecast the date of last spring freeze ($T\leq 28$ degrees Farenheit) of a farm in Wyandotte county in Kansas (i.e. [K.C. Farm School](https://www.kcfarmschool.org/)). **Using the XGBoost model, I decreased the mean absolute error (MAE) by 25% in comparison to standard prediction methods.** These solutions can be generalized for any cold-sensitive crops in a variety of environments but I am mainly focused on spring freeze injury to Kansas wheat. See [this publication](https://bookstore.ksre.ksu.edu/pubs/spring-freeze-injury-to-kansas-wheat_C646.pdf) for more details. I gathered this dataset using [NOAA's Climate Data Online tool](https://www.ncdc.noaa.gov/cdo-web/search).

#### Main results
In Figure 1, I show an example of minimum temperature and temperature fluctuation forecasts after Jan. 31, 2010. Generally the average and variation of the true and predicted values are similar. We can also see form the purple vertical lines that the predicted and true last day of spring freeze (LDSF) are only 3 days apart. Farmers and gardeners often use the [farmer's almanac](https://www.almanac.com/gardening/frostdates) but its average-based predictions don't capture any variations. For example, using the average, the absolute difference from the true LDSF in 2010 is 7 days, over 2 times larger than my prediction.

<p align="center">
    <img src="https://github.com/user-attachments/assets/7f747f2a-84e0-42c8-811c-bf780449fd0c" alt="Description" width="500"/>
</p>
<p align="center">Figure 1. The true minimum temperature and temperature fluctuatuation distributions are in blue. The XGBoost model was trained prior to "today" and everything after "today" is forecasted (exept True distribution obviously). The data is noisy so it is not surprising that the predictions are not perfect. But since we have prior information of the seasonality (sine function) we can get pretty close. Our machine learning model can focus on temperature fluctuations rather than the total temperature. `T_flucs(t+1)` is the prediction for temperature fluctuations one day into the future. `T_flucs(t+7)` is the prediction for temperature fluctuations seven days into the future. LDSF is the last day of spring frost for the prediction and truth.</p>


Here I show the mean absolute error (MAE) between the predicted and true LDSFs.

|  MAE(Avg. LDSF over previous years, truth) | MAE(sine model minus $1\sigma$, truth) | MAE(XGBoost 1-day forcast, truth)  |
|----------|----------|----------|
| 10.2 days   | 8.9 days   | 7.6 days   |

**Using the XGBoost model, the MAE decrease by a factor of 25%**

