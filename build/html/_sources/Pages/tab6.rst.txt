Extracting Geomorphic Covariance Structure (GCS) series
++++++++++++++++++++++++++++++++++++++++++++++++++++++++
In this step we extract width (W) and mean detrended bed elevation (Z), a inverse proxy for depth, across the longitudinal extent of 
the river segment via dense, evenly spaced, cross-sectional rectangles (see examples). W and Z value are standardized to capture relative cross-sectional geomtry, yielding
Ws and Zs respecively. Cross-sections with Ws > 0 are wider than the mean, and cross-sections with Zs > 0 are shallower (higher bed elevation) than the mean. 
Multiplying Ws and Zs, due to the their standardized nature (see :ref:`Intepreting results`) calculates their covariance at a given cross section, C(Ws,Zs). Each cross-sections W, Z, Ws, Zs, C(Ws, Zs) value
are stored in a csv file that is the basis for Geomorphic Covariance Structure analysis (see :ref:`Literature`).