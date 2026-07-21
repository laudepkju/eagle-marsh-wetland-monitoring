# Models used for this project

## Pre-processing of Sentinel-2 images :artificial_satellite:

This creates a new file Geodatabase, makes a copy of the image into it, along with a feature class of the boundary of the natural reserve 🖼️


![Eagle Marsh GIS Import Rasters model](models/Import_Rasters.PNG)


This clips the raster images to the feature layer and resamples each image to a 10m resolution, naming it accordingly to the process ✂️


![Eagle Marsh GIS Clip Resample model](models/Cut_Resample.PNG)


A raster function was created for temporally comparing two images and calculating the wetness gain, remapping them into a designated threshold and applying focal statistics for readability :bar_chart:


![Eagle Marsh GIS Raster Function MNDWI](models/RF_GananciaMNDWI.PNG)

Now the resulting areas are converted into vector polygons, clipped to the area, and a specific symbology is applied :artist:

![Eagle Marsh GIS Polygon Gains](models/Polygon_Gains.PNG)
