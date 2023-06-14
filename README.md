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
### Part-1: WeatherPY
For this portion of the challenge, we must create a Python script to visualize the weather of over 500 cities of varying distances from the equator. We will be using the citipy Python library and the OpenWeatherMap API links to external websites. We will use WeatherPy.ipynb from the starter code, in a Jupyter notebook. The starter code acts as a guide through the process, providing only what the output _should_ come to be. __Note:__ as mentioned later in the instructions, the city data we generate is based on random coordinates and different query times, so our outputs will not be an exact match to the provided starter notebook. 

#### Requirement-1
To meet first requirement, we must use the information acquired from OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code.

Create charts:
* Latitude vs. Temperature

* Latitude vs. Humidity

* Latitude vs. Cloudiness

* Latitude vs. Wind Speed

#### Requirement-2
Create charts:
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
Describe task notes
Create Maps:
* Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.

__city data map example__

![city_data_df](https://static.bc-edx.com/data/dl-1-2/m6/lms/img/humidity_map.png)

* Create a for hotel_df

__hotel map example__

![hotel_df](https://static.bc-edx.com/data/dl-1-2/m6/lms/img/hotel_map.png)

include png or links to png from readme to give examples

explain changes I made & why: color / metrics

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
(where possible will provide link to website)
* citypy library
* OpenWeatherMap documentation & API
* geoapify documentation & API
* pandas documentation
* matplotlib documentation
* hvplot documentation
* scipy.stats documentation
* ArcGIS geographic coordinate system documentation

This Challenge provided many opportunities to try and test new ideas.
