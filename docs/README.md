# ISS Tracker

An interactive web app that visualises the International Space Station’s current position and orbital path on a 3D globe.

This project was built in 48 hours for the **NASA Space Apps Challenge 2022** as part of a six-person team. It uses the **WorldWindJS Web App Template** as a foundation and extends it with live ISS tracking, orbital visualisation, and an ISS model rendered above Earth.

![issTracker](https://user-images.githubusercontent.com/60287993/207030093-6e1d782d-113b-4707-a738-b6bd045b1310.PNG)

## Live Demo

View the project here:

https://dylanpjhough.github.io/iss-tracker/

## Overview

ISS Tracker displays the International Space Station on an interactive globe and updates its position using live Two-Line Element data. The app plots the station’s orbit around Earth, places a 3D ISS model at its current location, and allows users to explore the globe through different map layers and settings.

The goal of the project was to make satellite tracking more visual and accessible by showing the ISS in context: where it is now, where it has been, and where it is heading next.

## Features

* Live ISS position tracking using TLE data
* 3D globe powered by WorldWindJS
* Rendered ISS model positioned above Earth
* Visual orbital path showing previous, current, and upcoming ground tracks
* Multiple base map and overlay layers
* Stars and atmospheric effects for a more realistic space view
* Layer and settings panels built with Bootstrap and Knockout
* Browser-based app with no backend required

## Tech Stack

* JavaScript
* HTML
* CSS
* WorldWindJS
* Bootstrap
* Knockout.js
* tle.js
* GitHub Pages

## How It Works

The app fetches current TLE data for the ISS and uses it to calculate the station’s latitude and longitude. That position is then mapped onto a WorldWindJS globe at an approximate ISS altitude.

The orbit path is generated from previous, current, and upcoming ground track data, then rendered as a raised path around the globe. A Collada 3D model of the ISS is loaded and updated every second to keep it aligned with the latest calculated position.

## Running Locally

Because the project uses JavaScript modules, it should be served through a local web server rather than opened directly as a file.

Clone the repository:

```bash
git clone https://github.com/DylanPJHough/iss-tracker.git
cd iss-tracker
```

Start a local server. For example, using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Project Structure

```text
iss-tracker/
├── index.html              # Main app page
├── app.js                  # App setup, ISS tracking logic, and WorldWind layers
├── Globe.js                # WorldWind globe wrapper and layer utilities
├── LayersViewModel.js      # Layer panel logic
├── SettingsViewModel.js    # Globe settings logic
├── SearchPreviewViewModel.js
├── custom.css              # App styling
├── images/                 # ISS model and visual assets
├── docs/                   # Project documentation/assets
└── LICENSE
```

## Background

This repository is forked from the WorldWindJS Web App Template, which provides the base globe, map layer, and UI functionality. The hackathon project builds on that foundation to focus specifically on ISS tracking and visualisation.

## Challenges and Learning

Building this in a 48-hour hackathon meant balancing speed with experimentation. The project involved working with orbital data, rendering a 3D model on a globe, updating positions in real time, and integrating multiple JavaScript libraries into a single browser-based experience.

Key learning areas included:

* Working with satellite TLE data
* Converting orbital data into map positions
* Rendering 3D assets in a geospatial environment
* Managing globe layers and UI state
* Collaborating under a tight hackathon deadline

## License

This project is licensed under the MIT License.

The original WorldWindJS template code is also MIT licensed.
