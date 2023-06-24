# Weather Forecasting Tool

The Weather Forecasting Tool is a command line tool that accepts a city's name as input and returns the current weather forecast. It leverages the OpenWeatherMap API to fetch weather data and parse it using Python.

## Usage

To use the Weather Forecasting Tool, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/Fastest-Coder-First/Weather_Forecast_Teampravi.git

2. Obtain an API key from OpenWeatherMap by signing up at https://openweathermap.org.

3. Create a secrets.ini file in the project directory and add the following content:
    
    [openweather]
    api_key = your_api_key

4.  Run the Weather Forecasting Tool:

    python weather_forecast.py city_name [-i]
    
    Replace city_name with the name of the city for which you want to fetch the weather forecast. The optional -i flag can be used to display the temperature in imperial units (Fahrenheit).

5. Architecture Overview

    The architecture of the Weather Forecasting Tool follows a simple flow:
    
        i.      Command Line Interface (CLI): The user interacts with the tool through the command line by providing the city name and optional flags for imperial units.
    
        ii.     Command Line Argument Parsing: The argparse module is used to parse the command line arguments provided by the user, including the city name and imperial unit flag.
    
        iii.    API Request Building: The build_weather_query function constructs the URL for an API request to the OpenWeatherMap Weather API. It utilizes the provided city name and imperial unit flag to create the query URL.

        iv.     API Request Execution: The get_weather_data function makes an HTTP request to the OpenWeatherMap API using the constructed URL. It handles potential errors, such as unauthorized access or not found responses.

        v.      API Response Parsing: The received data from the API response is parsed using the json module to extract the relevant weather information. The parsed data is returned as a Python object.

        vi.     Weather Information Display: The display_weather_info function takes the parsed weather data and displays the formatted weather information on the command line. It includes the city name, weather symbol, weather description, and temperature in the desired unit (imperial or metric).

6.GitHub Copilot Usage

    GitHub Copilot can assist in various scenarios throughout the codebase::

        i.     API Request URL Building: Copilot can provide suggestions in constructing the API request URL based on the city name and imperial unit flag, ensuring the correct formatting of the URL parameters.

        ii.    Configuration File Parsing: Copilot can assist in file handling and parsing the configuration file (secrets.ini) to retrieve the API key, suggesting code snippets for reading and extracting the key from the file.
        
        iii.   Error Handling and Exception Handling: Copilot can provide suggestions for error handling and exception handling in the get_weather_data function, helping to handle different HTTP error codes and displaying appropriate error messages to the user.
        
        iv.    Weather Information Formatting: Copilot can suggest improvements in formatting and displaying the weather information, such as aligning the output and improving the visual representation of weather symbols and descriptions.
 
        v.     Variable Naming and Code Organization: Copilot can provide suggestions for variable naming and code organization, helping to improve the readability and maintainability of the codebase.
      
    Please note that while GitHub Copilot can provide helpful suggestions, it's important to review and validate the generated code to ensure correctness and adherence to specific requirements.

7. Images/Videos of Working Solution
    
    Included relevant image showcasing working solution. This include screenshots of the tool in action.
