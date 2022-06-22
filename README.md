# 06 Python APIs - WeatherPy & VacationPy

## Background

In this project I developed two python scripts to create a representative model of weather across world cities.

## Skills

APIs | python requests | JSON | citypy | gmaps | jupyter notebook | numpy | pandas | matplotlib | scatter plots | linear regression 

## WeatherPy 

A python script that uses the Citypy python library and OpenWeatherMap API to visualize the weather of randomly selected 500+ cities across the world of varying distance from the equator.

1. Randomly selects at least 500 unique (non-repeat) cities based on latitude and longitude. Note: the city data generated is based on random coordinates and different query times; as such, the outputs will not be different everytime is run.
2. Performs a weather check on each of the cities using a series of successive OpenWeatherMap API calls.
3. Includes a print log of each city as it's being processed with the city number and city name.
4. Generates a CSV of all retrieved data.
5. Generates scatter plots to explore the relationship between latidude and different weather factors including: temperature, humidity, cloudiness and wind speed on the overall data, as well as the data separated into Northern and Southern Hemisphere.

<img width="707" alt="Screen Shot 2022-06-22 at 11 49 36 am" src="https://user-images.githubusercontent.com/77761497/174926381-4b0158d4-c1b4-498f-8154-ed9ff7d85e60.png">


### Conclusions

The random selection of the 541 cities analysed are evenly distributed througout a latitute range (-60, 80), composed of 382 cities in the northern hemisphere and 159 cities in the southern hemisphere. These numbers indicate that our sample could be slightly skewed, oversampling the northern hemisphere, while not providing sufficient data on the southern hemisphere, specially cities concerning latitutes in the range (-90, -60).

<img width="403" alt="Screen Shot 2022-06-22 at 12 04 12 pm" src="https://user-images.githubusercontent.com/77761497/174927674-d36ec5fc-6fd6-470b-bdce-6d9d9d75aee8.png">

In the Lat vs Max Temp plots, it can be observed that the cities closest to the equator, present the highest maximum temperatures. This is further supported with the linear regression of lat vs temp when dividing the data in northern and southern hemispheres. The latitude and temperature of cities in the northern hemisphere present a negative correlation (r-square = -0.89), in which the maximum temperature drops as we move away from the equator into higher latitudes. Complementary, the latitude and temperature of cities in the southern hemisphere present a positive correlation (r-square = 0.57), in which the maximum temperature increases as we move away from more negative latitudes towards latitude 0 in the equator. The r-square value in the southern hemisphere is lower than expected, however this could be due to insuficient data sampling and could be improved if more cities between latitude (-90, -60) are included.

The rest of parameters analysed (humidity, cloudiness and wind speed) did not present a clear relationship with latitude. Overall it could be observed that the points where spread inconsistently throughout the latitude range examined. Moreover, all r-square parameters when calculating correlations in the northern and southern cities were closer to 0 (from -0.30 to 0.34), indicating that despite of some trends (increased humidity and decreased wind speed towards the equator in cities of the southern hemisphere), there is no strong relationship between the variables.

## VacationPy 

A python script that uses weather data, along with gmaps and Google Places API to plan future vacations in cities with the ideal weather.

1. Creates a heat map that displays the humidity for every city from WeatherPy.
2. Filters the city data based on defined ideal weather conditions.
3. Using Google Places API, finds the first hotel for each city located within 5000 meters of your coordinates.
4. Plots the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

![hotel_map](https://user-images.githubusercontent.com/77761497/174927485-f42db30d-405e-48d3-90de-31bcd8d147b5.png)

