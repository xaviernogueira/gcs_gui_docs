Thalweg based DEM detrending
++++++++++++++++++++++++++++
Here we detrend the :term:`topo-bathymetric DEM` by applying a piecewise linear fit model to it's thalweg elevation profile.
This allows the resulting detrended DEM cell values to be a proxy for :term:`flow stage elevation` (Z).

Inputs
======

- The thalweg elevation profile .csv file, *xyz_elevation_table.csv*
- The generated topo-bathymetric digital elevation model, *las_dem.tif*
- **USER INPUT:** Thaleg elevation profile slope break points separated by commas

   * Separated by commas in ascending order 
   * i.e. *500,1000,1800,2900*
   * A tip for selecting slope breakpoints is to identify segments of linearity after plotting the residuals of a simple linear fit.
   .. note:: Selecting slope breakpoints is an iterative process. Do not detrend the DEM until the selected points produce a satisfactory piecewise linear fit model. See below.
   
Slope breakpoint selection example
==================================
We start by plotting a linear fit without breakpoints, and observing the residual plot:

.. image:: images/res1_ex.png
   :width: 500

As you can see, there are segments with considerable linearity at a scale greater 
than typical in-channel topographic heterogeniety. We mark these segments below.    

.. image:: images/res2_ex.png
   :width: 500

We then enter these slope breakpoints in the specified manner, and examine the quality of the piecewise linear fit. 

.. image:: images/linear_ex.png
   :width: 500

   .. image:: images/res3_ex.png
   :width: 500

In this case the quality of the fit seems suitable, and we have eliminated large scale linearity within the residual plot, therefore we could 
proceed to click the 'Detrend DEM!' button in the GUI.

.. important:: Sudden vertical jumps at the slope breakpoints will negatively effect the quality of your detrended DEM. Large scale residual trends (i.e. all positive residuals on one end of the channel, and all negative on the other) will substantial degrade GCS analysis quality. 

.. _detrend_error:

Relevant Outputs
================

- A detrended DEM in the same resolution as the input topo-bathymetric DEM, *ras_detren.tif*
- A text file recording chosen slope breakpoints and linear regression equations applied between them, *detrending_plots/detrending_fit_eqs.txt*
- A figure showing the plotted thalweg elevation profile and the piecewise linear regression model, *detrending_plots/fit_plot.png* 
- A figure showing the linear fit model residual values along the thalweg's longitudinal profile, *detrending_plots/residual_plot.png*



.. warning:: Wide, flat floodplains can cause erroneous artifacts of the detrendeding methodlogy to be observable, especially farther from the thalweg. 


Applied method flow chart
=========================

.. image:: images/tab4_flow_chart.png
   :width: 500
