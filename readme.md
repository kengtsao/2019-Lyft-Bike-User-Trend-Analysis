# Lyft Bike Analysis

## Dataset

This document explores a dataset containing Lyft bike rental records of first half year of 2019.
The data consisted attributes of users of approximately 1.2 millions Lyft renting records from January 2019 to June 2019. The attributes include user type, gender, start and end station locations ... etc. 68k datapoints are removed during the analysis because of missing values or inconsistencies.

## Assumptions

- People older than 100 years old won't use this service 
- People rent bikes more than 8 hours are outliers and does not fit the goal of this analysis

## Summary of Findings

In the exploration, I found that 
- Renting duration is a long tail distribution and most renting durations are shorter, I used log-scale duration for visualization. Log scale duration is a normal distribution with the center around 500-1000 seconds, which is reasonable with my personal experience. 
- People usually ride a bike for 5-10 mins for a commute distance that is slightly longer for walking and too short for driving. The majority of users are around 20 to 40 years old. March and April have more activate users than other months and 7-9am and 5-6pm are definitely the pick hour for people to commute with bikes. 
- Subscribers tend to rent slightly shorter time than customers. The mean of subscriber renting time is 350 seconds and the mean of customer renting time is around 500 seconds. 
- There is a trend that the frequency of bike renting is higher in weekday, but the average renting duration is higher during weekends. This result meets our daily experience. During the weekday, people rent bikes for commute. Short distances and frequent renting. In the weekend, people rent bikes for visiting and traveling, which takes longer time. 
- Renting duration is San Francisco is much longer than other areas.
- The quantity of females renting Lyft bikes is lower than male. Lyft bike is more frequently used in San Francisco than Oakland and the least popular area is San Jose. San Francisco active stations are the most concentrated (smaller longitude and latitude range). 


## Key Insights for Presentation

For the presentation, I focus on the influence of the age, user type, gender and week of day and leave out most of the intermediate derivations. I start by introducing the
rent duration distribution, followed by the pattern in age distribution and how the categories of groups afftect rent duration.

I started with violin plots of user type and member gender and the next plot is the effect of day of week to rent duration. Moreover, I digged out how day of week affect rent duration of different cities, genders and user types. I've made sure to use different color for each categories and put legend on plots. In the last plot of location of start stations in cities, I've made sure to downsize sample for plotting. If I used 1.1 million data points in the plot, we can't see any trends.
