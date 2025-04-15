# Geo-AI-project
## 🌍 GeoVision: AI-Powered Land Use Classification from Satellite Imagery
📌 Project Overview
GeoVision is a GeoAI project that leverages deep learning to classify land use and land cover (LULC) from real satellite imagery. This end-to-end pipeline uses Sentinel-2 satellite data, processes it into tiles, classifies each tile using a custom CNN model, and visualizes the results as an interactive geospatial map using GeoJSON and Folium.

🔧 Technologies & Tools Used
🛰️ Satellite Data: Sentinel-2 (RGB bands)

Model: Custom Convolutional Neural Network (CNN)

Geo Formats: GeoTIFF, GeoJSON

Visualization: Folium (interactive mapping)

Python Libraries: rasterio, torch, torchvision, numpy, Pillow, folium, geopandas

Key Features
Download and preprocess real Sentinel-2 satellite image patches.

reak large satellite images into 64x64 tiles for efficient classification.

Train and apply a CNN to perform multi-class land cover classification (e.g., urban, water, forest).

Generate predictions.geojson with predicted class for each tile.

Visualize results on an interactive map, with color-coded polygons and class popups.

Workflow Summary
Satellite Image Loading
Load and visualize Sentinel-2 GeoTIFF imagery.

Tile Extraction
Divide large images into smaller patches (64×64 px) for model input.

CNN Training & Inference
Train the model on labeled patches or use a pretrained dummy model for demo.

GeoJSON Generation
Associate predictions with spatial coordinates and export as GeoJSON.

Interactive Map Visualization
Overlay predictions on a Folium map for intuitive inspection.

📊 Example Output

Each tile represents a classified land cover type like urban, forest, water, etc.

📁 Folder Structure  (find other files in this ZIP folder - https://drive.google.com/file/d/1JGwt7-4oFbaimpEqrJVO7IsL5m19Ew3B/view?usp=sharing)

GeoVision/
│
├── libraries/                 # Contains main code , notebook file
├── model.pth/                # saved CNN trained model
├── predictions.geojson              # .geojson file

✅ How to Run
Clone this repo:
git clone https://github.com/yourusername/GeoVision.git

Install dependencies:

bash
Copy
Edit
pip install geopandas fiona shapely pyproj rasterio folium psycopg2-binary sqlalchemy 
Open and run the notebook:
libraries.ipynb

📌 Use Cases
Urban sprawl analysis

Forest and deforestation mapping

Agricultural land monitoring

GeoAI prototypes for smart city and environment planning
