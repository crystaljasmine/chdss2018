## Modelling scripts

Code for the Gaussian process model for inductive reasoning described in:

Hayes, Banner, Forrester & Navarro (in preparation). *Sampling frames and inductive inference.* Manuscript in preparation

Code directory has scripts for running the model

In the `output` directory there are two files

- `simulations.Rdata` contains the output from simulating the GP model. It contains the `make` function used to construct each simulation, and `sim`, a list that includes each separate condition (14 in total) as an element. See below for a summary of what each of these elements contains
- `fits_lines.pdf` is the plot showing model predictions 

The elements of a `sim` list (e.g., `sim$category_n2`) contain the following elements:

- `opt`: various options governing the JAGS simulations
- `obs`: data (including model parameters) fed to JAGS
- `string`: the JAGS model as a string
- `jagsmod`: the actual JAGS model object
- `samples`: the samples generated by the JAGS run
- `out`: a simple summary used to help draw pictures 