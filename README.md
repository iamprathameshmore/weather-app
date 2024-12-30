# Weather App

A Flutter-based Weather App that provides real-time weather updates using an API. The app refreshes data every 30 minutes, ensuring users receive the most up-to-date information about their location's weather.

## Features

- Fetches real-time weather data from a public API
- Automatically updates weather information every 30 minutes
- User-friendly interface
- Displays temperature, humidity, wind speed, and weather condition
- Location-based weather updates

## Screenshots

(Add screenshots of your app here)

## Installation

### Prerequisites

- Flutter installed on your system. [Install Flutter](https://flutter.dev/docs/get-started/install)
- An API key from a weather service provider, such as [OpenWeatherMap](https://openweathermap.org/).

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/weather-app.git
   cd weather-app
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Configure your API key:
   - Open the `lib/services/api_service.dart` file.
   - Replace `YOUR_API_KEY` with your API key.

4. Run the app:
   ```bash
   flutter run
   ```

## File Structure

```
lib/
├── main.dart                # Entry point of the app
├── services/
│   └── api_service.dart     # Handles API calls
├── models/
│   └── weather_model.dart   # Data model for weather information
├── screens/
│   └── home_screen.dart     # Main screen displaying weather details
├── widgets/
│   └── weather_card.dart    # Custom widget for displaying weather information
└── utils/
    └── constants.dart       # Stores constants like API URL
```

## API Integration

The app uses the [OpenWeatherMap API](https://openweathermap.org/api) to fetch weather data. Ensure you have a valid API key to use the service.

### Sample API Request

```bash
https://api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}
```

### Automatic Updates

The app uses a `Timer` to refresh weather data every 30 minutes:

```dart
Timer.periodic(Duration(minutes: 30), (timer) {
  fetchWeatherData();
});
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes with clear messages.
4. Push your changes to the branch.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For inquiries or support, please reach out:

- Email: iamprathameshmore07@example.com
- LinkedIn: [Your Name](https://linkedin.com/in/iamprathameshmore)

---

Happy Coding! 🌦️
