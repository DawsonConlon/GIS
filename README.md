Project Overview

This project demonstrates a geospatial data science workflow using Python to simulate environmental monitoring across Saskatchewan. The analysis integrates geographic data processing, coordinate reference system management, spatial buffering, contamination risk mapping, and watershed analysis.

Two primary workflows were implemented:
	1.	Saskatchewan GIS Data Acquisition and Sampling Site Mapping
	2.	Contamination Zone Simulation and Watershed Analysis

The project showcases practical GIS techniques using Python libraries such as:
	•	GeoPandas
	•	Shapely
	•	Matplotlib
	•	Pandas

The objective is to demonstrate how spatial data science techniques can be used to analyze environmental contamination risk and hydrological transport pathways

Project 1 Saskatchewan GIS Data & Sampling Sites

Objective

The goal of this project was to:
	•	Acquire geographic boundary data for Saskatchewan
	•	Demonstrate the importance of Coordinate Reference Systems (CRS)
	•	Simulate environmental sampling sites
	•	Visualize spatial environmental monitoring data

⸻

Data Acquisition

Saskatchewan boundary data was retrieved directly from an open GeoJSON dataset.

Coordinate Reference System (CRS) Transformation

The original dataset used WGS84 (EPSG:4326), which represents geographic coordinates in latitude and longitude.

However, geographic CRS systems distort measurements when calculating distances or areas.
For spatial analysis, the data was reprojected to:

EPSG:3347 — Statistics Canada Lambert

This projection is commonly used for Canadian spatial datasets because it preserves spatial accuracy for area and distance calculations.

The Lambert projection produces a more accurate spatial representation suitable for environmental analysis.

<img width="1427" height="914" alt="day1_crs_comparison" src="https://github.com/user-attachments/assets/fd9f7f68-d1de-46fa-ad8c-4a3f4c0e3cda" />

Sampling Site Simulation

Eight sampling sites were simulated across Saskatchewan using known town locations.
These represent hypothetical environmental monitoring stations.

Example attributes included:
	•	Site ID
	•	Site name
	•	Measured environmental parameter
	•	Simulated measurement value

<img width="791" height="1482" alt="day1_sampling_sites" src="https://github.com/user-attachments/assets/399e6591-fe91-45b1-ad86-e268fdc8995d" />


Project 2 Contamination Zone and Watershed Simulation

Objective

The second project expands the spatial analysis by simulating:
	•	contamination risk zones
	•	environmental monitoring buffers
	•	watershed regions
	•	spatial joins between monitoring sites and watersheds

This demonstrates how GIS can be used to evaluate environmental contamination spread and hydrological risk.

⸻

Sampling Site Buffer Analysis

To model potential contamination monitoring zones, 50 km buffers were generated around each sampling location.

  <img width="869" height="1482" alt="day2_buffers" src="https://github.com/user-attachments/assets/93b53671-ef53-4059-813e-e08c50d836c2" />
These buffers represent potential monitoring areas surrounding each sampling site.

A contamination source was simulated near Weyburn, Saskatchewan.

Contamination Zone Map: This visualization demonstrates how contamination impact can be modeled spatially around a pollution source


<img width="850" height="1482" alt="day2_risk_zones" src="https://github.com/user-attachments/assets/810da947-b2a4-40cb-b1fb-a8c31c9c8782" />


Watershed Simulation

Since water flow strongly influences contaminant transport, watershed zones were simulated to represent drainage basins.

For demonstration purposes, the Saskatchewan region was divided into a grid representing simplified watershed regions.
Each watershed polygon represents a theoretical drainage basin where water and contaminants would flow toward a common outlet.

<img width="865" height="1459" alt="day2_watersheds" src="https://github.com/user-attachments/assets/0875e43e-8d80-4f70-9acb-6bf2e830028b" />

Spatial Join Analysis

Sampling sites were spatially joined to watershed polygons using a point-in-polygon spatial join.
This allowed each sampling location to be assigned to a specific watershed.
Key Finding

The Qu’Appelle watershed contained the highest number of sampling sites, suggesting a higher probability of contamination transport within this drainage system.



Key GIS Concepts Demonstrated

This project demonstrates several important GIS and geospatial data science techniques:

Coordinate Reference Systems

Ensuring spatial data uses a projection suitable for distance and area calculations.

Spatial Buffering

Creating zones around geographic features to represent influence or monitoring regions.

Spatial Joins

Linking geographic features based on spatial relationships.

Watershed Analysis

Understanding how water movement influences environmental contamination transport.

Technologies Used

Python geospatial ecosystem:
GeoPandas
Shapely
Matplotlib
Pandas
NumPy
Potential Future Improvements

Possible extensions to this project include:
	•	Using real hydrological watershed datasets
	•	Integrating Digital Elevation Models (DEM) to compute true drainage basins
	•	Adding hydrological flow modeling
	•	Incorporating real environmental monitoring data
	•	Creating interactive maps using Folium or Plotly

⸻

Author

Dawson Conlon







