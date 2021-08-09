Generating a thalweg centerline + elevation profile
+++++++++++++++++++++++++++++++++++++++++++++++++++
A :term:`thalweg` centerline is generated using a smoothed version of the :term:`topo-bathymetric DEM`. Elevation values are sampled 
along the centerline at 1m intervals, and used to generate a thalweg elevation profile CSV file.

Inputs
======

- **USER GENERATED:** An upstream flow polygon that intersects the thalweg centerline
  
    * This defines the top of the thalweg longitidnal elevation profile
    * Generate manually in ArcPro or ArcGIS, define projection to match the thalweg centerline!
- The area of interest (AOI) shapefile
- Number of low pass filter runs to smooth topography with (15 is default)
- PAEK centerline smoothing distance / 'tolerance' in meters 
  
    * 6 m is the default  
    * PAEK: Polynomial Approximation with Exponential Kernel
    .. note:: For more information on the PAEK smoothing algorithm see ESRI's documentation (https://pro.arcgis.com/en/pro-app/latest/tool-reference/cartography/smooth-line.htm)

.. warning::  Please verify centerline quality, and edit if necessary, before generating the thalweg elevation profile.

Relevant outputs
================

- Smooth thalweg centerline, *thalweg_centerline.shp*
- Thalweg elevation profile CSV file, *xyz_elevation_table.csv*

Applied method flow chart
=========================

.. image:: images/tab3_flow_chart.png
   :width: 500