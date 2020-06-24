# Code for the initial trait space model and implementation.

## Methods

Our trait-space model applies an environmental filter (i.e. a white plague outbreak) to a reef community and then uses a hierarchical Bayesian model that incorporates intraspecific trait variation to predict the community assemblage after the environmental filter is applied. First, an ideal trait distribution for being resistant to the disease is created by taking the trait averages of the resistant species. Initially, only M. cavernosa values of Thalassobius mediterraneus abundance and Prophenyloxidase concentration were used to create the ideal trait distribution. This ideal, target trait distribution is essentially then environmental filter. Mclust, an R package for normal mixture modeling for model based clustering, classification, and density estimation, is then used to compute the probability of a trait given a species. Traits are drawn from the ideal traits distribution. This is the probability of a trait given the environment where the environment is the target traits. The posterior for the probability of a species given its traits and environment (target traits filter) is calculated. Finally, the posterior probability of a species given the ideal traits is determined by integrating out the traits. The model produces post-outbreak relative abundances of the species based on the resistant trait targets.

## Data Files used
Traits by replicate: traits_loggenes_env.csv
Thalassobius mediterraneus abundances by species: thalmed.csv
 Prophenyloxidase concentration by species: propheno.csv
 
 Please contact me if you need access to the files. 