# Predicting spring freeze for midwestern wheat yields
Bayu Wilson & Cecelia Ngo

### Notes
The purpose of this project is to use publically available weather data to forecast the last frost in a particular location. By "last frost" I mean the last date in which the air temperature is below freezing after summertime. This would mainly be beneficial in the field of agriculture. For example, [this publication](https://bookstore.ksre.ksu.edu/pubs/spring-freeze-injury-to-kansas-wheat_C646.pdf) shows the effect of spring freeze injury to Kansas wheat. It would be a good idea to read this.

Assumptions:
- Winter wheat is the crop of interest
- The region of interest is midwestern farmers, specifically Kansas farmers. But maybe it would be interesting to consider Ukraine? More relevant to current events.

According to [this website](Long%20Does%20Wheat%20Take,months%20when%20it%20goes%20dormant.), growing winter wheat takes about 180–250 days. Winter wheat growth time includes up to 90 days during the colder months when it goes dormant.

According to [the first publication](https://bookstore.ksre.ksu.edu/pubs/spring-freeze-injury-to-kansas-wheat_C646.pdf), the most severe crop impacts (due to spring freeze injury) will happen during the heading and flowering stage. 

If a farmer knows ahead of time, they can take action. For example, they can delay fertilization, wet the plants (evaporation releases heat), or covering the crops with insulation (like straw).

Let's assume that 1 month (or 1 week) is all a farmer needs to do properly mitigate these problems (monthly timescale mostly due to slow-release fertilizers).

What factors would likely be good indicators for predicting a spring frost?
- Daily Minimum Temperature
- Temperature rate of change
- precipitation (want soil to be somewhat damp)
- prior information about typical frost dates



