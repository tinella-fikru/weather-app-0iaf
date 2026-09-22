# Weather App

A single-file weather app (`index.html`) showing live conditions and a 5-day forecast from the [Open-Meteo](https://open-meteo.com/) API. It features animated SVG weather icons, a full-screen animated sky that matches the current conditions, and weather-tinted glass cards.

## Running

No build step is required. Open `index.html` directly in a browser:

```
file:///C:/Project/weather-app-0iaf/index.html
```

Or serve the folder with any static server, e.g.:

```
npx serve .
```

On load the app shows Tokyo, and you can search for any city. If the network request fails it falls back to cached Tokyo data.

## Previewing weather scenes

Add a `?preview=<type>` query parameter to force a specific weather type. This bypasses the live API and renders sample data so you can see the sky animation, icon, and card theme for that condition.

| Weather | URL |
|---|---|
| Clear sky | `file:///C:/Project/weather-app-0iaf/index.html?preview=sun` |
| Mostly clear | `file:///C:/Project/weather-app-0iaf/index.html?preview=mostly-clear` |
| Partly cloudy | `file:///C:/Project/weather-app-0iaf/index.html?preview=partly-cloudy` |
| Overcast | `file:///C:/Project/weather-app-0iaf/index.html?preview=cloud` |
| Fog | `file:///C:/Project/weather-app-0iaf/index.html?preview=fog` |
| Drizzle / light rain | `file:///C:/Project/weather-app-0iaf/index.html?preview=drizzle` |
| Rain | `file:///C:/Project/weather-app-0iaf/index.html?preview=rain` |
| Snow | `file:///C:/Project/weather-app-0iaf/index.html?preview=snow` |
| Thunderstorm | `file:///C:/Project/weather-app-0iaf/index.html?preview=storm` |

If you are serving the app over HTTP, use the same parameter on your local URL, e.g. `http://localhost:3000/?preview=rain`.

Remove the `?preview` parameter to return to live data.

## Features

- **Animated icons** – rotating sun rays, drifting clouds, falling rain and snow, flashing lightning, sliding fog. Icons enlarge and lift on hover.
- **Full-screen sky** – background gradient and particle effects (sun glow, clouds, raindrops, snowflakes, fog bands, lightning) change with the current weather.
- **Weather-tinted cards** – the search bar, current-weather card, and forecast cards use frosted glass styling with a palette matched to each condition.
- **Reduced motion** – all animations are disabled when the OS `prefers-reduced-motion` setting is on.
