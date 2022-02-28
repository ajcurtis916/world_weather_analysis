
# World Weather Analysis

## *Analyze weather patterns and retrieve city, lodging and transportation data using APIs*
---


### Project Overview
Our first task was to define what a client meant as "ideal" travel.  Over the course of the conversation, we narrowed that down to hotels that were within a given range of latitude and longitude of their preferred destination, and provided the right kind of weather for the client.   We first collected and analyzed weather data across cities worldwide, then recommended ideal hotels based on clients' weather preferences.  We added the "Current Weather" description in this portion of the analysis, as part of the included deliverables.  Our analysis was split into three main parts, or stages. 

1. Using the NumPy module we generated approximately 1,500 to 2,000 random latitudes and longitudes, then used the citipy module to list the nearest city to the latitudes and longitudes.  We folowed up by using the OpenWeatherMap API to request the current weather data from each unique city in our list, parsed the JSON data from the API request, added the information to a DataFrame and exported the data to a CSV.

2. Using the DataFrame from the first part of the analysis, we created a user input feature to request the optimal minimum and maximum temperatures for travel, and created a function to return only the "preferred" locations and their assosicated weather data to a new DataFrame and exported to a CSV.  We called upon the Google Maps Nearby Search API to add the closest hotels to the latitudes and longitudes compiled into our preferred cities DataFrame, then created a Google Maps figure noting all requested information using a map pop-up marker layer. 

3. In our third stage of the analysis, we imported the data from the previous stage and created a Google Maps figure displaying the route from start point to endpoint between four (4) of the preferred cities in one country.  This was meant to exemplify a potential "trip" based on the client's preferred weather parameters for travel, utilizing the Google Maps Directions Layer.  In order to display the correct markers, we had to first ultilize the to_numpy function to convert the latitudes into pairs of tuples.  To follow up, we added the same style of markers that we utilized in stage two to display the hotel name, location and weather data for each of the four (4) selected cities. 
