# Flight-Delays

This repository contains the presentation, jupyter notebooks and D3.js visualizations for my third Metis project, predicting flight delays. My goal was both to be able to identify which flights will be delayed using only information available several days before the flight takes off, and to identify which features have the most influence on whether or not a flight is delayed. 

My investigation consisted of two parts. First, I looked at all domestic flights in 2016 (>500K flights) using only the [Bureau of Transportation Statistics public data](https://www.transtats.bts.gov/DL_SelectFields.asp?Table_ID=236) on flight delays, which include features such as origin, destination, date, scheduled hour departure/arrival and carrier. Second, I narrowed my focus to flights from JFK to LAX and introduced weather data at both airports from [National Oceanic and Atmospheric Administration](https://www.ncdc.noaa.gov/cdo-web/).

To solve these problems, I used several classification algorithms in scikit-learn: logistic regression, random forest, k nearest neighbors, naive bayes and support vector machine. Using the coefficients from the logistic regression models, I made D3.js visualizations of feature importance. The first visualization is without weather, the second is with weather.

![Feature Importance No Weather](https://github.com/michaelaaroncantrell/Flight-Delays/blob/master/images/All-Bubbles.png)

![Feature Importance Weather](https://github.com/michaelaaroncantrell/Flight-Delays/blob/master/images/Weather-Bubbles.png)

The size of the bubbles correspond to the amount of influence the feature has. The features in orange are negatively correlated with delays. For example, an increase in visibilty in JFK correlates with an decrease in likelihood of delay. The blue bubbles have positively correlation with delay.

Here's a comparison of how the different models compared on the JFK-LAX weather problem.

![Comparison-Weather]((https://github.com/michaelaaroncantrell/Flight-Delays/blob/master/images/model-comparison.png)




