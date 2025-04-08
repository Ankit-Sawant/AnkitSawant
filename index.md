---
layout: default
title: Data Visualization Dashboard
---

# 🧭 Data Visualization Dashboard

This page presents two data visualizations generated using Vega-Lite and embedded via HTML in this GitHub Pages Jekyll site. Each visualization includes a description, design explanation, and discussion of interactivity, transformations, and overlap with Homework 5.

---

## 📊 Visualization 1: Bigfoot Sightings by State
<iframe src="assets/bigfoot_state_counts.html" width="900" height="450" style="border:none;"></iframe>

### What is being visualized?
This bar chart visualizes the number of Bigfoot sightings reported across various U.S. states, based on the BFRO dataset.

### Design Choices: Encodings
- **X-axis (Nominal):** State names  
- **Y-axis (Quantitative):** Number of reported sightings  
- **Color (Quantitative):** Used to represent the number of sightings, using the "blues" colormap to enhance visual differentiation.

### Design Choices: Colormap
A sequential "blues" color scheme is used to encode the number of sightings, allowing viewers to quickly identify states with higher counts.

### Data Transformations
Sightings were aggregated by state using Python to prepare the data before feeding it into Vega-Lite.

### Homework #5 Overlap
This visualization **does not overlap** with Homework #5 in either dataset or design approach.

---

## 🌍 Visualization 2: Bigfoot Sightings by Season (Interactive)
<iframe src="assets/bigfoot_season_time.html" width="700" height="450" style="border:none;"></iframe>

### What is being visualized?
This interactive scatter plot visualizes Bigfoot sightings over time and latitude, categorized by season. The dropdown menu allows filtering based on season.

### Design Choices: Encodings
- **X-axis (Temporal):** Date of sighting  
- **Y-axis (Quantitative):** Latitude  
- **Color (Nominal):** Season  
- **Size:** Fixed, uniform dot size  
- **Tooltip:** Shows sighting details on hover

### Design Choices: Colormap
Color is encoded by season using a default nominal palette to distinguish between the five seasons (Summer, Spring, Winter, Fall, Unknown).

### Data Transformations
A filtering transformation was implemented using Vega-Lite's parameter binding. Python was used initially to parse and clean date and season fields.



---

## 💡 Write-up: Interactivity
The second chart allows users to filter sightings by season. This enhances interpretability and encourages exploratory analysis by season, showing how activity patterns may vary over the year.

---

## 🔗 Data Sources
- **Bigfoot dataset:** [BFRO Fall 2022](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv)  
- **Building dataset:** [Illinois Building Inventory](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)

---

## 📓 Python Notebooks
- [Notebook: Extra Credit](https://github.com/Ankit-Sawant/AnkitSawant/blob/main/Extra_credit.ipynb)  
- [Notebook: Workbook](https://github.com/Ankit-Sawant/AnkitSawant/blob/main/Workbook%20(11).ipynb)

---


