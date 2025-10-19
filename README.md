# ISYS5002-Assignment-2
For Curtin University authorized personnel view only. 
# 🌤️ Weather Dashboard Application

A powerful, interactive Python-based weather application that fetches real-time weather data, processes natural language queries, and provides beautiful visualizations.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1IuDdavi_5tswsJZTiciinU_qSbpmsGrU?usp=sharing)

---

## 📖 Project Description

The Weather Dashboard is an interactive Jupyter notebook application designed to make weather information accessible and easy to understand. Built with Python, it combines multiple technologies to provide a comprehensive weather experience:

- **Real-time Data Fetching**: Retrieves current weather and 5-day forecasts from OpenWeatherMap API
- **Natural Language Processing**: Understands questions like "Will it rain tomorrow in Paris?"
- **Smart Auto-Correction**: Automatically fixes misspelled city names using Levenshtein distance algorithm
- **Data Visualization**: Generates interactive charts for temperature trends, humidity, wind speed, and rainfall
- **Multi-City Comparison**: Compare weather conditions across multiple cities simultaneously
- **User-Friendly Interface**: Multiple interaction modes including terminal menus and natural language queries

This project demonstrates skills in:
- API integration and data fetching
- Data processing with Pandas
- Data visualization with Matplotlib
- Natural language processing
- Input validation and error handling
- Object-oriented programming
- User interface design

---

## ✨ Features

### 🌡️ Real-Time Weather Data
- Current temperature, feels-like temperature, and conditions
- Humidity, wind speed, and atmospheric pressure
- Visibility and weather descriptions
- 5-day detailed forecasts

### 💬 Natural Language Processing
- Ask questions naturally: "Should I bring an umbrella in Perth today?"
- Automatically detects city names from questions
- Identifies query types: temperature, rain, wind, humidity, conditions
- Supports time-based queries: "tomorrow", "next Friday", "in 3 days"
- Optional AI enhancement using Ollama for complex queries

### 🔧 Smart Auto-Correction
- Automatically capitalizes city names (london → London)
- Detects and corrects misspellings using fuzzy matching
- Suggests alternatives for ambiguous inputs
- Handles multi-word cities (New York, Los Angeles, etc.)
- Database of 300+ known cities worldwide

### 📊 Data Visualization
- **Temperature Trends**: Line chart showing high, low, and feels-like temperatures
- **Humidity Levels**: Bar chart with percentage values
- **Wind Speed**: Line chart with shaded area
- **Rain Forecast**: Bar chart showing expected rainfall
- Export data to Pandas DataFrame for further analysis

### 🌍 Multi-City Comparison
- Compare weather across up to 10 cities simultaneously
- Side-by-side weather information display
- Ideal for travel planning and regional analysis

### 🛡️ Robust Input Validation
- Validates city name formats
- Checks for invalid characters and empty inputs
- Provides helpful error messages with correction suggestions
- Automatic retry loops until valid input is provided

---

### I hope you enjoy this little project! ###
Thuy Linh Nguyen
22835707
Curtin Business and Law Faculty
Master of Commerce
Semester 2/2025
