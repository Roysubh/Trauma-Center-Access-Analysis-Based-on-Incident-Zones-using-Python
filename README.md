🏥 Trauma Center Access Analysis Based on Incident Zones

📄 Overview:
    This project, done entirely in Python, analyzes access to trauma centers in Kolkata, India, based on multiple incident points and multiple trauma center locations. Using open-source geospatial tools and network analysis, the pipeline computes shortest-path distances and travel times from each incident point to all trauma centers, generating a multi-origin multi-destination (OD) cost matrix. Routes are classified into Safe, Warning, and Danger zones based on travel time, and results are visualized in interactive maps. The workflow integrates data collection, geospatial processing, OD computation, and GIS-ready outputs.

📊 Project Specifications:
| Attribute              | Details                                                                     |
| ---------------------- | --------------------------------------------------------------------------- |
| **Title**              | Trauma Center Access Analysis Based on Incident Zones                       |
| **Study Area**         | Kolkata, West Bengal, India                                                 |
| **Data Sources**       | OpenStreetMap (roads & hospitals), simulated multi-point incident locations |
| **Platform**           | **Python** (GeoAI / GIS Analysis)                                           |
| **Spatial Resolution** | Road network-level                                                          |
| **Sample Type**        | Multi-point incident locations                                              |
| **Analysis**           | Network-based **multi-origin multi-destination OD cost matrix** computation |
| **Output Formats**     | GeoPackage (GPKG), CSV, interactive Folium HTML maps                        |
| **Validation Metrics** | Travel time-based zone classification                                       |

⚙️ Dependencies:
    Install required packages: osmnx geopandas networkx folium shapely numpy scipy tqdm pandas
    
| Library               | Purpose                                             |
| --------------------  | ----------------------------------------------------|
| **osmnx**             | Download road network & POIs from OpenStreetMap     |
| **geopandas**         | Handling geospatial vector data (roads, points)     |
| **networkx**          | Build road network graph & shortest path analysis   |
| **folium**            | Interactive map visualization                       |
| **numpy** / **scipy** | Numerical operations & KD-tree snapping             |
| **pandas**            | Tabular data management                             |
| **shapely**           | Geometry handling (points, lines)                   |
| **tqdm**              | Progress bar for loops                              |

🚀 Workflow:
A[🎯 Define Objective] → B[🗺️ Download Road & Hospital Data] → C[📍 Generate Multi-Point Incident Locations]
C → D[🧭 Snap Points to Road Network & Build Graph] → E[📏 Compute Multi-Origin Multi-Destination OD Cost Matrix]
E → F[🛣️ Classify Routes into Safe / Warning / Danger Zones] → G[📤 Export GeoPackage + CSV]
G → H[🗺️ Visualize in Folium Interactive Map]

📌 Key Parameters:
| Parameter        | Value      | Description                                         |
| ---------------- | ---------- | --------------------------------------------------- |
| **num_points**   | 1000       | Number of simulated incident points along roads     |
| **min_distance** | 10 m       | Minimum distance between incident points            |
| **speed_kmh**    | 40 km/h    | Constant speed assumed for travel time calculation  |
| **CRS**          | EPSG:32645 | Metric projection for accurate distance calculation |

📈 Evaluation Metrics:
    Travel Time Zones:
      Safe Zone: ≤ 20 min travel time
      Warning Zone: 20–30 min
      Danger Zone: > 30 min
    Unreachable: No path available from incident point to trauma center
    OD Cost Matrix: Multi-origin to multi-destination travel times, distances, and zone classification

📦 Final Outputs:
| Output Type       | Format     | Description                                                                      |
| ----------------- | ---------- | -------------------------------------------------------------------------------- |
| Roads & Hospitals | GeoPackage | Vector layers with attributes                                                    |
| Incident Points   | GeoPackage | Simulated multi-point incidents along roads                                      |
| OD Cost Matrix    | CSV        | Distances, travel time, and zone classification for all origin-destination pairs |
| OD Routes by Zone | GeoPackage | Safe / Warning / Danger routes with origins and destinations                     |
| Interactive Map   | HTML       | Folium map showing roads, hospitals, incident points, and OD routes              |

⚡ Highlights:
      Done entirely in Python with open-source geospatial libraries
      End-to-end geospatial analysis pipeline from multi-point incidents to trauma center access mapping
      Computes multi-origin multi-destination OD cost matrices using network analysis
      Provides zone-based trauma accessibility mapping for decision support
      GIS-ready outputs for further analysis in QGIS/ArcGIS
      Interactive visualization of incident points, trauma centers, and routes by zone

✍️ Author: Subham Roy ✨🌟
    📧 Email: subhamofficwork@gmail.com 
    🔗 LinkedIn: https://www.linkedin.com/in/subham-roy-601867167/ 
    📚 Google Scholar: https://scholar.google.com/citations?user=bTxDrQgAAAAJ&hl=en 
    📝 ResearchGate: https://www.researchgate.net/profile/Subham-Roy-14

✅ Conclusion:
  This project demonstrates a comprehensive Python-based geospatial workflow for analyzing trauma center accessibility from multiple incident points. By integrating open-source road network data, simulated incident locations, and hospital POIs, we were able to:
  Compute multi-origin multi-destination OD cost matrices
  Classify routes into Safe, Warning, and Danger zones based on travel time
  Produce GIS-ready outputs for spatial analysis and planning
  Generate interactive visualizations for quick insights
  
  The workflow supports decision-making for emergency response, trauma care planning, and urban health infrastructure assessment. It also provides a reusable framework for similar accessibility studies in other urban areas.


