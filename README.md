This repository contains the code for the individual-based population projection model from Field CR, Bayard T, Gjerdrum C, Hill J, Meiman S, Elphick CS. 2017. High-resolution tide projections reveal extinction threshold in response to sea-level rise. Global Change Biology 23:2058–2070, http://dx.doi.org/10.1111/gcb.13519. 

The goal of the analysis was to develop a computational model that can produce robust projections to quantify the potential for thresholds and non-linearities in population responses to sea-level rise. This modeling framework made it possible to project saltmarsh sparrow populations by explicitly modeling the most important demographic and environmental processes that govern population dynamics. The general model structure is a specification that follows each female in the population over the study period, including life span and the factors that determine the number of young produced (e.g. nest-building, provisioning, flooding, re-nesting, season start and end dates). At the end of each year, any females that are produced and survive to the end of the year (according to first-year survival rates) are added to the simulation.   


Data files needed to run the script; available at https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1111%2Fgcb.13519&file=gcb13519-sup-0001-SupInfo.docx:

high_dates_NL.csv
For each tide prediction in "high_tides_NL.csv", the days since May 1 of the given year. 

high_tides_NL.csv
Rows are the predicted height (ft) of astronomical tide for every high tide, in sequential order, between between May 1 and August 31 of a given year. Columns are years; first column is 2012.

IBM_parameters.csv
Parameters from the list in Table 2 of the paper that do not have separate .csv files

nest_failure_MCMC.csv
Rows are posterior draws from the parameters (columns) that describe nest success probabilities. The columns are, in order, the intercept, effect of tide height, and the standard deviation of the nest-level random effect. 

renest_prob_MCMC.csv
Rows are posterior draws from the parameters (columns) that describe quitting probability (from Ruskin et al. 2015). The columns are, in order, the intercept, effect of latitude (which is constant at the latitude of Long Island Sound in the model), and the effect of date. 

SLR_Rahmstorf.csv
Projections of global sea level from Vermeer and Rhamstorf (2009). We use A1F1 and B1 in the model.

storm_surge_posteriors.csv
Rows are posterior draws from the parameters (columns) that describe the baseline and temporal trends in non-tidal fluctuations. The columns, are in order, the intercept, the yearly trend, the mean of year-specific parameters for within-season trends, the deviance of the model, the strength of temporal autocorrelation, the standard deviation of the residual variation, the standard deviation of variation in parameters for within-season trends, and the standard deviation of yearly variation.

surv_avgsite_MCMC.csv
Rows are posterior draws from the parameters (columns) that describe adult annual survival (from Field et al. 2016). The columns are, in order, the mean survival rate and the standard deviation desribing spatial variation in the parameter.
