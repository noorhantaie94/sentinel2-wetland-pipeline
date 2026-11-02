# Sentinel-2 Wetland Classification (Iraqi Marshes)

A Python implementation for Land Use / Land Cover (LULC) classification over the Iraqi Marshes using Sentinel-2 satellite imagery.

The project queries Sentinel-2 data via STAC API, computes spectral indices (NDVI and MNDWI), and applies a Random Forest model to classify surface water, vegetation, and bare soil.

## Pipeline Steps
1. **Data Access**: Query Sentinel-2 L2A data via `pystac-client` and Microsoft Planetary Computer.
2. **Preprocessing**: Windowing over bbox coordinates and resampling spectral bands.
3. **Feature Extraction**: Compute NDVI (vegetation) and MNDWI (water).
4. **Classification**: Train a `RandomForestClassifier` on extracted spectral features.
5. **Output**: Save results as a georeferenced GeoTIFF (`marsh_lulc_classification.tif`).

## Structure
* `01_synthetic_demo.py`: Algorithm prototype using synthetic spatial data.
* `02_sentinel2_wetland_pipeline.ipynb`: Main notebook running on real Sentinel-2 imagery.

## Requirements
`pystac-client`, `planetary-computer`, `rasterio`, `geopandas`, `scikit-learn`, `matplotlib`
