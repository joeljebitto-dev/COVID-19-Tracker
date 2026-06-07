# COVID-19 Tracker

A React-based COVID-19 tracker dashboard that displays global and country-level pandemic statistics using live data from the disease.sh API. The app includes summary cards, country selection, an interactive map, a ranked country table, and historical line charts.

## Features

* Live worldwide COVID-19 statistics
* Country-specific COVID-19 data
* Dropdown country selector
* Summary cards for cases, recovered, and deaths
* Interactive Leaflet map
* Country markers based on selected case type
* Ranked table of live cases by country
* Historical line graph for worldwide cases, recoveries, and deaths
* Number formatting with Numeral.js
* Material UI card and form components
* Responsive dashboard-style layout

## Tech Stack

* React
* Create React App
* Material UI
* Chart.js
* React Chart.js 2
* Leaflet
* React Leaflet
* Numeral.js
* JavaScript
* CSS

## Project Structure

```text id="cv5gne"
COVID-19-Tracker/
├── public/
├── src/
│   ├── App.js
│   ├── App.css
│   ├── InfoBox.js
│   ├── InfoBox.css
│   ├── LineGraph.js
│   ├── Map.js
│   ├── Map.css
│   ├── Table.js
│   ├── Table.css
│   ├── util.js
│   └── index.js
├── package.json
└── README.md
```

## Data Source

The app uses the public disease.sh COVID-19 API.

Main endpoints used by the app:

```text id="v8nr01"
https://disease.sh/v3/covid-19/all
https://disease.sh/v3/covid-19/countries
https://disease.sh/v3/covid-19/countries/{countryCode}
https://disease.sh/v3/covid-19/historical/all?lastdays=120
```

## How It Works

Application flow:

```text id="j0o79p"
Load app
  ↓
Fetch worldwide COVID-19 totals
  ↓
Fetch country-level COVID-19 data
  ↓
Render summary cards, map, and country table
  ↓
User selects case type or country
  ↓
Dashboard updates selected statistics, map, and chart
```

Core UI sections:

* **Stats cards:** show today and total values for cases, recovered, and deaths
* **Country dropdown:** switches between worldwide and selected-country data
* **Map:** visualizes country-level data using Leaflet
* **Table:** lists countries ordered by case count
* **Line graph:** displays historical worldwide data for the selected case type

## Installation

Clone the repository:

```bash id="ur5xry"
git clone https://github.com/joeljebitto-dev/COVID-19-Tracker.git
cd COVID-19-Tracker
```

Install dependencies:

```bash id="dqkgav"
npm install
```

Or with Yarn:

```bash id="jg8p2z"
yarn install
```

## Running the App

Start the development server:

```bash id="mvwp8c"
npm start
```

Or with Yarn:

```bash id="amsr7t"
yarn start
```

Then open:

```text id="j5hbwm"
http://localhost:3000
```

## Available Scripts

```bash id="a75v9i"
npm start
npm test
npm run build
```

Or with Yarn:

```bash id="e6kufd"
yarn start
yarn test
yarn build
```

## Build for Production

```bash id="nl9c71"
npm run build
```

The optimized production build will be generated in the `build/` directory.

## Notes

* This is a frontend-only React dashboard.
* The app depends on the availability and response shape of the disease.sh API.
* The displayed COVID-19 data is for visualization and learning purposes.
* The project uses older Create React App, React, Material UI, Chart.js, and React Leaflet versions.
* COVID-19 API data may be incomplete, delayed, deprecated, or unavailable depending on the external data provider.

## Future Improvements

* Add loading and error states for API requests
* Add API failure fallback UI
* Add TypeScript
* Add search/filter for the country table
* Add mobile-responsive layout improvements
* Add country flag display
* Add date range controls for historical charts
* Add tests for utility functions and rendering
* Upgrade React and project dependencies
* Replace deprecated packages where needed
* Add environment-based API configuration
* Add deployment instructions for Vercel, Netlify, or Firebase Hosting

## Author

Built by [Joel Jebitto](https://github.com/joeljebitto-dev).
