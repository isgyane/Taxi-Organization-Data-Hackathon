# Data Analysis Report

Main AIM: To increase the revenue of the taxi organization.
Think of yourself as a data analyst working in a Taxi Organization and you are provided with data about the organization to drive their revenue and also to create detailed reports on their taxis and customers.

## Overview
From the EDA Notebook, the dataset appears to be well-structured and clean. The key variables—Total Amount, Fare Amount, Trip Distance, and Tip Amount—are correlated with each other, which makes sense in the context of transportation data.

## Key Data Transformations
Calculated columns were done in PowerBi instead of DAX to avoid a large model. DAX was used mainly for Calculated Columns. The calendar table was created using Power Query's M-Language 

I checked for trips were the drop off date was the next day. There were 19/1000 of them, meaning people travelled less at night


## Issues with Data
Customer ID Limitation: Each trip only has one Customer ID, but more than one customer can be on a trip (1-4 people per trip).

## Revenue Drivers
- For trip purposes, errands generated the most revenue, followed closely by business trips. However, the differences among the five groups are minimal.
- In terms of the day of the week, revenue was highest on Tuesday, Wednesday, and Friday.

## Correlation Analysis
- Trip Distance and Duration have a poor correlation; however, as distance increases, the fare amount also increases (correlation is 0.9). This indicates that focus should be given to long-distance trips with lower traffic.
- Total revenue was highest during moderate traffic conditions, while light traffic generated the least revenue. This could be due to reduced trip distances in light traffic conditions.

However, a correlation analysis conducted using Python in Power BI indicates that the single most important factor in revenue generation was DISTANCE.

### Important Notes on Correlation
- It is crucial to note that correlation measures the linear relationship between two variables. A near-zero correlation suggests that there is no linear relationship between the day of the week and total revenue. This does not imply that there is no relationship at all; it may indicate that any relationship is non-linear or influenced by other factors such as promotions, events, or seasonality that are not captured in simple correlation analysis.
- The near-zero correlations among other variables indicate that they do not have linear relationships with each other or with fare amounts. This could mean:
    * These variables may not be relevant to predicting fare amounts or other outcomes.
    * There may be non-linear relationships present that are not captured by simple correlation analysis.

Since correlation only captures linear relationships, future work could explore non-linear relationships using techniques such as:
- Polynomial Regression: To model non-linear relationships.
- Decision Trees or Random Forests: These can capture complex interactions and non-linearities without requiring explicit modeling of relationships.

## Visual Analysis
1. Location vs Total Revenue: Uptown locations generated the highest revenue, followed by Midtown.
2. Traffic Conditions: Moderate traffic situations seem to generate more revenue than heavy and light traffic.
3. Pickup Zones: Five pickup zones appear to generate more revenue (either more trips or people from those locations traveling further).
4. Trip Duration: More trips were recorded between 45 to 60 minutes, followed by 15 to 30 minutes. The average trip duration was 32 minutes.
5. Driver Performance: Some drivers generated more revenue by completing more trips; however, some drivers had higher revenue per trip despite having fewer trips. It is important to check route optimization for those making more trips with lesser revenue per trip.
6. Traffic Demand Patterns: Demand for cars is highest on Thursdays when most trips are for leisure, followed by Tuesdays and Wednesdays when trips are primarily for errands. 




