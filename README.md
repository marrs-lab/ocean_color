# ocean_color
Tools and algorithms for drone and satellite based ocean color science

Currently in the process of implementing a few of the NASA Ocean Color team's chlorophyll retrieval algorithms from https://oceancolor.gsfc.nasa.gov/atbd/chlor_a/. The goal is to make these algorithms more easily understandable and to allow fine-tuning for sensors that differ from the primary NASA ocean observing satellites, particularly for drone-based multispectral sensors. This is all done right now using the NASA bio-Optical Marine Algorithm Dataset (NOMAD) available at https://seabass.gsfc.nasa.gov/wiki/NOMAD.

Currently implemented algorithms:
* Hu et al 2012 color index (https://doi.org/10.1029/2011JC007395) - [code](https://github.com/marrs-lab/ocean_color/blob/main/ocean_color_index_recreating.ipynb)
  * complete and exactly replicates the nonlinear regression coefficients, r-squared, and RMS from the paper.
  * this is the algorithm NASA uses for oligotrophic (low-productivity) waters in the global ocean
* OCx algorithm (originally via https://doi.org/10.1029/98JC02160 but more recently updated on https://oceancolor.gsfc.nasa.gov/atbd/chlor_a/) - [code](https://github.com/marrs-lab/ocean_color/blob/main/oc4_algo_recreating.ipynb)
  * nearly exact but the exact filtering procedure and curve matching approach isn't outlined
  * will be updating to match https://doi.org/10.1016/j.rse.2019.04.021 at some point

Application examples
* applying the OCx algorithm on Landsat 8's Provisional Aquatic Reflectance product - [code](https://github.com/marrs-lab/ocean_color/blob/main/landsat8_chla_processing.ipynb)

![VIIRS Ocean Color img](https://github.com/marrs-lab/ocean_color/blob/main/V2021005.SWAtlantic.jpg?raw=true)

January 5, 2021 image from VIIRS (credit NASA Ocean Color)
