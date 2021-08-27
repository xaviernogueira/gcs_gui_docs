Prepping LiDAR data from processing
+++++++++++++++++++++++++++++++++++++++++++
LiDAR data point files are prepared for LAStools vegetation point removal. NAIP imagery is used to generate a NDVI raster and create a polygon representing non-vegetated bare-ground.

Inputs
=======

- The directory containing river valley LiDAR point cloud files (:ref:`Setting up`)
- The directory containing NAIP imagery (:ref:`Setting up`)
- A shapefile with the LiDAR project's spatial reference frame (see 'Setting up')
- A shapefile defining the area of interest in the desired output spatial reference frame (:ref:`Setting up`)
  
    * This shapefile should be manually edited to somewhat tightly surround the river channel and flood-plain.
    * Do not exclude any areas that could be submerged under flood stage flows, but excess AOI coverage will substantially slow the LiDAR processing step.
    * Define the shapefile's spatial reference frame (including vertical). This will be the reference frame of all output files, and defines the units used within the analysis.
- NDVI threshold (default is 0.4)
  
    * NDVI = Normalized Difference Vegetation Index, https://en.wikipedia.org/wiki/Normalized_difference_vegetation_index
    * The threshold corresponds to the minimum NDVI value that gets defined as vegetation.
    * In arid regions, lower values may be required (0.15-0.3).
    .. note:: Inspect the 'veg_poly.shp' file within the output folder. Verify vegetation mask quality. Adjust NDVI value and run again if necessary.

Relevant outputs
==================

- A shapefile representing bare-ground, *ground_poly.shp*
- A shapefile representing the LiDAR data extent, *las_footprint.shp*

Applied method flow chart
=========================

.. image:: images/tab1_flow_chart.png
   :width: 500

Example of a correctly set up input directory
=============================================

.. image:: images/set_up_folder.png
   :width: 500