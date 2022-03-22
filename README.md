# PlanMyTrip Application
### This analysis develops code to retrieve weather data paired with randomly generated geographical coordinates to offer clients potential destinations for their vacation plans based on weather preferences.

### Retrieve Weather Data
The "Weather_Database_ipynb.ipynb" file in this repository will acquire 2,000 randomly generated latitude and longitude combinations to be set as posible destinations for future travelers. Of these 2,000 coordinates, roughly 35% will be both on land and close to a hotel to be recommended. Therefor, the actual options for travelers is roughly 700 hotels which will sufice. To determine which coordinates correspond to a hotel, a google api key is used to call gmaps and determine which coordinates will be useful going forward. This data set is then saved to a csv file for future use to avoid making further api calls.

### Create a Customer Travel Destinations Map

The creation of the "Customer Travel Destinations Map" is the purpose of the file "Vacation_Search.ipynb". It first uploades the csv file that was saved in the above section, then requests input by the user (traveler) for temperature parameters for their travel preferences. They are guided to input their desired  minimum and maximum temperatures for their vacation. Once inputed, the code filters through the hotel dataset for only the hotels that are in climates that exclusively meet the criteria of the user. A new data set is created, cleaned and then used to generate a map that shows all the potential locations for the vacation.

![WeatherPy_vacation_map](https://user-images.githubusercontent.com/95305584/159542902-0fff8e2d-adda-40df-96d7-9bf745a4de84.png)


### Create a Travel Itinerary Map

Now equiped with sufficient hotels across the world, 4 hotels in relatively close proximity were chosen as a potential travel itinerary for the user. The map below shows markers for each hotel, a pop-up info box for each location as well as direction from one hotel to next that returns to the initial hotel. At this point, the user has all the information they need to start planning their trip!
![WeatherPy_vacation_map_directions](https://user-images.githubusercontent.com/95305584/159545161-e6148de4-4e20-405c-8adf-2bd25ce144c8.png)


