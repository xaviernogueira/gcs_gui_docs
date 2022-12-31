.. gcs_gui_documentation documentation master file, created by
   sphinx-quickstart on Tue Jul 20 14:44:16 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

GCS GUI documentation
+++++++++++++++++++++
This webpage includes the documentation for the Geomorphic Covariance Structure 
(GCS) Analysis Tools Graphic User Interface (GUI).

You can find the repository `here <https://github.com/xaviernogueira/GCS-Analysis-Tools>`_.

Included files
==============

- Graphic user interface executable script, *gui_tkinter.py*
- Python files defining GUI implemented function/methods.
- A copy of pre-requisite executables from RapidLasso's `LAStools <http://lastools.org/>`_.
- A copy of the 'Breeze' GUI `theme <https://github.com/MaxPerl/ttk-Breeze>`_.

Pre-requisite packages
======================
- ``arcpy`` with a valid Spatial Analyst license.

.. attention:: The GUI must be ran using a `clone of the default ArcPro Python 3 environment <https://pro.arcgis.com/en/pro-app/latest/arcpy/get-started/work-with-python-environments.htm>`_! 

- ``scipy``
- ``pillow`` - https://python-pillow.org/
- ``plotly`` - https://plotly.com/
- ``seaborn`` - https://seaborn.pydata.org/
- ``openpyxl`` - https://openpyxl.readthedocs.io/ 


All non- ``arcpy`` packages can be installed to the `cloned ArcPro Python environment <https://pro.arcgis.com/en/pro-app/latest/arcpy/get-started/work-with-python-environments.htm>`_
by simply using the ArcPro Python Package Manager or via ``conda`` in the command line::

    $ conda activate ...\ESRI\conda\envs\arcgispro-py3-clone\python.exe
    $ conda install -c conda-forge scipy
    $ conda install -c conda-forge pillow
    $ conda install -c conda-forge plotly
    $ conda install -c conda-forge seaborn
    $ conda install -c conda-forge openpyxl

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
I would appreciate if all bugs and feature requests be made via out GitHub Issues page_.
.. _page: https://github.com/xaviernogueira/GCS-Analysis-Tools/issues

If you prefer a more direct approach, do not hesitate to contact me via email at 
xavier.rojas.nogueira@gmail.com with bug reports, questions, or other feedback.

I will try to respond expeditiously, and update the software when necessary.

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
