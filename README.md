# python-api-challenge
UNC DataBootCamp API module challenge

## Challenge Descricription
### Background
> Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

> Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

***from the UNC Bootcamp instructions for this challenge***

## Deliverables
This challenge is broken down into two parts, WeatherPY then VacationPY.

We will be working with Jupyter notebooks, using APIs from various sites to achieve this.

We will be using OpenWeatherMap for the API key as well as API call formatting examples.

The URL I generate for the city_day variable uses "units=imperial" because this would make the output measurements easier to interpret. _Conversions applied where needed._

I am color-blind but I am well aware the importance color can bring to a audience. That said I could not tell what colors the plots were meant to be for the scatter plot charts so I used documentation from matplotlib.org color tables for color IDs. For the linear regression scatter plots my goal was to choose colors that were different from one another.

### Part-1: WeatherPY
For this portion of the challenge, we must create a Python script to visualize the weather of over 500 cities of varying distances from the equator. We will be using the citipy Python library and the OpenWeatherMap API links to external websites. We will use WeatherPy.ipynb from the starter code, in a Jupyter notebook using a modified URL we generate along with the other pieces of code. The starter code acts as a guide through the process, providing only what the output _should_ come to be. __Note:__ as mentioned later in the instructions, the city data we generate is based on random coordinates and different query times, so our outputs will not be an exact match to the provided starter notebook. We then convert this city data into a pandas DataFrame,  city_data_df , which will be used to plot the charts in __Requirement-1__ and __Requirement-2__ , we will also save this DataFrame over cities.csv in the output_data folder to be used later. 

#### Requirement-1
To meet first requirement, we are to create plots that display the relationship between different weather variables and _Latitude_ . We will use city_data_df to do this, along with the strftime function to convert the date from Unix to a more legible (Year-Month-Day) format in the title. We will also, export these charts as Fig1-4.png to the output_data folder, overwriting the original files.

The Scatter Plots will showcase the following relationships:
* Latitude vs. Temperature
* Latitude vs. Humidity
* Latitude vs. Cloudiness
* Latitude vs. Wind Speed

#### Requirement-2
To meet the second requirement, we are to compute the linear regression for each relationship in both Northern (Latitude  >=  0) and Southern (Latitude < 0) Hemispheres. Along with this, we were tasked to define a function in order to generate the linear regression plots. In this case I chose to define two functions, one for both the Northern Hemisphere and Southern Hemisphere, this way the outputs could be displayed in different formatting for when/if the data is compared side by side. Along with the linear regression line, these scatter plots also need to include each models's formula (y = _m_ x +  _b_ ) and the r value. I also chose to export these charts as linreg1-8.png to the output_data folder to provide quicker access if ever needed.

The Linear Regression Scatter Plots will showcase the following relationships:
* Northern Hemisphere: Temperature vs. Latitude
* Southern Hemisphere: Temperature vs. Latitude
* Northern Hemisphere: Humidity vs. Latitude
* Southern Hemisphere: Humidity vs. Latitude
* Northern Hemisphere: Cloudiness vs. Latitude
* Southern Hemisphere: Cloudiness vs. Latitude
* Northern Hemisphere: Wind Speed vs. Latitude
* Southern Hemisphere: Wind Speed vs. Latitude

__linear regression chart example__

 ![lin-regress-plot](https://static.bc-edx.com/data/dl-1-2/m6/lms/img/linear-regression-plot.png)

### Part-2: VacationPY
> In this deliverable, you'll use your weather data skills to plan future vacations.

Use the cities.csv created in __Part-1: WeatherPy__ to provide the initial DataFrame ,city_data_df, for this portion of the challenge. From this DataFrame we create the first map and the remainder of the challenge will be completed in the following __Steps__ :

1. Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image  _(see example)_ . The size of the point should be the humidity in each city.

__city data map example__

![city_data_df](https://static.bc-edx.com/data/dl-1-2/m6/lms/img/humidity_map.png)

2. Narrow down the city_data_df DataFrame to find "our" ideal weather condition and save this as ideal_city_df . I chose to use the suggested conditions from the example, however my units were already Imperial, so I converted to the units to Imperial and wrote the code accordingly:
 * Max temperature  <  81 degrees but  >  70
 * Wind speed  <  10 
 * Zero cloudiness
3. Create a new DataFrame called hotel_df using a copy of  ideal_city_df , only using and reording the following columns: city, country, coordinates, and humidity. After this, add a Hotel Name column to the DataFrame.
4. For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates. The search and output here will populate the Hotel Name column in hotel_df .
5. Create a  _final_  map for  hotel_df . We are first going to clean up the data by only displaying results from the previous step that did NOT say "No hotel found" as new (final) DataFrame called  hotel_found_df . Add the hotel name and the country as additional information in the hover message for each city on the map.

__hotel map example__

![hotel_df](https://static.bc-edx.com/data/dl-1-2/m6/lms/img/hotel_map.png)


## Resources
### Bootcamp References
Module 6 Instructions

starter_code
* WeatherPy.ipynb
* VacationPY.ipynb

Example Data:

output_data _(original folder)_
* cities.csv
* Fig1.png
* Fig2.png
* Fig3.png
* Fig4.png

***Special Thanks:***
* Jamie Miller
* Mounika Mamindla
* Lisa Shemanciik

### External References
_(where possible will provide link to website)_
* citypy library
* OpenWeatherMap documentation & API
* geoapify documentation & API
* pandas documentation
* matplotlib documentation
* hvplot documentation
* scipy.stats documentation
* ArcGIS geographic coordinate system documentation

This Challenge provided many opportunities to try and test new ideas.
