# Weather-Monitoring-System_

## Objective
This project is a real-time data processing system that monitors weather conditions and provides summarized insights using rollups and aggregates, utilizing data from the OpenWeatherMap API.

## Features
- Continuous weather data retrieval for major metros in India.
- Daily weather summaries including average, maximum, and minimum temperatures.
- Alert system for user-configurable weather conditions.
- Visualizations for historical data and triggered alerts.

## Getting Started

### Prerequisites
- Docker or Podman
- Python 3.x
- API Key from [OpenWeatherMap](https://openweathermap.org/)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/weather-monitoring-system.git
   cd weather-monitoring-system
   
2.**Build the Docker container:**
   ```bash
    docker build -t weather-monitor .

3. **Run the container:**
    ```bash
   docker run -d -p 8080:8080 -e OPENWEATHER_API_KEY=your_api_key weather-monitor
    
### Configuration
Set the environment variable OPENWEATHER_API_KEY with your OpenWeatherMap API key when running the container.

### Design Choices
1.Modular Architecture: The code is structured into separate modules for data retrieval, processing, alerting, and visualization for better maintainability and testing.
2.SQLite Database: Chosen for its simplicity and lightweight nature to store daily summaries.

### Dependencies
-sqlite3: For database interactions.
-requests: For making API calls.
-matplotlib: For visualizations.
-Flask: For web interface (if applicable).

### Usage
Access the application at http://localhost:8080 to view daily summaries and alerts.

### Testing
Tests are located in the tests/ directory. Run tests using:
python -m unittest discover -s tests


