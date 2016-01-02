#### Simulation results for "Assessing Time-Varying Causal Effect Moderation in Mobile Health"

The simulation results for each scenario are generated by the following R scripts. R output and simulation data are respectively saved to .Rout and .RData files by the same name.

File | Description
---- | ----
[sim-omit.R](sim-omit.R) | Averaging over an underlying moderator
[sim-stable.R](sim-stable.R) | Weight stabilization
[sim-ar1.R](sim-ar1.R) | Non-independence working correlation structure

Each of these scripts call routines defined in the files below.

File | Description
---- | ----
[rsnmm.c](rsnmm.c) | Data generator
[rsnmm.R](rsnmm.R) | Data generator interface
[sim.R](sim.R) | Simulation routine
[utils.R](utils.R) | Loads require packages, read source files, defines miscellaneous utility functions
[xgeepack.R](xgeepack.R) | Extensions for the geepack R package; extract, from a geepack model object, elements (e.g. working covariance, estimating function) needed for variance calculations
[xzoo.R](xzoo.R) | Extensions for the zoo R package; apply lags, difference, rolling summaries to a sample of time series
