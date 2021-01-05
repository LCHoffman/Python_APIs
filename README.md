# Python APIs Homework

# Background
Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"
Now, we know what you may be thinking: "Duh. It gets hotter..."
But, if pressed, how would you prove it?

# WeatherPy
### Requirements
In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

Your final notebook must:

 * Randomly select at least 500 unique (non-repeat) cities based on latitude and longitude.
 * Perform a weather check on each of the cities using a series of successive API calls.
 * Include a print log of each city as it's being processed with the city number and city name.
 * Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Notes 

 * WeatherPy builds a csv file of cities with weather data from Open Weather.  These cities were selected from a randomly generated list of latitude and longitude pairs.  The 1500 random lat/long pairs resulted in 601 cities.  
 * When an Open Weather API was run, 548 cities with weather data remained.  This data was saved to cities.csv in the output_data folder.
 * The open weather data was then used to graph the latitude versus temperature, humidity, wind speed and cloudiness in separate scatter plots.  All of these graphs were saved as PNG files in the output_data folder.

# VacationPy
### Requirements
Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.  Create a heat map that displays the humidity for every city from the part I of the homework.  Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.  Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

### Notes
 * VacationPy used the 548 city csv file to create a heatmap using Google maps.  The heatmap indicated the humidity of each city.
 * The city csv file was converted to a dataframe and then the list of vacation cities was narrowed based on ideal weather conditions.  The remaining cities (10) were: between 70 and 80 degrees F, had a wind speed less than 10mph and 0% cloudiness.  A blank column "Hotel Name" was added to this 10 row dataframe.
 * This dataframe was used in a Google API pull for hotels within 5000 meters of the city's coordinates.  The first hotel returned was added to the dataframe in the "Hotel Name" column.
 * A marker layer was created that dropped markers on each city with an info-box.  The info-boxes included the name of the Hotel, the City and the Country.  This marker layer was added over the humidity heatmap.
