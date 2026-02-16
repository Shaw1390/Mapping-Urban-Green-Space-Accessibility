# Mapping Urban Green Space Accessibility: Vancouver Case Study

![Vancouver Map](https://img.shields.io/badge/Project-GIS%20Analysis-green)
[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![OSMnx](https://img.shields.io/badge/Library-OSMnx-orange)](https://osmnx.readthedocs.io/)
[![GeoPandas](https://img.shields.io/badge/Library-GeoPandas-150458?logo=pandas&logoColor=white)](https://geopandas.org/)

## 📌 Project Overview
This project provides a quantitative analysis of urban green space accessibility in Vancouver, BC. Using Python's geospatial ecosystem, I modeled the walking network and proximity of residential areas to public parks and green spaces. 

The primary goal is to identify **"green gaps"**—areas where residents lack easy access to nature—to support data-driven urban planning and environmental equity.

## 🚀 Key Features
* **Automated Data Acquisition**: Programmatically retrieved street networks and land-use data (parks, grass, forests) using the `OSMnx` library.
* **Network Analysis**: Built a walkable graph network to simulate realistic pedestrian movement rather than simple "as-the-crow-flies" Euclidean distances.
* **Spatial Join & Proximity Modeling**: Calculated precise distances from residential centroids to the nearest green space using `GeoPandas` and `Shapely`.
* **Interactive Visualization**: Developed interactive web maps using `Folium` to visualize accessibility clusters and specific "service deserts."
* **Statistical Profiling**: Generated a summary report on population coverage within 300m, 500m, and 1km thresholds.

## 🛠️ Tech Stack
* **Language:** Python
* **Geospatial Libraries:** * `GeoPandas`: Vector data manipulation and spatial joins.
    * `OSMnx`: Complex network analysis and OpenStreetMap integration.
    * `Shapely`: Geometric operations and distance calculations.
    * `PyProj`: Handling Coordinate Reference Systems (CRS) for accurate metric measurements (UTM Projection).
* **Visualization:** * `Folium`: Leaflet.js wrapper for interactive maps.
    * `Matplotlib`: Static network plots and data distribution charts.
    * `Contextily`: Integration of web map tiles for basemaps.

## 📊 Methodology
1.  **Data Extraction**: Defined a study area in Vancouver and fetched the walking network with a 2km buffer to avoid edge effects.
2.  **CRS Projection**: Re-projected data to a local projected coordinate system (UTM) to ensure distance calculations in meters were accurate.
3.  **Feature Engineering**: Filtered OSM geometries for specific tags (e.g., `leisure=park`, `landuse=grass`) to define "Green Space."
4.  **Accessibility Analysis**: 
    * Identified the nearest green space for each residential point.
    * Classified accessibility based on urban planning standards (e.g., the "300m rule").

<img width="748" height="798" alt="Image" src="https://github.com/user-attachments/assets/37266d6a-9a3a-4d36-856d-7e523c5a8f46" />


## 📈 Results & Insights
Based on the analysis of the study area:
* **High Accessibility**: **94.4%** of residents live within 300 meters of a green space.
* **Average Proximity**: Residents are, on average, only **0.06 km** away from their nearest park.
* **Urban Design**: The data suggests a highly integrated park system in the sampled district, with **0.0%** of residents living more than 1km from a green space.

![Image](https://github.com/user-attachments/assets/d2ce8d29-2ab5-4f00-904b-a4cea335b645)



## 🛠️ Installation & Usage
1.  **Clone the repo**:
    ```bash
    git clone [https://github.com/yourusername/vancouver-green-space.git](https://github.com/yourusername/vancouver-green-space.git)
    ```
2.  **Install dependencies**:
    ```bash
    pip install geopandas osmnx networkx matplotlib contextily folium shapely
    ```
3.  **Run the analysis**:
    Open `Mapping_Urban_Green_Space_Vancouver.ipynb` in Jupyter or Google Colab and run all cells.

## 🔮 Future Work
* **Topographical Impact**: Incorporate elevation data to account for slope-adjusted walking distances.
* **Demographic Overlay**: Join with census data to analyze accessibility equity across different socio-economic groups.
* **Temporal Analysis**: Compare green space growth against population density changes over the last decade.
