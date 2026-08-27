# TV Series List

A React app for searching TV shows and viewing show details, built on the free [TVmaze API](https://www.tvmaze.com/api).

## Features

- Search-as-you-type for TV shows
- Click a result to view a detail page with premiere date, rating, and poster image
- Client-side routing via `react-router-dom`

## Tech Stack

- React 16.8.6 (Create React App / react-scripts 3.0.1)
- react-router-dom for routing
- TVmaze API (no API key required)

## Getting Started

This project uses an older version of `react-scripts` that requires Node 16 (newer Node versions will throw an OpenSSL-related build error).

```bash
git clone https://github.com/tnelson2016/tv-series-app.git
cd tv-series-app
nvm use 16          # or use NODE_OPTIONS=--openssl-legacy-provider on newer Node
npm install
npm start
```

The app will open at [http://localhost:3000](http://localhost:3000).

## Known Issues

- No loading/error states beyond a basic "Loading..." message
- Styling is minimal/unstyled — functional but not polished
- No test coverage beyond the default CRA smoke test

## Project Structure

```
src/
  components/
    App/           # Root component
    Main/           # Route switch (list view vs. detail view)
    Intro/          # Simple message component
    SeriesList/     # Renders search results as a list
  containers/
    Series/         # Search input + results (home page)
    SingleSeries/    # Show detail page (fetched by id)
```