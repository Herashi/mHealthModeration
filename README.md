#### Numerical results for "Assessing time-varying causal effect moderation in mobile health"

##### Simulation studies

The simulation results for each scenario are generated by the following R scripts. Running a script in batch mode from your system command line with, say,
```shell
R CMD BATCH --vanilla sim-omit.R
```
will create R output and simulation data files by the same name; sim-omit.Rout and sim-omit.RData, respectively.

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
[init.R](init.R) | Loads required packages and reads source files
[xgeepack.R](xgeepack.R) | Extensions for the geepack R package; extract, from a geepack model object, elements (e.g. working covariance, estimating function) needed for variance calculations
[xzoo.R](xzoo.R) | Extensions for the zoo R package; apply lags, difference, rolling summaries to a sample of time series

##### Application to simulated data

Instead of the application presented in the paper (which considers sensitive data), we provide an example using simulated data.

File | Description
---- | ----
[example.R](example.R) | Loads geepack and zoo extensions, generates data and runs an analysis similar to the application presented in the paper
[example.Rout](example.Rout) | Provides the output obtained by running the example in batch mode
