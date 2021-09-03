.. gcs_gui_documentation documentation master file, created by
   sphinx-quickstart on Tue Jul 20 14:44:16 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

GCS GUI documentation
+++++++++++++++++++++
This webpage includes the documentation for the Geomorphic Covariance Structure (GCS) analysis GUI, 
https://github.com/xaviernogueira/gcs_gui 

Included files
==============
- Graphic user interface executable script, *gcs_gui.py*
- Python files defining GUI implemented function/methods
- Copy of RapidLasso's LAStools software, http://lastools.org/
- Copy of 'Breeze' GUI theme, https://github.com/MaxPerl/ttk-Breeze

Pre-requisite packages
======================
- ``arcpy`` 

.. attention:: ``arcpy`` must be associated with a valid ArcPro license. The GUI must be ran using a `clone of the default ArcPro Python 3 environment <https://pro.arcgis.com/en/pro-app/latest/arcpy/get-started/work-with-python-environments.htm>`_! 

- ``pillow``

  * https://python-pillow.org/
- ``plotly``
  
  * https://plotly.com/
- ``seaborn``

  * https://seaborn.pydata.org/
  * - ``plotly``

  * https://plotly.com/python/
- ``openpyxl``

  * https://openpyxl.readthedocs.io/ 


All non- ``arcpy`` packages can be installed to the `cloned ArcPro Python environment <https://pro.arcgis.com/en/pro-app/latest/arcpy/get-started/work-with-python-environments.htm>`_
by simply using the ArcPro Python Package Manager or via ``conda`` in the command line::

    $ conda activate ...\ESRI\conda\envs\arcgispro-py3-clone\python.exe  
    $ conda install pillow
    $ conda install plotly
    $ conda install seaborn
    $ conda install plotly
    $ conda install openpyxl

.. _Setting up:
Setting up 
==========
Create a folder containing following:

- LAS/LAZ point cloud data files with spatial extents/footprint that capture a river valley's in-channel topography. Either bathymetric LiDAR or traditional LiDAR collected during dry channel conditions.
- Any shapefile (.shp) from the LiDAR project's metadata that has a spatial reference frame matching the point cloud data. Can also be manually created based on project metadata files.
- A shapefile (.shp) defining the analysis area of interest (AOI). Projected in a spatial reference frame with desired analysis units (Meters or US Feet)This shapefile's spatial reference is applied to all output files.
- A folder (within the top level directory) containing only 4-band, 1m- resolution NAIP imagery .jp2 files that cover the AOI.

Bugs and errors
=================================
Do not hesitate to contact xavier.rojas.nogueira@gmail.com with bug reports, errors, or other feedback. 
We will try to respond expeditiously, and update the software when necessary.

.. toctree::
   :maxdepth: 2
   :caption: Processing steps

   Pages/tab1
   Pages/tab2
   Pages/tab3
   Pages/tab4
   Pages/tab5
   Pages/tab6
   Pages/tab7
   Pages/tab8
   Pages/tab9
   

.. toctree::
   :maxdepth: 2
   :caption: Information

   Pages/fcr_theory
   Pages/literature
   Pages/glossary
   Pages/acknowledgements


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
