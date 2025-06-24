
# 🌐 Real-Time Weather & Air Quality Dashboard using Power BI

This repository showcases a dynamic and interactive **Weather & AQI Dashboard** built in **Power BI**, powered by **live data from WeatherAPI**. It delivers real-time weather conditions and air quality insights for any selected city, with a clean and responsive UI.

---

## 📊 Project Overview

The goal of this project is to integrate live weather and air quality data into a fully functional Power BI dashboard that not only informs but also engages. From temperature and humidity to pollutants like SO₂ and CO, every detail is visualized with clarity and purpose.

---

## 🔧 Features

- **Real-time weather data**
  - Temperature, Humidity, UV Index, Wind Speed, Visibility, and Pressure
- **Air Quality Index (AQI) readings**
  - Visualizations for SO₂, PM10, CO, and O₃
  - Color-coded AQI levels using custom DAX logic
  - Health suggestions based on AQI thresholds
- **7-day weather forecast**
  - Line chart for temperature trends
  - Horizontal bar chart for chance of rain
- **Sunrise and sunset timings**
- **City toggle switch**
  - Choose between multiple cities (e.g., Pune, Noida)
- **Modern dark-themed UI with responsive layout**

---

## 🛠️ Tools & Technologies

- [Power BI Desktop](https://powerbi.microsoft.com/)
- [WeatherAPI](https://www.weatherapi.com/)
- Power Query (for data extraction and transformation)
- DAX (for dynamic measures, logic, and visual encoding)

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/weather-aqi-dashboard.git
````

### 2. Get Your WeatherAPI Key

* Sign up at [weatherapi.com](https://www.weatherapi.com)
* Copy your free or premium API key

### 3. Connect API to Power BI

* Open the `.pbix` file in Power BI Desktop
* Navigate to `Transform Data` → `Advanced Editor`
* Replace `"YOUR_API_KEY"` in the query URL with your actual key
* Replace city name if needed (e.g., `q=Pune`)

### 4. Load the Data

* Power BI will fetch real-time data from WeatherAPI
* Click **Close & Apply** to load the transformed data into your model

---

## 🧠 Custom DAX Measures

The dashboard uses modular and reusable DAX measures to:

* Dynamically color-code AQI readings
* Provide AQI-based health recommendations
* Categorize pollutant levels (Good, Moderate, Unhealthy, etc.)

Example:

```DAX
AQI Status =
VAR AQI = ROUND(SELECTEDVALUE('Current'[current.air_quality.pm10]), 0)
RETURN
SWITCH(
    TRUE(),
    AQI <= 50, "Good",
    AQI <= 100, "Moderate",
    AQI <= 150, "Unhealthy for Sensitive",
    AQI <= 200, "Unhealthy",
    AQI <= 300, "Very Unhealthy",
    "Hazardous"
)
```

---

## 🖼️ Screenshots

> Add screenshots here (e.g., `assets/screenshot-1.png`, `screenshot-2.png`)

---

## 📌 Use Cases

* Weather monitoring for cities
* Public health dashboards
* Smart city or IoT visualization layer
* Learning resource for API integration in Power BI

---

## 🙌 Acknowledgements

* [WeatherAPI](https://www.weatherapi.com) for free and accurate weather data
* Microsoft Power BI Community for learning resources

---

## 📬 Contact

**Author:** Shivam Shukla
**Email:** [imshivam077@gmail.com](mailto:imshivam077@gmail.com)
**LinkedIn:** [linkedin.com/in/shivam-shukla-5500ba239](https://linkedin.com/in/shivam-shukla-5500ba239)
**GitHub:** [github.com/shivamim](https://github.com/shivamim)


