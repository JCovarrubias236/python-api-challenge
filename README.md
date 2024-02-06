# Python API Challenge
This repository will be used for the Module 6 Python API challenge.

## Description

The main purpose of this project was to answer the fundamental question of "What is the weather like as we approach the equator?" As we all know, the weather tends to get hotter as you get closer to the equator, but I wanted to provide an in-depth analysis of what other weather factors change as well. This project consists of two main Python Jupyter files which are called "WeatherPy.ipynb" and "VacationPy.ipynb". 

The Weather Jupyter file uses the OpenWeatherMap API to search for current weather data for 573 predetermined cities. For each city, I grabbed the latitude, longitude, max temp, humidity, cloudiness, wind speed, country, and date of retrieval to help with my analysis. I used scatter plots to determine the relationships between latitude and temperature, latitude and humidity, latitude and cloudiness, and latitude and wind speed. Next, I wanted to make a comparison between the northern and southern hemispheres so I filtered the city_data_df data frame by the latitude field accordingly. With the data split between the northern and southern hemispheres, I created a linear regression plot for each of the aforementioned relationships and also determined the correlation coefficient.

In the Vacation Jupyter file, I took it a step further to visualize all the cities from the city_data_df data frame on the world map. I then created my "ideal" weather conditions for vacation and used the Geoapify API to determine the first hotel located within 10,000 meters of the ideal weather city coordinates. Lastly, I visualized the cities that fit my ideal weather conditions and the closest hotel to the coordinates provided.

## Installation

Feel free to download the CSV and the Python Jupyter Notebook files I provided to look over and run the Python script files.

Input the below modules for the WeatherPy.ipynb script file to run properly

```python
# Dependencies and Setup
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import requests
import time
import json
import scipy.stats as stats
from scipy.stats import linregress

# Import the OpenWeatherMap API key
from api_keys1 import weather_api_key

# Import citipy to determine the cities based on latitude and longitude
from citipy import citipy
```

Input the below modules for the VacationPy.ipynb script file to run properly

```python
# Dependencies and Setup
import hvplot.pandas
import pandas as pd
import requests

# Import API key
from api_keys1 import geoapify_key

# Turn off warning messages
import warnings
warnings.filterwarnings("ignore")
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change/recommend.

## Authors and Acknowledgement

I solely worked on this project, however, I did utilize the help of my TAs during office hours to complete some tasks that either I needed a refresher on or I didn't know how to resolve certain bugs I was receiving. They helped me with the VacationPy Jupyter script to display the world map plot of the cities as I was inputting the longitude and latitude coordinates incorrectly so that was resulting in a plot frame size error. I also received help with the Geoapify API search for hotels near the ideal weather city coordinates as I could not find a single hotel at first so it was just a fault in how I wrote my code.
