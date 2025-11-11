# Project 3 - Analysis of Drowning Cases in the Sea in Catalonia (2025)

## Introduction

This project was inspired by recent drowning cases in the sea in Catalonia, a region in Spain. My main curiosity was to find out if there was any pattern and if there were specific locations where drownings occurred more frequently. Here you can check the website: [Drowned People in the sea](https://journadata.github.io/Project3_Drownedpeople/)

I also wanted to know if there was a pattern behind.

---

## Project Workflow

### 0. Data Acquisition and Preparation

- Collected data from all official government press releases.
- Cleaned the data using Python pandas for better structuring.
- Geolocated the points to be able to map them (geopy.geocoders / Nominatim).
- Requested official data from the government to cross-check and validate the information collected.

### 1. Creating the Map (2025)

- Used QGIS to:
  - Obtain the ocean, land, and coastline layers.
  - Import a CSV file containing coordinates where drownings occurred.
  - Import the CSV again to display flags and related icons.
  - Illustrator to to edit the layers and create the icons

- Icons used:
  - Flag: *Flag* by Iain Hector - [Noun Project](https://thenounproject.com/browse/icons/term/flag/) (CC BY 3.0)
  - Drowned: *Drown* by Adrien Coquet - [Noun Project](https://thenounproject.com/browse/icons/term/drown/) (CC BY 3.0)
  - Footer drown icon: Ian Rahmadi Kurniawan - [Noun Project](https://thenounproject.com/browse/icons/term/drown/) (CC BY 3.0)

- Fonts used:
  - [Fira Sans](https://fonts.google.com/specimen/Fira+Sans)
  - Georgia

- Color palette (created with Adobe):
  - #A5BFDD
  - #5F7793
  - #f2e3c7

- DISPLAY: I tried to make the map interactive for an scrollytelling with ai2html and scrollama webpage, but I was unable to fully integrate it into the website. 
- Instead, I created a simpler scrollytelling template with backgound images webpage scrolly-images/index.html. I used scrollama and generated .png images of each step from the map already created and edited.

### 2. Extracting and Analyzing Historical Data

- 2025 data: manually recorded from the Catalan government press notes to build my own dataset, mainly used to geolocate drowning sites. Initially tried Google Maps API, but switched to using `geopy.geocoders` and Nominatim. (See notebook: `Geolocate_beach_2025.ipynb`)

- Past decade data: requested from the press department, who provided Word documents listing cases including date, gender, beach, age, nationality, lifeguard presence, and flag color. Performed cleaning and extraction to build a dataframe. (See notebook: `extracting_drownedinfo.ipynb`)

- Analysis: explored number of drownings by comarca (county). (See notebook: `Drowned_all_analysis.ipynb`)

### 3. Creating Visualizations


- Built a temporal evolution chart of drownings over the past decade using D3 Observable, embedded as SVG in `index.html`. The live version is available here: [Evolution of Drownings in D3 Observable](https://observablehq.com/@journa4data/evolution_drowned)

- Created a liquid wave graphic with help from ChatGPT based on this example: [Stack Overflow example](https://stackoverflow.com/questions/65300031/d3-liquid-water-chart-conversion-from-d3v3-to-v4)

- Other graphics (e.g., showing most drownings occur when lifeguards are present and the flag is green, confirmed by historical data) were created with Flourish.

---

## Areas for Improvement

- Add information on which regions have the highest number of victims.
- Learn to geolocate more efficiently using Google Maps API.
- Fully master embedding ai2html SVG images despite no longer having an Illustrator license.

---

## Final Reflection

This project was an opportunity to apply a wide variety of languages and tools learned over the past 10 weeks. It was a lesson in time management, managing expectations, and how to redirect a project when encountering difficulties. It also taught me to overcome frustration when not knowing everything perfectly but still pushing forward to finish a project that offers significant learning and value.

---

*Thank you for reviewing my project!*
