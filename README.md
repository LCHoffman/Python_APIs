# Python_APIs

# WeatherPy

WeatherPy builds a csv file of cities with weather data from Open Weather.  These cities were selected from a randomly generated list of latitude and longitude pairs.  The 1500 random lat/long pairs resulted in 601 cities.  

When an Open Weather API was run, 548 cities with weather data remained.  This data was saved to cities.csv in the output_data folder.

The open weather data was then used to graph the latitude versus temperature, humidity, wind speed and cloudiness in separate scatter plots.  All of these graphs were saved as PNG files in the output_data folder.

# VacationPy

VacationPy used the 548 city csv file to create a heatmap using Google maps.  The heatmap indicated the humidity of each city.

The city csv file was converted to a dataframe and then the list of vacation cities was narrowed based on ideal weather conditions.  The remaining cities (10) were: between 70 and 80 degrees F, had a wind speed less than 10mph and 0% cloudiness.  A blank column "Hotel Name" was added to this 10 row dataframe.

This dataframe was used in a Google API pull for hotels within 5000 meters of the city's coordinates.  The first hotel returned was added to the dataframe in the "Hotel Name" column.

A marker layer was created that dropped markers on each city with an info-box.  The info-boxes included the name of the Hotel, the City and the Country.  This marker layer was added over the humidity heatmap.