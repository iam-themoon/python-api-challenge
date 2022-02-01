# python-api-challenge
Repository for HW 6 - APIs

This assignment was divided into two parts - the WeatherPy and VacationPy challenges. 

### WeatherPy 

For the WeatherPy portion, it starts with my top three observations from the data analysis.
* In the code portion, we do our imports, including our API keys and the CSV file (cities.csv). We also pre-determine the latitude and longitude ranges used.
* We accrue a list of lat/lng pairs for our cities, then use our OpenWeather API to create a table full of data for all those lat/lng pairs
    - This query includes a sleep clause that pauses for 60 seconds after every 50 cities, to avoid any errors
* Next, we check to see if there are any humidity readings over 100% and create a dataframe that excludes these
* Then we move into plotting the data
    - Lat v. Temp scatter plot
    - Lat v. Humidity
    - Lat v. Cloudiness
    - Lat v. Wind Speed
* Then we create a linear regression that we can apply to each of these plots
    - But before we do that, we take it a step further by creating dataframes of northern hemisphere and southern hemisphere data
    - This way, we can create graphs of NH and SH specific data and put our regressions on those
    - Under each plot is a sentence explaining the correlation in the data
    
### VacationPy

For the VacationPy portion:
* We do our imports, including the same CSV
* First, we configure a heatmap of the humidity for the data
* Then we narrow the data down to "ideal weather" - my ideal is over 60 and less than 70, with less than 10mph wind and no clouds
    - We also drop any empty/null values and reset our index to start at 0
* From this narrowed data we add a "Hotel Name" column to populate next
* We query the Google API and find the hotels nearest to our ideal weather cities
    - These hotels are added to the narrowed dataframe
    - Using this dataframe, we create another map with markers, showing the hotels 
    
And that's it! Pretty straight forward. Thanks for reading :)