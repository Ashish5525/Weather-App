# Weather-App
This is a simple weather application built using Swift and UIKit. It fetches and displays weather data based on the user's current location or a city name inputted by the user. The app integrates with the OpenWeatherMap API to retrieve current weather information.

## Table of Contents
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)

## Features

- Fetches weather data using the user's current location
- Fetches weather data based on a city name input
- Displays temperature, weather condition, and city name
- Uses 'CLLocationManager' for location services
- Uses 'URLSession' for network requests

## Requirements
- iOS 13.0+
- Xcode 11+
- Swift 5.0+
- An API key from [OpenWeatherMap](https://openweathermap.org)

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2. **Open the package in Xcode**:
    ```sh
    cd weather-app
    open WeatherApp.xcodeproj
    ```

3. Replace 'YOUR_API_KEY' in the 'WeatherManager' struct with your actual OpenWeatherMap API key.

4. Build and run the project on your simulator or physical device.

## Usage
### Interface

- Location Button: Fetches weather data using the user's current location.
- Search Field: Allows the user to input a city name to fetch weather data.
- Search Button: Triggers the search based on the city name input.

### Example
1. Open the App
2. Allow location access when prompted.
3. Tap the location button to get weather data for your current location.
4. Alternatively, type a city name in the search field and press the search button to get weather data for the specified city.

## Code Overview

### ViewController
- WeatherViewController: The main view controller that handles user interactions and updates the UI with weather data.
  
### Extensions
- UITextFieldDelegate: Handles text field events for searching by city name.
- WeatherManagerDelegate: Handles the weather data received from the API.
- CLLocationManagerDelegate: Handles location updates and errors.
  
### Model
- WeatherModel: Represents the weather data with properties for condition ID, city name, and temperature.
- WeatherData: Represents the structure of the JSON data received from the OpenWeatherMap API.
- Main: Represents the main section of the JSON data with the temperature.
- Weather: Represents the weather section of the JSON data with an ID and description.
  
### Networking
- WeatherManager: Handles network requests to fetch weather data from the OpenWeatherMap API and parses the JSON response.
  
### AppDelegate and SceneDelegate
- Standard setup for an iOS application, handling app lifecycle events.
  
### API Integration
The app uses the OpenWeatherMap API to fetch weather data. Make sure to sign up on their website to get an API key and replace 'YOUR_API_KEY' in the 'WeatherManager' struct.
 ```swift
 let weatherUrl = "https://api.openweathermap.org/data/2.5/weather?appid=YOUR_API_KEY&units=imperial"
 ```

### Acknowledgement
- OpenWeatherMap for providing the weather API.

