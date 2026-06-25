# Weather Dashboard

A modern, responsive weather dashboard that fetches real-time weather data from a public API and displays it in an intuitive interface.

## Features

- ✅ Real-time weather data from OpenWeatherMap API
- ✅ Current weather conditions
- ✅ 5-day forecast
- ✅ Search by city name
- ✅ Geolocation support
- ✅ Responsive design (mobile, tablet, desktop)
- ✅ Temperature unit toggle (°C / °F)
- ✅ Weather alerts
- ✅ Local storage for saved locations

## Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla JS)
- **API:** OpenWeatherMap Free API
- **Styling:** Bootstrap 5 / Custom CSS
- **Storage:** LocalStorage API

## Getting Started

### Prerequisites

- Modern web browser
- OpenWeatherMap API key (free tier available)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/sunsadika-jpg/windows10.git
cd windows10
```

2. Get a free API key from [OpenWeatherMap](https://openweathermap.org/api)

3. Create a `.env` file in the project root:
```bash
VITE_WEATHER_API_KEY=your_api_key_here
```

4. Open `index.html` in your browser or use a local server:
```bash
python3 -m http.server 8000
# or
npx http-server
```

5. Visit `http://localhost:8000`

## Project Structure

```
windows10/
├── index.html          # Main HTML file
├── css/
│   ├── style.css       # Main stylesheet
│   └── responsive.css  # Mobile responsiveness
├── js/
│   ├── app.js          # Main application logic
│   ├── weather-api.js  # API integration
│   └── ui.js           # UI updates and interactions
├── assets/
│   ├── icons/          # Weather icons
│   └── images/         # Background images
├── .env.example        # Environment variables template
└── README.md           # This file
```

## Usage

1. **Search for a City:** Enter city name in the search bar
2. **Use Geolocation:** Click the location icon to use your GPS
3. **Toggle Temperature Units:** Click the °C/°F button
4. **View Forecast:** Scroll down to see 5-day forecast
5. **Save Location:** Click heart icon to save favorite locations

## API Integration

The dashboard uses the **OpenWeatherMap API**:

- Current Weather Endpoint: `/weather`
- Forecast Endpoint: `/forecast`
- Geocoding Endpoint: `/geo/1.0/direct`

### Example API Call:
```javascript
fetch(`https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${API_KEY}&units=metric`)
  .then(res => res.json())
  .then(data => displayWeather(data))
```

## Environment Variables

```env
VITE_WEATHER_API_KEY=your_openweathermap_api_key
VITE_API_BASE_URL=https://api.openweathermap.org/data/2.5
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT License - see LICENSE file for details
