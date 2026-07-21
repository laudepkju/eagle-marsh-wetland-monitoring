# Models used in this project

## Sentinel-2 image Pre-processing :artificial_satellite:

### 1. Create the Project Geodatabase ℹ️

Create a new File Geodatabase, copy the Sentinel-2 imagery into it, and imports the Eagle Marsh boundary feature class for subsequent processing.

![Eagle Marsh GIS Import Rasters model](images/Import_Rasters.PNG)


### 2. Clip and Resample Imagery ✂️

Clips the Sentinel-2 imagery to the Eagle Marsh boundary and resamples each raster to a 10-meter spatial resolution, generating standardized datasets for later analysis.

![Eagle Marsh GIS Clip Resample model](images/Cut_Resample.PNG)


## Image analysis 🔍

### 1. Wetness Change Detection (MNDWI) 💧

A custom raster function compares two Sentinel-2 images acquired at different dates to calculate changes in wetness using the Modified Normalized Difference Water Index (MNDWI).

The workflow:

Calculates the MNDWI
Applies threshold remapping
Uses Focal Statistics to improve raster readability
Produces a raster representing areas of wetness gain

![Eagle Marsh GIS Raster Function MNDWI](images/RF_GananciaMNDWI.PNG)


### 2. Vectorization of Wetness Gain Areas

The resulting raster is converted into vector polygons, clipped to the project boundary, and symbolized for visualization and area calculations

![Eagle Marsh GIS Polygon Gains](images/Polygon_Gains.PNG)


## Importing Assets from ArcGIS Field Maps 🗺️

The hosted feature layer created in ArcGIS Field Maps is imported into the local project geodatabase while preserving:

Attachments
Domains
Attribute information
Related tables

This workflow enables offline analysis while maintaining the original data structure.

![Eagle Marsh AGOL Local assets](images/AGOL_Local.PNG)
