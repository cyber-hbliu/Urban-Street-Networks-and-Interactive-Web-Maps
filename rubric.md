# Grading Rubric for Assignment #6

Please include your name at the top of the submitted notebook.

**Important:** Your notebooks should be a polished finished product. For example:

- please remove any extra or unnecessary code.
- please try to use markdown cells with section headers to mark different sections of the analysis.

## Rubric

**Part 1: Visualizing crash data in Philadelphia (28 points)**

- 1.1 Load the geometry for the region being analyzed (2 points)
- 1.2 Get the street network graph (2 points)
- 1.3 Convert your network graph edges to a GeoDataFrame (2 points)
- 1.4 Load PennDOT crash data (1 point)
- 1.5 Convert the crash data to a GeoDataFrame (1 point)
- 1.6 Trim the crash data to Center City (2 points)
- 1.7 Find the nearest edge for each crash (2 points)
- 1.8 Calculate the total number of crashes per street (3 points)
- 1.9 Merge your edges GeoDataFrame and crash count DataFrame (2 points)
- 1.10 Calculate a "Crash Index" (3 points)
- 1.11 Plot a histogram of the crash index values (2 points)
- 1.12 Plot the street networks, colored by the crash index (2 points)
- 1.13 An interactive map of the crash index (4 points)

**Part 2: Interactive web maps with Folium (12 points)**

- Pulling the data from an API (5 points)
- Transforming the geometry lat/lng to the proper coordinates format for the HeatMap plugin (3 points)
- Make the interactive Folium heatmap (4 points)

**Total points: 40 points**
