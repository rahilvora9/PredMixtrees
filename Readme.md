## Table of contents
* [General info](#general-info)
* [Models](#models)
* [Installation and Usage](#Installation)
* [Tutorial](#Tutorial)

## General info
This project implements Baum-Welch algorithm to predict trees/class from output file of Mixtures models such as MAST, GHOST or Q-matrix model.\
The input file for B-W algorithm is .sitelh/.siteprob along with .alninfo output files from iqtree.\
Project is created using R, depends on R packages "aphid", "tidyverse", "reshape2" and "testit".\
The output is vector indicating the tree/class for a given site.\
Supports initial scatter plots and prediction plots.

## Models
Model 1 - The tree with highest probability at a given site is considered, and converted into a sequence for training of B-W algorithm.\
Model 2 - The tree with highest probability at a given site and constant sites are considered, and converted into a sequence for training of B-W algorithm.\
Model 3 - The tree with highest probability at a given site, constant sites and non-informative sites are considered, and converted into a sequence for training of B-W algorithm.\
Model 4 - The tree with highest probability at a given site, constant sites, non-informative sites and same parsimony sites are considered, and converted into a sequence for training of B-W algorithm.\
Mix Model - Starts from model 1 and moves to next model if the current B-W model doesn't converge in 100 iterations.

## Installation and Usage
```
devtools::install_github("rahilvora9/PredMixtrees")
library("PredMixtrees")
help(package="PredMixtrees")
```
