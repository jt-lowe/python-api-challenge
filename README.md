# python-api-challenge

## Week 6 Assingment - Monash Data Course

### WeatherPy Tasks
We randomly selected 600+ cities using the Citipy API, searched each city through the OpenWeatherMap API to collect the Lattitude, Longtitude, Max Temperature, Humidity, Cloudiness, Wind Speed, Country and Date/Time for each location.

Each of these values were stored in a separate list, then combined into a dictionary which was converted into a DataFrame. This DataFrame was then written to a CSV file stored under the "weather_data.csv" file in the "WeatherPy_output" folder.

We ran the pandas .describe() function to get a quick statistical analysis of the DataFrame.

We then created multiple scatterplots, plotting Latitude against Max Temperature, Humidity, Cloudiness, and Wind Speed, and analysed each plot for any visible trends. 

Next task was splitting the data into the Northern and Southern Hemispheres, which was just by collecting all data below Lat = 0 and above Lat = 0 and placing into separate DataFrames.

We created scatterplots for the same comparisons as above, but split by hemisphere on these new DataFrames, then ran the linear regression analysis on the plots. We then analysed the regression models and further analysed the scatterplots.

### VacationPy Tasks
First step was to import the weather data from the WeatherPy output, we use this data to create a heatmap in the GMaps API, using the Latitude and Longtitude for locations and the Humidity to determine the weight of the heatmap.

Using the following conditions;
- Max Temp between 70F (21.1111C) and 80F (26.6667C) degrees
- Wind Speed is less than 10 mph
- Zero Cloudiness

we then determined the "Ideal Locations" to visit, these ideal locations were placed into a new DataFrame by comparing the original DataFrame to the above conditions.

Using the GMaps Places API, we performed a keyword search at the corresponding latitude and longtitude of each of our ideal locations, cycling through each row using the .itterows() function native to pandas, we pulled the name of the closest hotel to our ideal weather locations.

We added these hotel names back into our DataFrame and renamed it hotel_df, then reordered and dropped some columns that were no longer needed. We then added the hotels into a marker code and plotted the markers over the top of our earlier heatmap.
