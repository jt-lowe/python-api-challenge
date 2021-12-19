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
