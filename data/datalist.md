# Data folder – Wetland suitability modelling

This folder contains all spatial datasets used for generating suitability maps for **in-stream wetland placement**, including input rasters and vector layers.

## Input vector layers

- `E_306_margala_a.gpkg` – Existing wetland polygons  
- `E_203_vooluveekogu_j.gpkg` – Water bodies (lines: rivers, streams, ditches)  
- `E_203_vooluveekogu_a.gpkg` – Water bodies (polygons: lakes, wide channels)  
- `wetland_points.gpkg` – Random points generated within existing wetlands  
- `no_wetland_points.gpkg` – Random points within stratified non-wetland polygons  
- `stratified_no_wetland_polygon.gpkg` – Balanced non-wetland sampling polygons

## Raster files by source and resolution

Each environmental variable is provided at **two spatial resolutions (10 m and 50 m)** and from **two data sources**:

- `_a.tif` suffix → Local data source  
- `_GEE_a.tif` suffix → Global data source (Google Earth Engine)

| Variable            | Example (Local 50 m)            | Example (Global 50 m)           |
|---------------------|----------------------------------|----------------------------------|
| Slope               | `slope_50m_a.tif`                | `slope_50m_GEE_a.tif`            |
| Flow Accumulation   | `flow_acc_50m_a.tif`             | `flow_acc_50m_GEE_a.tif`         |
| TWI                 | `twi_50m_a.tif`                  | `twi_50m_GEE_a.tif`              |
| Clay Content        | `clay_50m_a.tif`                 | `clay_50m_GEE_a.tif`             |
| Soil Organic Carbon | `soc_50m_a.tif`                  | `soc_50m_GEE_a.tif`              |

Equivalent versions exist at 10 m resolution using `_10m_` in the filename.

## Derived data

- Final suitability outputs:
  - `ML_suitability_50m_local_final.tif`  
  - `AHP_local_50m_final.tif`

## notes

- All raster files are aligned and projected to the same CRS for consistency in analysis.
- If using data at a different resolution or source, update filenames accordingly in the notebooks.
