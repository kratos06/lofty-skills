---
name: weather
description: Weather data and forecasts
---

# Weather Integration

Weather data and forecasts

## Configuration

### Environment Variable

```bash
export OPENWEATHER_API_KEY="your-api-key"
```

### Get API Credentials

https://home.openweathermap.org/api_keys

---

## API Reference

**Base URL:** `https://api.openweathermap.org/data/2.5`

**Authentication:** API key in query parameters

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/weather` | Current weather |
| GET | `/forecast` | 5-day forecast |
| GET | `/weather` | Weather by coords |

## Examples

### 1. Current weather

```bash
curl -s \
  "https://api.openweathermap.org/data/2.5/weather?q=London&units=metric&appid=$OPENWEATHER_API_KEY"
```

### 2. 5-day forecast

```bash
curl -s \
  "https://api.openweathermap.org/data/2.5/forecast?q=London&units=metric&appid=$OPENWEATHER_API_KEY"
```

### 3. Weather by coords

```bash
curl -s \
  "https://api.openweathermap.org/data/2.5/weather?lat=51.5&lon=-0.1&units=metric&appid=$OPENWEATHER_API_KEY"
```

---

## Author

community

## Version

1.0.0
