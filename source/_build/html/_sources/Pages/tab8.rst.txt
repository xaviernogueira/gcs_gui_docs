GCS nesting analysis outputs
+++++++++++++++++++++++++++++

Methodology + motivation
------------------------

* Cross-sections along each of the selected flow stage centerlines are aligned to the longest centerline path (typically the lowest flow stage) based on Euclidian distance. 
* Ws, Zs, C(Ws, Zs) values are aligned for all flow stages, faciliating comparison.  
* GCS nesting analysis attempts to capture the `nested hierarchical topographic structure <https://onlinelibrary.wiley.com/doi/10.1002/esp.4411>`_ of the study river.
* Nesting patterns associated with landforms can be provide insight into which flow stages (and their respective discharges) contribute to maintaining desirable aspects of channel topography such as :term:`riffle-pool sequences`, or heterogeneity broadly. 


Outputs 
--------

Plots output to */nesting_analysis/* **IF** ``Run GCS nesting analysis?`` is set to **Yes**

- A individual plot for Ws, Zs, and C(Ws, Zs) showing series for each key flow stage, ex: *nesting_analysis/nested_Ws_plot.png*
- A plot showing all key flow stage relative landform abundance pie charts together, ex: *nesting_analysis/landform_pies.png*
- A plot showing heatplots visualizing the 2D distribution of cross-sectional paired Ws, Zs for all key flow stages, ex: *nesting_analysis/key_heatplots.png*
- Two Sankey Diagram visualizing cross-section landform transitions as flow stage increases. One with 'normal' cross-sections, ex: *nesting_analysis/landform_transitions.png*, and one without,  ex: *gcs_plots/landform_transitions_nonorm.png*

    * Statistics and Chi-squared significance levels associated with transition abundance relative to landform abundance are output at *nesting_analysis/transition_stats.txt*
    * Chi-squared expected frequency parameter is defined by the relative landform abundance at the higher flow stage for a given transition. 
    * For example, take a river where 50% of cross-sections that are *nozzles* (narrow and shallow) at a 0.7ft flow stage transition into wide bars (wide and shallow) at a 1.2ft flow stage. If *wide bar* cross-sections only represent 20% of the higher flow stage, we can say that nozzles preferentially transition into wide bars if significant at the p < 0.05 level. 
- Violin plots visualizing whether relative topographic highs and lows (abs(Zs) > 0.5) are preferentially nested within wider or narrow (abs(Ws) > 0.5) geometry at the next higher flow, ex: *nesting_analysis/violin_plots.png

    * Statistics and Welch's T-test significance levels associated with preferred nesting structure are output at *nesting_analysis/violin_stats.txt*
  

