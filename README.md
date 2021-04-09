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

The data is available in two formats : JSON and CSV.

### JSON
The JSON structure is the following :
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

### CSV
There are 2 CSV files :
- `data_comma_period.csv` : values are comma-separated, and periods (`.`) are used as decimal separator,
- `data_semicolon_comma.csv` : values are semicolon-separated, and commas (`,`) are used as decimal separator.

On the 8<sup>th</sup> of April, the set contains 2972 data points.

### Wind direction
The wind direction is an integer between 0 and 16 (inclusive), each one indicating a specific direction.
| Integer | Direction |
| ------- | --------- |
| 0 | West |
| 1 | West-North-West |
| 2 | North-West |
| 3 | North-North-West |
| 4 | North |
| 5 | North-North-East |
| 6 | North-East |
| 7 | East-North-East |
| 8 | East |
| 9 | East-South-East |
| 10 | South-East |
| 11 | South-South-East |
| 12 | South |
| 13 | South-South-West |
| 14 | South-West |
| 15 | West-South-West |
| 16 | Invalid/Error |

## Usage
You are free to use this data to do whatever you want, as long as you credit this repo. No guarantee is provided about the exactitude of the data.