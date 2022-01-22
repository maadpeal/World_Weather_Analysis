# World_Weather_Analysis

### Purpose
    - From a random set of data, we seek to filter the possible destination cities that a user could 
    choose based on maximum and minimum temperature preferences.

### Steps of Analysis
    - From a random set of 2000 latitudes and longitudes, the closest city is searched through the 
    citipy library, of which only 750 turn out with results, the rest are estimated to be coordinates 
    in inhospitable places or the sea.
    - After this, a call is made to the api of http://api.openweathermap.org, to obtain the climate 
    of the cities previously obtained, only 675 had information available, the rest are deleted and 
    the results are saved in a csv file.
    - Based on the information obtained previously, the user is asked what maximum and minimum 
    temperature he would like for his trip, based on this the cities of the data set are filtered.
    - The cities that still remain in the dataframe are searched through the google api 
    (https://maps.googleapis.com/maps/api/place/nearbysearch/json), in this search there will be 
    cities that will not have nearby hotels, which are removed from the options.
    - From the result we proceed to graph with gmaps (image A-1).

![](https://github.com/maadpeal/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)  

(image A-1)

    - Finally, we do the exercise of being the user, we decide from the remaining countries to choose 
    4 cities in the same country and create the route that we will possibly visit, in this case 
    4 cities in South Africa were chosen (image B-1, B-2).
    
![](https://github.com/maadpeal/World_Weather_Analysis/blob/main/Vacation_Itinerary/context.png)

(image B-1)
    
![](https://github.com/maadpeal/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)

(image B-2)
