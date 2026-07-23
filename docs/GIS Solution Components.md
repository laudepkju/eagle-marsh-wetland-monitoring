# GIS Solution Components

The completed framework produces a series of complementary GIS products:

##  🖥️ ArcGIS Pro project

The ArcGIS Pro project serves as the central workspace for data management, spatial analysis, cartographic production, and geoprocessing. It integrates all project datasets, maps, models, and layouts into a single environment that supports the complete analytical workflow.

<p align="center">
  <img src="../images/ArcGISPRO_Project.PNG" width="850">
</p>


## ⚙️ Automated ModelBuilder workflows

ModelBuilder automates the preprocessing of Sentinel-2 imagery, including clipping, resampling, and raster preparation. These workflows reduce manual processing time, improve consistency, and enable the analysis to be repeated whenever new imagery becomes available.

<p align="center">
  <img src="../models/AGOL_Local.PNG" width="900">
</p>
  
## 🛰️ Custom raster function for temporal moisture comparison

A custom raster function compares moisture conditions between satellite acquisition dates by calculating temporal changes in the Modified Normalized Difference Water Index (MNDWI). This modular approach enables rapid processing without permanently generating intermediate datasets.

<p align="center">
  <img src="../models/RF_GananciaMNDWI.PNG" width="450">
</p>
  
## 🌿 Moisture Gain and Loss Analysis

The temporal comparison identifies areas where surface moisture has increased or decreased between acquisition dates. The resulting maps support the interpretation of seasonal hydrologic dynamics and provide the basis for subsequent spatial analyses.

<p align="center">
  <img src="../images/8_MNDWI_Ganacia_Assets-text.PNG" width="850">
</p>

## ⛰️ Terrain and Slope Analysis

Digital Elevation Model (DEM) data was used to derive terrain characteristics and slope gradients, providing additional context for interpreting water accumulation patterns and understanding the hydrologic behavior of the wetland.

<p align="center">
  <img src="../images/EM_Pendiente.png" width="850">
</p>

  
## 🗃️ Enterprise Geodatabase

The geodatabase was designed to manage park assets using standardized domains, subtypes, and relationship classes. This structure improves data integrity while supporting maintenance history, inspections, and long-term asset management.

<p align="center">
  <img src="../images/4_Domains.png" width="800">
</p>

## 📊 ArcGIS Dashboard

The dashboard consolidates maintenance activities, asset conditions, and operational metrics into a single interface. Interactive maps, indicators, charts, and filters allow managers to quickly identify priorities and monitor ongoing work.

<p align="center">
  <img src="../images/7_dashboard.PNG" width="900">
</p>


## 🌐 ArcGIS StoryMap

The StoryMap communicates the ecological importance of Eagle Marsh through interactive maps, imagery, and narrative content. It was designed for a general audience, translating technical analyses into an accessible and engaging experience.

<p align="center">
  <img src="../images/EM_storymap_cover.PNG" width="850">
</p>


## 👷 Workforce Project

ArcGIS Workforce coordinates maintenance assignments by linking field personnel with specific tasks and park assets. The application supports real-time task tracking and improves communication between managers and field crews.

<p align="center">
  <img src="../images/Mantenimiento_mapa.PNG" width="850">
</p>


## 📱 Field Maps

Field Maps provides a standardized workflow for collecting infrastructure inventory and inspection data directly from mobile devices. The application improves data quality while reducing the need for manual transcription and post-processing.

<p align="center">
  <img src="../images/Fieldmap_assets.PNG" width="350">
</p>

## 📚 Technical Documentation

The repository includes detailed technical documentation describing the analytical framework, data preparation, geoprocessing models, and system architecture. Together, these documents enable the workflow to be understood, reproduced, and extended by other GIS professionals.
