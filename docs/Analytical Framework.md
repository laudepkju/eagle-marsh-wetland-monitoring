# Analytical Framework

## Overview

The Eagle Marsh Wetland Monitoring project was designed as an integrated Geographic Information System (GIS) for monitoring seasonal moisture variation, supporting ecological management, and improving maintenance planning within the Eagle Marsh Nature Preserve in Fort Wayne, Indiana.

Rather than focusing on a single remote sensing analysis, the project combines satellite imagery, terrain analysis, spatial modeling, enterprise geodatabase design, and ArcGIS Online applications into a repeatable monitoring workflow. The framework was developed to support future environmental assessments while providing practical tools for park managers, maintenance personnel, and volunteers.

---

# Project Objectives

The analytical framework was developed around four primary objectives:

- Monitor seasonal changes in wetland moisture using satellite imagery.
- Identify areas susceptible to water accumulation through spatial analysis.
- Support infrastructure maintenance using an enterprise GIS asset inventory.
- Improve decision making through interactive web applications and dashboards.

Together, these components create a workflow capable of supporting long-term environmental monitoring while reducing manual processing and improving operational efficiency.

---

# Solution Architecture

The project integrates multiple GIS technologies into a single monitoring framework.

```
                Data Collection
                       │
        ┌──────────────┼──────────────┐
        │              │              │
  Sentinel-2        Indiana DEM    LiDAR
        │              │              │
        └──────────────┼──────────────┘
                       │
                Data Preparation
                       │
         Clipping • Resampling • Geodatabase
                       │
              Spatial Analysis Models
                       │
        NDWI • MNDWI • Terrain Analysis
                       │
             Moisture Change Detection
                       │
        Raster Classification & Polygons
                       │
              Decision Support Products
                       │
 StoryMap • Dashboard • Workforce • Field Maps
```

The analytical workflow follows a modular design, allowing each processing stage to be updated independently as new satellite imagery or field observations become available.

---

# Environmental Analysis Workflow

Seasonal monitoring begins with Sentinel-2 multispectral imagery acquired during representative dry and wetter conditions.

After importing the imagery into the project geodatabase, raster preprocessing includes clipping the imagery to the Eagle Marsh study area and resampling the datasets to a common spatial resolution.

The processed imagery is then used to calculate spectral water indices:

- Normalized Difference Water Index (NDWI)
- Modified Normalized Difference Water Index (MNDWI)

To improve interpretation, a custom raster function compares moisture conditions between acquisition dates, identifying areas that gained or lost surface moisture over time.

The resulting raster is classified into meaningful moisture categories before being converted into polygons for additional spatial analysis.

This approach creates a repeatable workflow capable of monitoring environmental change using future satellite imagery with minimal modifications.

---

# Terrain and Hydrologic Context

Remote sensing results are complemented using additional geospatial datasets that provide environmental context.

Digital Elevation Model (DEM) data is used to derive slope and better understand the influence of terrain on water accumulation.

Hydrologic Unit Code (HUC-12) watershed boundaries provide regional hydrologic context, while LiDAR-derived elevation data supports three-dimensional visualization of the landscape.

Together, these datasets improve interpretation of the moisture analysis by relating observed changes to topography and hydrologic processes.

---

# Asset Management Workflow

Environmental monitoring represents only one component of the overall system.

A geodatabase was designed to manage park infrastructure including trails, bridges, observation platforms, bird nests, benches, signage, and other maintenance assets.

Feature classes, domains, subtypes, and relationship classes were implemented to standardize data collection and improve inventory consistency.

This structure allows field observations to be associated with individual assets while supporting long-term maintenance history and condition tracking.

The resulting database provides a scalable foundation for future inspections and asset management activities.

---

# Decision Support Applications

The analytical framework extends beyond desktop GIS by integrating ArcGIS Online applications that support day-to-day park operations.

**Field Maps** enables standardized field data collection.

**Workforce** supports task assignment and coordination between maintenance personnel and volunteers.

**Dashboards** summarize maintenance priorities, work status, and asset conditions through interactive indicators and maps.

Finally, an **ArcGIS StoryMap** communicates the ecological importance of Eagle Marsh to the general public using interactive maps, imagery, and visual storytelling instead of technical language.

Together, these applications transform analytical results into practical management tools.

---

# Integrated Monitoring Framework

The project was designed as a repeatable monitoring system rather than a one-time analysis.

As new Sentinel-2 imagery becomes available, the workflow can be executed again using the existing ModelBuilder models and raster functions to generate updated moisture comparisons.

Because each processing stage is modular, additional remote sensing indices, new environmental datasets, or field observations can be incorporated without redesigning the overall workflow.

This scalability makes the framework suitable for long-term wetland monitoring while supporting adaptive management strategies.

---

# Project Deliverables

The completed framework produces a series of complementary GIS products:

- ArcGIS Pro project
- Automated ModelBuilder workflows
- Custom raster function for temporal moisture comparison
- Moisture gain and loss analysis
- Terrain and slope analysis
- Enterprise geodatabase for asset management
- ArcGIS Dashboard
- ArcGIS StoryMap
- Workforce project
- Field Maps project
- Technical documentation and GitHub repository

Together, these deliverables demonstrate how desktop GIS, remote sensing, enterprise geodatabases, and web GIS applications can be integrated into a comprehensive decision-support system for environmental management.
