---
layout: default
title: Data Visualization Dashboard
---

# 🧭 Data Visualization Dashboard

This page presents two data visualizations generated using Vega-Lite and embedded via HTML in this GitHub Pages Jekyll site. Each visualization includes a description, design explanation, and discussion of interactivity, transformations, and overlap with Homework 5.

---

## 📊 Visualization 1: Bigfoot Sightings by State
<iframe src="assets/bigfoot_state_counts.html" width="1700" height="450" style="border:none;"></iframe>

### What is being visualized?
This bar chart displays the number of Bigfoot hunting or research licenses issued in different U.S. states during Fall 2022. The goal of this visualization is to highlight geographic differences in Bigfoot-related activity and participation, based on state-issued licenses.

### Design Choices: Encodings
I used a vertical bar chart where the x-axis encodes the state (nominal) and the y-axis encodes the count of licenses (quantitative). Each bar represents one state. The bars are sorted in descending order by count so that states with the highest activity appear first, making it easier to compare them. I applied the 'oranges' color scheme to the bars, which gives the chart a slightly humorous or playful tone while still providing a heatmap-like gradient that emphasizes the volume of licenses per state.

### Data Transformations
To prepare the data, I cleaned out any rows with missing or invalid values in the state or relevant columns. I then grouped the dataset by state and calculated the number of records (licenses) associated with each one. The result was a simple frequency table, which I sorted to ensure the most active states were emphasized in the visualization.


---

## 🌍 Visualization 2: Bigfoot Sightings Over Time by Season (Interactive)
<iframe src="assets/bigfoot_season_time.html" width="700" height="450" style="border:none;"></iframe>

### What is being visualized?
This interactive scatterplot shows the geographical distribution (latitude) of Bigfoot sightings over time, with an option to filter the data by season. The chart aims to uncover any seasonal or spatial trends in Bigfoot sighting reports.

### Design Choices: 
The x-axis represents the date of the sighting (temporal data), and the y-axis represents the latitude (quantitative), showing how far north or south the sightings occur. The color encoding is based on season, a nominal variable, which helps distinguish seasonal trends and clusters. Points are styled as circles, with a tooltip that includes the date, state, season, latitude, and longitude for added context. The color categories are automatically chosen by Altair to differentiate seasons clearly.



### Data Transformations
The data used in this plot was pre-cleaned (df_clean) to ensure accurate latitude, longitude, date, and season values. No aggregation was needed, as each row represents a single sighting.



---

## Interactivity
 dropdown menu allows users to select a season (Fall, Winter, Spring, Summer or Unknown). When a season is selected, the chart dynamically filters the data to show only the sightings from that time of year. This feature significantly enhances clarity by decluttering the view and allowing focused analysis of how sightings may shift north/south or increase/decrease depending on the season.

---

### EXTRA CREDIT

## 📊 Visualization 3: Top 15 Agencies by Total Building Square Footage
<iframe src="assets/building_sqft_by_agency.html" width="700" height="450" style="border:none;"></iframe> 

### What is being visualized?
This visualization is a horizontal bar chart that displays the top 15 government agencies in Illinois by the total square footage of the buildings they own or manage. The chart helps convey which agencies occupy the most physical infrastructure space and provides a clear comparison of their building footprints.

### Design Choices: 
For this chart, I used a horizontal bar layout to improve readability of the agency names, which can often be long. The x-axis encodes the total square footage (a quantitative field), while the y-axis encodes the agency name (a nominal variable). The bars are sorted in descending order of square footage, which allows viewers to quickly identify the largest agencies. I applied color encoding to the bars using the 'teals' color scheme, where darker shades represent higher total square footage. This visual cue reinforces the magnitude of each bar and adds aesthetic appeal.


### Data Transformations
On the data side, I first ensured that the Square Footage column was numeric by coercing any invalid entries. I then removed rows with missing values in the Agency Name or Square Footage columns. To create the summary view, I grouped the data by Agency Name and calculated the total square footage for each agency. After aggregating the data, I sorted the agencies in descending order and selected only the top 15 for display to keep the visualization focused an

--- 
## 📊 Visualization 4: Building Age Vs Sqaure Footage
<iframe src="assets/building_age_sqft.html" width="700" height="450" style="border:none;"></iframe> 


### What is being visualized?
This plot is an interactive scatterplot that explores the relationship between the age of a building and its square footage, with an added dropdown filter to isolate individual agencies. This visualization helps identify patterns in how agencies use building space over time, such as whether newer buildings are larger or smaller than older ones.

### Design Choices:
The x-axis represents building age, calculated as 2025 - Year Acquired, and the y-axis represents the building's square footage. Each point in the scatterplot is a building, and the color of each point corresponds to its Usage Description, a nominal variable that describes how the building is used (e.g., office, warehouse). I chose a circle mark with a size of 60 to ensure visibility without overcrowding. I also included a tooltip that reveals key information—location name, square footage, age, and usage—when hovering over a point. These design decisions aim to balance clarity and interactivity while allowing for deep exploration of trends.

### Data Transformations
I began by converting the Year Acquired and Square Footage columns to numeric, coercing errors to handle any non-numeric values. I dropped rows with missing values in the key columns needed for this analysis. I then created a new column, Building Age, by subtracting the acquisition year from 2025. This allowed me to easily plot age on the x-axis. The resulting dataset was filtered to remove rows lacking necessary information for either axis or color encoding.

### Interactivity
This plot includes a dropdown menu that allows users to select an agency from the dataset. When an agency is selected, the scatterplot updates to only show buildings belonging to that agency. This makes the plot much more informative and user-friendly, as it avoids overwhelming the viewer with thousands of data points at once. The dropdown enables focused analysis and comparison between agencies, helping users better understand how different types of buildings are distributed over time and space.

---

## 🔗 Data Sources
- **Bigfoot dataset:** [BFRO Fall 2022](https://github.com/Ankit-Sawant/AnkitSawant/blob/main/bfro_reports_fall2022.csv)  
- **Building dataset:** [Illinois Building Inventory](https://github.com/Ankit-Sawant/AnkitSawant/blob/main/building_inventory.csv)

---

## 📓 Python Notebooks
- [Notebook: Extra Credit](https://github.com/Ankit-Sawant/AnkitSawant/blob/main/Extra_credit.ipynb)  
- [Notebook: Workbook](https://github.com/Ankit-Sawant/AnkitSawant/blob/main/Workbook%20(11).ipynb)

---


