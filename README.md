# 06 Python APIs - WeatherPy & VacationPy

## Background

In this project I developed two python scripts to create a representative model of weather across world cities.

## Skills

APIs | python requests | JSON | citypy | gmaps | jupyter notebook | scatter plots | linear regression 

### WeatherPy 

A python script that uses the Citypy python library and OpenWeatherMap API to visualize the weather of randomly selected 500+ cities across the world of varying distance from the equator.

1. Randomly selects at least 500 unique (non-repeat) cities based on latitude and longitude. Note: the city data generated is based on random coordinates and different query times; as such, the outputs will not be different everytime is run.
2. Performs a weather check on each of the cities using a series of successive OpenWeatherMap API calls.
3. Includes a print log of each city as it's being processed with the city number and city name.
4. Generates a CSV of all retrieved data.
5. Generates scatter plots to explore the relationship between latidude and different weather factors including: temperature, humidity, cloudiness and wind speed on the overall data, as well as the data separated into Northern and Southern Hemisphere.

### VacationPy 

A python script that uses weather data, along with gmaps and Google Places API to plan future vacations in cities with the ideal weather.

1. Creates a heat map that displays the humidity for every city from WeatherPy.
2. Filters the city data based on defined ideal weather conditions.
3. Using Google Places API, finds the first hotel for each city located within 5000 meters of your coordinates.
4. Plots the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.
