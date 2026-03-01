# ☀️ Weather App

A modern, responsive web application that provides real-time weather information. Get current weather conditions for your location or search for any city worldwide using the OpenWeatherMap API.

![Weather App](./assets/weather-app-banner.png)

## ✨ Features

- **Your Weather**: Get real-time weather for your current location with just one click
- **Search Weather**: Search weather information for any city in the world
- **Real-time Data**: Powered by OpenWeatherMap API
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Weather Details**: View comprehensive weather information including:
  - Current temperature (in Celsius)
  - Weather description and conditions
  - Wind speed
  - Humidity level
  - Cloud coverage
  - Country flag for the location

- **Session Caching**: Coordinates are cached in session storage for improved performance
- **Modern UI**: Clean, intuitive interface with smooth transitions and loading animations

## 🚀 Live Demo

[View Live Demo](https://yourname.github.io/Weather-App)

## 🛠️ Technologies Used

- **HTML5** - Semantic markup and structure
- **CSS3** - Modern styling with Flexbox and Gradients
- **JavaScript (ES6+)** - Dynamic functionality and API integration
- **OpenWeatherMap API** - Real-time weather data
- **Geolocation API** - User location detection
- **Google Fonts** - Merriweather Sans typography

## 📋 Prerequisites

- Modern web browser with JavaScript enabled
- Internet connection
- OpenWeatherMap API key (free tier available)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Weather-App.git
   cd Weather-App
   ```

2. **Get an API Key**
   - Visit [OpenWeatherMap](https://openweathermap.org/api)
   - Sign up for a free account
   - Generate an API key

3. **Update API Key**
   - Open `index.js`
   - Replace the `API_KEY` variable with your OpenWeatherMap API key:
     ```javascript
     const API_KEY = "your_api_key_here";
     ```

4. **Run the application**
   - Open `index.html` in your web browser
   - Or use a local server:
     ```bash
     # Using Python (Python 3)
     python -m http.server 5500
     
     # Using Node.js with http-server
     npx http-server
     ```
   - Navigate to `http://localhost:5500` in your browser

## 📁 Project Structure

```
Weather-App/
├── index.html          # Main HTML file
├── index.css           # Styling
├── index.js            # JavaScript functionality
├── assets/             # Images and icons
│   ├── cloud.png
│   ├── humidity.png
│   ├── loading.gif
│   ├── location.png
│   ├── search.png
│   ├── wind.png
│   ├── favicon.ico
│   └── not-found.png
└── README.md          # Documentation
```

## 🎯 How to Use

### View Your Current Weather
1. Click on the **"Your Weather"** tab
2. Click the **"Grant Access"** button to allow location access
3. Your current weather will be displayed automatically

### Search for Weather
1. Click on the **"Search Weather"** tab
2. Enter a city name in the search box
3. Press Enter or click the search button
4. Weather information for that city will be displayed

## 🌐 API Integration

This app uses the **OpenWeatherMap API** for weather data:

- **Current Weather Endpoint**: `/data/2.5/weather`
- **Parameters Used**:
  - `lat`: Latitude (for location-based weather)
  - `lon`: Longitude (for location-based weather)
  - `q`: City name (for search-based weather)
  - `appid`: API key
  - `units`: Metric (for Celsius)

Response includes: temperature, description, weather conditions, wind speed, humidity, and cloud coverage.

## 🎨 Design Highlights

- **Color Scheme**: Professional blue gradient background with light accent colors
- **Typography**: Google Fonts Merriweather Sans for elegant readability
- **UI Components**:
  - Interactive tabs for navigation
  - Loading animation during API calls
  - Parameter cards for weather details
  - Country flags for location identification
  - Weather condition icons

## 🔒 Browser Compatibility

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Mobile browsers: ✅ Fully responsive

## 🚨 Troubleshooting

### Issue: "Grant Access" button doesn't work
- **Solution**: Ensure HTTPS is enabled (required for geolocation on non-localhost)
- Check browser geolocation permissions settings

### Issue: Weather data not loading
- **Solution**: Verify your API key is correct
- Check internet connection
- Ensure API rate limit hasn't been exceeded

### Issue: City not found
- **Solution**: Try searching with the exact city name
- Some cities may require country code (e.g., "London, UK")

## 📝 Code Highlights

### Geolocation Integration
```javascript
function getLocation() {
    if(navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition);
    }
}
```

### API Call Example
```javascript
const response = await fetch(
    `https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${API_KEY}&units=metric`
);
const data = await response.json();
```

### Session Storage for Performance
```javascript
sessionStorage.setItem("user-coordinates", JSON.stringify(userCoordinates));
```

## 🎓 Learning Resources

- [OpenWeatherMap API Documentation](https://openweathermap.org/api)
- [Geolocation API - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)
- [Fetch API - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📚 Future Enhancements

- [ ] 5-day and 10-day forecast
- [ ] Multiple weather alerts
- [ ] Dark/Light theme toggle
- [ ] Weather history
- [ ] Favorites/Bookmarked cities
- [ ] Unit toggle (Celsius/Fahrenheit)
- [ ] Air quality index
- [ ] Sunrise/Sunset times
- [ ] UV index
- [ ] PWA support for offline functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

Your Name - [GitHub Profile](https://github.com/yourusername)

## 🙏 Acknowledgments

- OpenWeatherMap for the comprehensive weather API
- Flagcdn for country flags
- Google Fonts for typography
- The amazing open-source community

## 📞 Support

If you have any questions, feel free to:
- Open an issue on GitHub
- Create a discussion
- Contact me directly

---

**Made with ❤️ and JavaScript**
