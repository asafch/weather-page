# Weather Screen

A full-screen weather dashboard designed for always-on displays (e.g. an iPad by your front door). Shows hourly and daily forecasts, sun/moon position arcs, and animated weather backgrounds — all in a single HTML file with no dependencies.

## Features

- **12-hour forecast** — hourly cards with temperature, weather icon, and precipitation probability
- **6-day forecast** — daily cards with high/low temps and conditions
- **Sun arc widget** — real-time sun position on a sunrise-to-sunset arc, with next event times
- **Moon arc widget** — moonrise/moonset arc with current moon phase
- **Animated backgrounds** — CSS-only animations for clear, cloudy, rain, drizzle, thunderstorm, snow, fog, wind, and night conditions
- **Location support** — pass any city via query parameter; coordinates and timezone are resolved automatically
- **Auto-refresh** — weather data updates every 30 minutes

## Data Sources

| Data | Source | API Key |
|------|--------|---------|
| Weather forecast | [Open-Meteo](https://open-meteo.com) | Not required |
| Geocoding | [Open-Meteo Geocoding](https://open-meteo.com/en/docs/geocoding-api) | Not required |
| Moonrise/moonset | Calculated client-side (astronomical algorithm) | N/A |
| Moon phase | Calculated client-side (synodic month) | N/A |

## Usage

### Local

Open `index.html` in any browser. By default it shows weather for New York City.

To change the location, add a `?location=` query parameter:

```
index.html?location=London
index.html?location=Tokyo
index.html?location=Ramat+Gan
index.html?location=San+Francisco
```

### GitHub Pages

1. Fork or push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch**, select `main`, and click Save
4. Your site will be live at `https://<username>.github.io/weather-screen/`

Then use:

```
https://<username>.github.io/weather-screen?location=Paris
```

### iPad Setup

1. Open the URL in Safari on your iPad
2. Rotate to **landscape** orientation
3. Tap the Share button → **Add to Home Screen**
4. Open from the Home Screen (launches in full-screen mode)
5. Enable **Guided Access** (Settings → Accessibility → Guided Access) to lock the iPad to this app

## Technical Details

- Single `index.html` file — HTML, CSS, and JS are all inline
- No build step, no frameworks, no external assets
- Minimal JavaScript — only used for API fetches and DOM rendering
- Temperatures displayed in Celsius
- Optimized for iPad Mini in landscape (1024×768), but works on any screen size
