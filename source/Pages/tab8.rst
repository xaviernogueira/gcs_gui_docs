GCS nesting analysis outputs
+++++++++++++++++++++++++++++

Methodology + motivation
------------------------

* Cross-sections along each of the selected flow stage centerlines are *aligned* to the longest centerline path (typically the lowest flow stage) based on Euclidian distance. 
* Ws, Zs, C(Ws, Zs) values are aligned for all flow stages, faciliating comparison.  
* GCS nesting analysis attempts to capture the `nested hierarchical topographic structure <https://onlinelibrary.wiley.com/doi/10.1002/esp.4411>`_ of the study river.
* Nesting patterns associated with landforms can be provide insight into which flow stages (and their respective discharges) contribute to maintaining desirable aspects of channel topography such as :term:`riffle-pool sequences`, or heterogeneity broadly. 


Outputs 
--------

**Directory Location:** By default all nesting analysis outputs are saved @ *GCS_analysis_outputs/nesting_analysis/*.


**Visual Outputs:**

Static *.png* plots visualizing Ws, Zs, and C(Ws, Zs) series where each flow stage 
is stacked in a single plot, i.e., *Ws_nesting_gcs_plots.png* (see example below).
    .. image:: images/Ws_nesting_gcs_plots.png
        :width: 500

Interactive HTML "Sankey Diagrams" visualizing cross-section landform 
transitions between each increasing flow stage. The code outputs one with 'normal' 
cross-sections included, and another focusing only on non-normal GCS landforms (see the static example below).
    .. image:: images/hover_gcs_sankey.png
        :width: 500

**Tabular Ouputs:**

- A *.csv* table with Chi-squared significance levels associated for all landform transitions between flow stages. *landform_transitions_chi_square.csv*.
    * Note that the Chi-squared expected frequency parameter is defined by the relative landform abundance at the higher flow stage for a given transition. 
    * For example, take a river where 50% of cross-sections that are *nozzles* (narrow and shallow) at a 0.7ft flow stage transition into wide bars (wide and shallow) at a 1.2ft flow stage. If *wide bar* cross-sections only represent 20% of the higher flow stage, we can say that nozzles preferentially transition into wide bars if significant at the p < 0.05 level. 


- A *.csv* table with results from a T-Test comparing the the relative width (Ws) values of cross-sections with Zs < -0.5 and Zs > 0.5 **at the next higher flow stage**.
    * The idea here is to see whether high and low elevation cross-sections have some preferential relationship with channel geometry at the next-higher flow stage.
    * Output: *preferential_nesting_ttest.csv*.

