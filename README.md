# Location Search Microservice:

## How to Request Data:
Send a GET Request to:
http://<server-address>:5001/location-search?q=<city name>[, state code]

EXAMPLE:
http://localhost:5001/location-search?q=Gretna

## How to Receive Data:
This service responds with JSON data:
```json
[
  {
    "name": "Gretna",
    "state": "LA",
    "country": "US",
    "lat": 29.9167,
    "lon": -90.05,
    "weather": {
      "description": "overcast clouds",
      "temperature": 79.03,
      "feels_like": 79.03,
      "humidity": 63,
      "wind_speed": 5.75
    }
  }
]
```
## Steps:
1. Open app.py and RUN.
2. Open test_location_search.py, and RUN.
3. In the terminal, enter the city name you would like to search, following the prompt:

Enter a city name to search:

Example: Gretna

It will pull up something like this:

```
Enter a city name to search: Gretna
Location: Gretna, Louisiana, US
  Coordinates: (29.9146493, -90.0539604)
  Weather: scattered clouds
  Temperature: 79.21 °F
  Feels Like: 79.21 °F
  Humidity: 62%
  Wind Speed: 3.44 mph
----------------------------------------
Location: Gretna, Florida, US
  Coordinates: (30.6171378, -84.6599145)
  Weather: clear sky
  Temperature: 80.13 °F
  Feels Like: 83.68 °F
  Humidity: 74%
  Wind Speed: 3.44 mph
----------------------------------------
Location: Gretna, Virginia, US
  Coordinates: (36.9528412, -79.3602341)
  Weather: broken clouds
  Temperature: 72.34 °F
  Feels Like: 73.27 °F
  Humidity: 85%
  Wind Speed: 7.61 mph
----------------------------------------
Location: Gretna, Nebraska, US
  Coordinates: (41.1469269, -96.2390053)
  Weather: clear sky
  Temperature: 64.13 °F
  Feels Like: 62.98 °F
  Humidity: 58%
  Wind Speed: 5.75 mph
----------------------------------------
Location: Gretna, Scotland, GB
  Coordinates: (54.9953097, -3.0669404)
  Weather: broken clouds
  Temperature: 48.96 °F
  Feels Like: 44.37 °F
  Humidity: 78%
  Wind Speed: 11.14 mph
----------------------------------------

Process finished with exit code 0
```
Important Detail to NOTE:

When running app.py, you MUST get an API KEY from the OpenWeatherMap website. This is where the json data comes from. Here is how to do that:

1. Go to: https://home.openweathermap.org/users/sign_up

2. Create an account, then log in with your credentials.

3. Navigate to the API Keys section.

4. Click "Create key" or use the default key provided for you.

5. Copy the key, and paste it into this line between the dashes:
```
OWM_API_KEY = ''  # Replace with your actual API key
```

After that, you're set to follow the steps as normal. Remember to run app.py, then test_location_search.py, and follow the prompts in the terminal.

## UML Sequence Diagram:

![Screenshot 2025-05-21 at 7.43.35 PM.png](..%2F..%2F..%2F..%2Fvar%2Ffolders%2Ffl%2F_xw5rz3x69n7wsdpjn2d1d7c0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_2aq3u3%2FScreenshot%202025-05-21%20at%207.43.35%20PM.png)
