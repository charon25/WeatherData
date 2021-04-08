# Weather Data
This repo contains weather data collected by a weather station built located in Strasbourg, France by myself and a friend for a class project.

## Data
The data was (and still is) collected every 10 minutes between approximately 8 am and 6 pm, sometimes earlier or later. It started on February 22<sup>th</sup>.

Every point contains 6 measurements along with a Unix timestamp. Those measurements are :
- temperature in °C,
- humidity in %,
- air pressure in hPa,
- wind speed in km/h,
- wind direction (see below for format),
- battery voltage in V.

It is presented in two formats : JSON and CSV. The JSON structure is the following :
- `units` : dictionary of measurements name and units,
- `wind_direction_dic` : dictionary of wind direction value and real direction,
- `values` : list of data point
  - [
  	- `timestamp` : int,
  	- `temperature` : float,
  	- `humidity` : int,
  	- `pressure` : float,
  	- `wind_speed` : float,
  	- `wind_direction` : int,
  	- `battery_voltage` : float,  	
  - ]
  - ...

## Usage
You are free to use this data to do whatever you want, as long as you credit this repo. No guarantee is provided about the exactitude of the data.