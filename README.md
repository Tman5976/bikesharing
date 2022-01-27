# bikesharing

## Overview of Project

The project focused on using Tableau to create a story visualizing data from a 2019 study examining a bike-sharing program in New York City.

This project aims to create a story presented to potential investors to peak interest in developing similar programs in other cities.

## Objectives

### Step 1 - Data Cleaning
Using a jupyter notebook to examine and clean data for easy use in creating Tableau story.

Changing the `tripduration` column from int64 to DateTime was the only adjustment needed.

``` citibike_data_df["tripduration"] = pd.to_datetime(citibike_data_df["tripduration"], unit='s') ```


### Step 2 - Tableau

Seven visualizations were created to communicate the results of the data. A link to the full Tableau story is provided below.

[CitiBike Story](https://public.tableau.com/app/profile/tony.giombetti/viz/CitiBikeWorkbook_16333093573820/Story1#1)

#### Count of trips started per station
The first graph shows the number of trips started by individual bike stations. The stations that see the most trips started are represented by the largest and darkest circles.

<img src="https://user-images.githubusercontent.com/85756203/135904333-31b4119c-4a96-4d69-ae4f-e720682b5317.png" width=85% height=85%>

#### Hour/Day heat map
This graph displays the number of trips taken throughout the week based on the time of the day. The chart shows cells depicting an hour-long window during a specific day. The blue represents a low number of rides, and the red shows the highest number.

Thursday from 5 p.m. to 7 p.m. sees the highest number of trips during the week.
Saturday and Sunday have the most consistent rider count throughout the day.

<img src="https://user-images.githubusercontent.com/85756203/135904355-dcd5ed85-c7df-4b64-95a2-75d469954cc7.png" height=95% width=95%>

#### Day/Week heat map by gender
This chart shows a similar breakdown as the previous heat map. Instead of measuring per hour per day, this map measures rides per day with an added filter based on gender.

The gender filter shows a similar breakdown of the most populated days and hours of the week.

This data also looks at the difference in users based on gender. From this, male riders are more prevalent than female riders.

<img src="https://user-images.githubusercontent.com/85756203/135904381-736388c0-ce31-4399-b8ea-aef83f796974.png" width=85% height=85%>

#### Trip duration per ride
The above graph displays a breakdown of how long each trip lasted. The data is filtered with hours and minutes of each recorded trip. The data only included trips of less than two hours because there was a lack of data for trips lasting longer than two hours.

The majority of trips last fewer than ten minutes—trips. There is a peak between five and six minutes with a combined 292,000 trips.

<img src="https://user-images.githubusercontent.com/85756203/135904414-55b1a735-7d8a-4190-931e-90ce36370a5b.png">

#### Trip duration per ride by gender
Similar to the previous graph, this chart communicates the total trip duration with an added gender filter. Again, the trip duration remains consistent across genders, but male riders take the most trips.

<img src="https://user-images.githubusercontent.com/85756203/135904433-cfe35c2b-bae0-4c0c-bf9f-e42f6f931320.png" width=75% height=75%>

#### Subscribers vs. Single-use riders
This graph shows how many bike users are one-time customers or subscribers. The single-use riders are blue, and subscribers are orange.

Subscribers make up most users recording trips, with 81% of trips taken by subscribers.

<img src="https://user-images.githubusercontent.com/85756203/135904461-c64475d3-66d5-4c1d-a421-ddb531531b03.png" width=60% height=75%>

#### Ride heat map based on gender/subscriber
The final graph shows the breakdown of user types filtered by weekday and gender.

The results from this graph are consistent with our previous conclusions;
- There are considerably more subscribers than users.
- Thursday sees the highest number of traffic.
- Males are taking the most trips.

<img src="https://user-images.githubusercontent.com/85756203/135904480-b74cdfc4-f897-4b11-8170-de4b56778eff.png">

## Summary

After examining the different graphs, a few recommendations can be made for future bike-sharing programs.

Bike-sharing stations need to be close enough to limit trips to less than ten minutes. There is a considerable dropoff of trips that last longer than ten minutes from the New York data. If potential riders have easy access to stations in the city, they will be more likely to use the bikes.

The stations also need to be ready for peak demand between 5 p.m. and 7 p.m., especially on Thursdays. A couple of the graphs showed that those hours saw the most trips taken. The bike-sharing program needs to be prepared to handle.

