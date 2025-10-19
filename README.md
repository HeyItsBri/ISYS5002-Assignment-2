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
## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- Internet connection (for API calls)
- Google Colab account (recommended) or Jupyter Notebook

### Installation

#### Option 1: Google Colab (Recommended - No Installation Required)

1. Click the "Open in Colab" badge at the top of this README
2. All dependencies are pre-installed in Colab
3. Simply run the cells!

#### Option 2: Local Installation

1. **Clone the repository:**
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

2. **Install dependencies:**
```bash
pip install requests pandas matplotlib pyinputplus ipywidgets
```

3. **Get API Key:**
   - Sign up at [OpenWeatherMap](https://openweathermap.org/api)
   - Get your free API key
   - The notebook includes a demo API key, but replace it with your own for production use

4. **Run the notebook:**
```bash
jupyter notebook Weather_Dashboard.ipynb
```

---

## 📱 Usage Guide

### Quick Start

1. **Open the notebook** in Google Colab (click badge above) or Jupyter
2. **Run all cells**: Click `Runtime` → `Run all` (Colab) or `Cell` → `Run All` (Jupyter)
3. **Wait for initialization**: All cells will execute automatically
4. **Scroll to the bottom**: Find the interactive menu
5. **Start exploring!**

---

### Interface Modes

The application offers multiple ways to interact:

#### 1. 🖥️ Terminal Menu Mode

A full-featured text-based menu with all options.

**How to use:**
1. Select option `1` from the main menu
2. Choose from:
   - View Current Weather
   - View 5-Day Forecast
   - Ask Natural Language Question
   - Visualize Weather Data
   - Compare Multiple Cities
   - Exit Dashboard

**Example:**
```
Select option: 1
Enter city name: london
✨ Did you mean 'London'?
✓ Fetching weather for London...
```

---

#### 2. 💬 Natural Language Mode

Ask questions in plain English.

**How to use:**
1. Select option `2` from the main menu
2. Type your question naturally
3. Optionally use AI (Ollama) for better understanding
4. Get instant answers!

**Example Questions:**
```
❓ What's the temperature in London?
→ The current temperature in London, GB is 15.2°C. It feels like 14.1°C.

❓ Will it rain tomorrow in Paris?
→ Yes, rain is expected in Paris tomorrow. About 2.5mm of rainfall with light rain.

❓ Should I bring an umbrella in Perth today?
→ No, it's not raining in Perth right now. The weather is clear sky.

❓ How windy is it in Tokyo?
→ The wind speed in Tokyo is 3.2 m/s.

❓ What's the weather in New York next Friday?
→ In 5 days in New York, expect partly cloudy with a temperature of 23.5°C.
```

**Supported Query Types:**
- Temperature: "What's the temp in London?"
- Rain: "Will it rain in Paris?"
- Wind: "How windy is Tokyo?"
- Humidity: "What's the humidity in Dubai?"
- General: "What's the weather like in Sydney?"

**Time References:**
- Current: "today", "right now", "currently"
- Tomorrow: "tomorrow"
- Specific days: "next Friday", "this Monday"
- Days ahead: "in 3 days", "5 days from now"

---

#### 3. 🚀 Quick Check Mode

Fast single-city weather lookup.

**How to use:**
1. Select option `3` from the main menu
2. Enter a city name
3. View detailed weather information
4. Optionally see visualizations

**Example:**
```
📍 Enter city name: tokyo

✓ Fetching weather for Tokyo...

═══════════════════════════════════════════════
📍 Tokyo, JP
═══════════════════════════════════════════════
☁️  Conditions: Clear Sky
🌡️  Current Temperature: 18.3°C (Feels like 17.8°C)
💧 Humidity: 65%
💨 Wind Speed: 3.2 m/s
🎈 Pressure: 1013 hPa
👁️  Visibility: 10.0 km

📅 5-Day Forecast:
──────────────────────────────────────────────
Monday, Oct 20:
  🌡️  High: 21.3°C | Low: 15.2°C
  ☁️  Clear Sky
...

📊 Show visualizations? (Y/n):
```

---

#### 4. 🌍 Compare Multiple Cities

Compare weather across multiple locations.

**How to use:**
1. Select Terminal Menu → Compare Multiple Cities
2. Enter cities separated by commas
3. View side-by-side comparison

**Example:**
```
📍 Enter cities: london, paris, tokyo

✓ Valid input! Comparing 3 cities:
  1. London
  2. Paris
  3. Tokyo

🔍 Fetching weather data for 3 cities...

[Weather data for all 3 cities displayed]
```

**Input Formats Accepted:**
```
✓ london, paris, tokyo          (lowercase, auto-corrected)
✓ London, Paris, Tokyo           (proper capitalization)
✓ LONDON, PARIS, TOKYO           (uppercase, auto-corrected)
✓ new york, los angeles          (multi-word cities)
```

---

### Auto-Correction Examples

The system automatically corrects common mistakes:

**Capitalization:**
```
Input: "london" → Corrected to: "London"
Input: "new york" → Corrected to: "New York"
```

**Misspellings:**
```
Input: "londn" 
🤔 Did you mean:
  1. London
  2. Lund
  3. Londo
Select (1-3): 1
✓ Using London
```

**Close Matches:**
```
Input: "paaris"
✨ Auto-corrected to 'Paris'
```

---

### Visualizations

When you request visualizations, you'll see 4 charts:

1. **Temperature Trends**
   - Line chart with 3 lines: High, Low, Feels Like
   - Shows temperature variation over 5 days
   - Color-coded for easy reading

2. **Humidity Levels**
   - Bar chart showing humidity percentage
   - Values labeled on top of each bar
   - Scale from 0-100%

3. **Wind Speed**
   - Line chart with shaded area underneath
   - Shows wind speed variation
   - Measured in meters per second

4. **Rain Forecast**
   - Bar chart showing expected rainfall
   - Only shows bars for days with rain
   - Measured in millimeters

**Data Table:**
All forecast data is also available as a formatted table:
```
       Date        Day  Temperature (°C)  High (°C)  Low (°C)  ...
0  2025-10-20     Monday              15.2       17.3      13.1
1  2025-10-21    Tuesday              14.8       16.5      12.9
...
```

---

## 🎯 Use Cases

### 1. Daily Weather Check
```python
# Quick morning weather check
Select mode: Quick Check
Enter city: perth
→ See today's weather instantly
```

### 2. Travel Planning
```python
# Compare destinations
Select mode: Terminal Menu → Compare Cities
Enter cities: london, paris, rome, barcelona
→ Compare weather across all potential destinations
```

### 3. Natural Conversation
```python
# Ask like you'd ask a friend
Select mode: Natural Language
Question: Should I bring a jacket to Tokyo tomorrow?
→ Get a conversational response with weather details
```

### 4. Data Analysis
```python
# Get data for further analysis
city = "London"
weather_data = get_weather_data_openweather(city)
df = process_weather_to_dataframe(weather_data)
# Now you have a Pandas DataFrame for analysis
```

---

## 🏗️ Project Structure
```
Weather_Dashboard.ipynb
├── Cell 1: Weather API Functions
│   ├── get_weather_data_openweather()
│   ├── display_weather_for_city()
│   ├── create_weather_dashboard()
│   └── validate_city_input()
│
├── Cell 2: Data Visualization
│   ├── process_weather_to_dataframe()
│   └── visualize_weather_data()
│
├── Cell 3: Natural Language Processing
│   ├── parse_weather_question()
│   ├── generate_weather_response()
│   ├── extract_city_name()
│   └── detect_time_frame()
│
├── Cell 4: Menu Interface
│   ├── weather_menu_pyinputplus()
│   └── weather_menu_ipywidgets()
│
└── Cell 5: Main Application
    ├── DependencyManager
    ├── InputValidator
    ├── UserInterface
    ├── WeatherService
    ├── ApplicationMode classes
    └── WeatherDashboardApp
```

---

## 📊 Code Examples

### Example 1: Get Weather Data
```python
# Fetch weather for a single city
city = "London"
weather_data = get_weather_data_openweather(city)

# Access current temperature
temp = weather_data['current']['main']['temp']
print(f"Temperature: {temp}°C")
```

### Example 2: Process Natural Language
```python
# Parse a natural language question
question = "Will it rain tomorrow in Paris?"
parsed = parse_weather_question(question)

# Get weather data
weather_data = get_weather_data_openweather(parsed['city'])

# Generate response
response = generate_weather_response(parsed, weather_data)
print(response)
```

### Example 3: Create Visualizations
```python
# Get weather and create charts
city = "Tokyo"
weather_data = get_weather_data_openweather(city)
df = process_weather_to_dataframe(weather_data)

# Display data table
print(df)

# Create visualizations
visualize_weather_data(df, city)
```

### Example 4: Compare Multiple Cities
```python
# Compare weather across cities
cities = ["London", "Paris", "Tokyo", "New York"]
create_weather_dashboard(cities)
```

---

## 🧪 Testing

### Sample Test Cases

#### Test 1: Valid City Input
```python
city = "London"
weather_data = get_weather_data_openweather(city)
assert weather_data is not None
assert weather_data['current']['name'] == "London"
```

#### Test 2: Invalid City Input
```python
city = "InvalidCity12345"
weather_data = get_weather_data_openweather(city)
assert weather_data is None
```

#### Test 3: Natural Language Parsing
```python
question = "What's the temperature in London?"
parsed = parse_weather_question(question)
assert parsed['city'] == 'London'
assert parsed['query_type'] == 'temperature'
assert parsed['success'] == True
```

#### Test 4: Multi-word Cities
```python
city = "New York"
weather_data = get_weather_data_openweather(city)
assert weather_data is not None
assert "New York" in weather_data['current']['name']
```

#### Test 5: Auto-Correction
```python
city = "londn"
corrected, was_corrected, suggestions = InputValidator.auto_correct_city(city)
assert corrected == "London"
assert was_corrected == True
```

---

## 🛠️ Technologies Used

- **Python 3.x**: Core programming language
- **Requests**: HTTP library for API calls
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization and charting
- **PyInputPlus**: Enhanced input validation (terminal menu)
- **IPyWidgets**: Interactive widgets for Jupyter (GUI menu)
- **OpenWeatherMap API**: Real-time weather data source
- **Levenshtein Distance Algorithm**: String similarity for auto-correction
- **Regular Expressions**: Pattern matching for NLP
- **Object-Oriented Programming**: Modular, maintainable code structure

---

## 🔑 API Information

### OpenWeatherMap API

This project uses the OpenWeatherMap API to fetch weather data.

**API Key:** The notebook includes a demo API key for testing purposes.

**For production use:**
1. Create a free account at [OpenWeatherMap](https://openweathermap.org/api)
2. Get your API key from the dashboard
3. Replace the API key in Cell 1:
```python
def get_weather_data_openweather(location, forecast_days=5, api_key="YOUR_API_KEY_HERE"):
```

**API Limits (Free Tier):**
- 60 calls/minute
- 1,000,000 calls/month
- Current weather data
- 5-day forecast

**Endpoints Used:**
- Current weather: `api.openweathermap.org/data/2.5/weather`
- 5-day forecast: `api.openweathermap.org/data/2.5/forecast`

---

## 🐛 Troubleshooting

### Issue 1: "Module not found" error
**Solution:**
```bash
pip install requests pandas matplotlib pyinputplus ipywidgets
```

### Issue 2: API key invalid
**Solution:**
- Verify your API key is correct
- Check if your API key is activated (may take a few hours)
- Ensure you're using the correct endpoint

### Issue 3: City not found
**Solution:**
- Check spelling of city name
- Try using the full city name
- Use English names for international cities
- Example: Use "Moscow" not "Москва"

### Issue 4: Widgets not displaying
**Solution:**
- Make sure you're using Jupyter Notebook or Google Colab
- Widgets don't work on GitHub (use "Open in Colab" badge)
- In Jupyter, run: `jupyter nbextension enable --py widgetsnbextension`

### Issue 5: Ollama queries failing
**Solution:**
- Install Ollama: [https://ollama.ai](https://ollama.ai)
- Start Ollama: `ollama serve`
- Download a model: `ollama pull llama2`
- Or simply use without AI (works perfectly fine!)

### Issue 6: Charts not showing
**Solution:**
- In Jupyter, add this to the first cell: `%matplotlib inline`
- In Colab, charts should display automatically
- Check that matplotlib is installed

---

## 📝 Assignment Completion Checklist

### Core Requirements
- [x] Fetch weather data from API
- [x] Process and display weather information
- [x] Handle user input
- [x] Error handling and validation
- [x] Data visualization
- [x] Natural language processing
- [x] Multi-city comparison

### Advanced Features
- [x] Auto-correction of city names
- [x] Levenshtein distance algorithm
- [x] Interactive menu system
- [x] Pandas DataFrame integration
- [x] Multiple visualization types
- [x] Time-based query parsing
- [x] Modular, object-oriented design

### Code Quality
- [x] Clear variable names
- [x] Comprehensive comments
- [x] Function documentation
- [x] Error handling
- [x] Input validation
- [x] Separation of concerns
- [x] Reusable functions

### Testing
- [x] Tested with multiple locations
- [x] Tested various question types
- [x] Tested edge cases
- [x] Tested invalid inputs
- [x] Tested visualizations
- [x] All features functional

---

### I hope you enjoy this little project! ###
Thuy Linh Nguyen
22835707
Curtin Business and Law Faculty
Master of Commerce
Semester 2/2025
