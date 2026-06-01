# Orlando Tourist Corridor Infrastructure & Asset Management Suites

This repository houses two technical geospatial engineering and data operations portfolios focusing on urban infrastructure, asset tracking, and stormwater management systems within the high-traffic tourist corridors of Orlando, Florida.

---

## 🛠️ Project 1: Orlando Tourist Corridor Stormwater Infrastructure & Drainage Mapping Suite

### Project Overview
Developed an interactive spatial mapping application designed to isolate, audit, and analyze secondary drainage networks and localized stormwater vulnerabilities surrounding the high-traffic tourist routes near Universal Orlando Resort. 

### Methodology & Execution Steps
1. **Data Acquisition & Environment Setup:** Leveraged the Orange County Government GIS Open Data Hub to acquire primary infrastructure feature layers, including `Stormwater Pipes` and `Stormwater Structures` (culverts, inlets, and catch basins).
2. **Spatial Isolation:** Imported raw vector layers into QGIS and established an OpenStreetMap spatial basemap. Used advanced querying and geometric filtering to clip and isolate datasets within a localized 2-mile radius of the Universal Orlando Resort hub.
3. **Data Quality Control & Validation:** Conducted systematic attribute checks within the data pipelines to locate missing schema values, unlinked vertices, or size discrepancies. Manually updated missing pipe diameters and converted civil drawing annotations into precise digital sketches to guarantee absolute database integrity.
4. **Deliverable Production:** Generated a cartographic layout sheet utilizing the QGIS Print Layout engine, integrating proper scale parameters, localized coordinate grids, and an engineering index.

### Repository Assets
* `/QGIS-stormwater/universal_stormwater_map.qgx` - Final high-resolution map layout document.
* `/QGIS-stormwater/universal_pipes.shp` - Cleaned and verified stormwater pipe geometric data.
* `/QGIS-stormwater/universal_structures.shp` - Audited stormwater structure points.

---

## 🛣️ Project 2: International Drive & Disney Area Roadway Asset Management Visualizer

### Project Overview
Programmed an open-source data analysis dashboard and interactive web application linking tabular spreadsheet data to a live map canvas. This application enables cross-functional maintenance crews to filter, index, and review roadway degradation metrics (such as pavement cracking, structural damage, and potholes) across the corridors leading to Walt Disney World.

### Methodology & Execution Steps
1. **Application Architecture:** Developed the full application layout in Python using Visual Studio Code (VS Code), leveraging the Streamlit web framework and Folium for geospatial map rendering.
2. **Data Integration Pipeline:** Built an automated data handler to simulate a spreadsheet input pipeline, converting standard tabular columns (Asset ID, Street Name, Coordinates, Degradation Type, Severity) into interactive geospatial marker layers.
3. **UI/UX Engineering & Control Constraints:** Created a structural sidebar component using Streamlit's state filters, allowing users to actively isolate specific degradation threats by severity (High, Medium, Low). 
4. **Dynamic Map Customization:** Configured a conditional logic engine to style marker nodes dynamically (e.g., severe pavement failures render as high-visibility red nodes) centered directly over the dynamic I-Drive / resort transportation network junctions.
5. **Electronic Document Indexing:** Integrated an interactive data log matrix connected to an export framework, giving administrative reviewers the ability to download filtered database records instantly as a clean CSV file.

### How to Run the Dashboard Locally
Ensure you have Python installed, clone this directory, and execute the following commands in your terminal:
```bash
# Install the required web and mapping frameworks
pip install streamlit pandas folium streamlit-folium

# Launch the interactive local server
streamlit run app.py
