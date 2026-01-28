# toxin_potency_over_concentration
This readme file was generated on 2025-12-02 by Paola Rubiano-Buitrago, and corresponds to the content of the zip folder, in this project

#GENERAL INFORMATION

##Author of the R projects: 
Paola Rubiano-Buitrago; Institution: Cornell University ; Email: par259@cornell.edu

Dataset of the publication:
Title:Macroevolution of plant defense favors toxin potency over concentration
Authors: 
Paola Rubiano-Buitrago 1†
Xosé López-Goldar 2†
Amy P. Hastings 1
Ellie M. Goud 3
Marjorie G. Weber 4
Anurag A. Agrawal *1,5

##Affiliations:

1 Department of Ecology and Evolutionary Biology, Cornell University, Ithaca, NY (USA)
2 School of Biological Sciences, Illinois State University, Normal, IL (USA)
3 Department of Biology, Saint Mary's University, Halifax, Nova Scotia (Canada)
4 Department of Ecology and Evolutionary Biology, University of Michigan, Ann Arbor, MI (USA)
5 Department of Entomology, Cornell University, Ithaca, NY (USA)


##correspondence and Principal investigators: 

Anurag A. Agrawal aa337@cornell.edu ; https://orcid.org/0000-0003-0095-1220  

Date of data collection: starting 2019-09-01 til 2024-09-22
Geographic location of data collection: Ithaca, NY, United States of America
Information about funding sources that supported the collection of the data: US National Science Foundation grant (IOS-2209762) 

# SHARING/ACCESS INFORMATION

Links to other publicly accessible locations of the data: 
Title: Data of leaves extracts from 60sp of Asclepias sp.
Leaves MassIVE MSV000099124
Link: ftp://MSV000099124@massive-ftp.ucsd.edu


# DATA & FILE OVERVIEW

The dataset is divided in two folders, one with code for R studio (Feature_models), the other one for SAS analysis (SAS analysis).

#DATA-SPECIFIC INFORMATION FOR: Feature_models

the folder contains:
##R project: feature_models.Rproj
##data:  
"list_of_species_rev.csv" 
"toxicity_data_aug25.csv"
"all_species_leaves_iimn_gnps_quant_for_R.csv"
"features_sirius.csv"
"annotated_features.csv"
"richness_uv.csv"
##script: 
"packages_phylogeny.R" 
"resources_phylogeny.R"

##Markdowns: 
"feature_models.Rmd"

in markdown, run resources, data and following chunks accordingly to the chunk "run data based on the model of interest". After there are the different combinations for the random forest that include:
#RF ic50 porcine-w/predictors
#RF ic50 porcine-w/out predictors
#RF ic50 monarch-w/predictors
#RF ic50 monarch-w/out predictors
#RF ic50 ratio w/predictors
#RF ic50 ratio w/out predictors

Code for Figure 2 and S1 can be found in this markdown

# METHODOLOGICAL INFORMATION FOR: Feature_models

##Methods used to collect and process the data: 

"toxicity_data_aug25.csv" see methods in Macroevolution of plant defense favors toxin potency over concentration for the toxicity analysis based on in vitro assays of milkweed leaves against resistant and sensitive enzyme
"richness_uv.csv" chromatography peaks of each milkweed extract in UV at 218 nm. 
"features_sirius.csv" and "annotated_features.csv" . Contains the result of the classification by the chemical class of the highest-scoring features in each model with CANOPUS (Dührkop et al. 2021) using the NPClassifier taxonomy and its own probability score. We annotate each feature at superclass level, however we tentatively annotate the chemical classes for those features with a score >65%

"all_Species_leaves_iimn_gnps_quant_for_R.csv"correspond to the output of leaves data after Mzmine 4.2.0 wizard  processing, with the following modifications: The quantification file ("_quantif.csv") was refined by removing non-essential columns (D-M), renaming headers of column A (row ID), B (row mz), C (row retention time) with id, mz, and rt respectively. The number of decimals was reduced in mz (column B) to optimize filtering in R Markdown. 

## Instrument- or software-specific information needed to interpret the data: 
All analyses in this dataset can be replicated using R studio 2025.05.0 and following the markdowns of each project.

#DATA-SPECIFIC INFORMATION FOR: SAS analysis

the folder contains:
##data:
"asclepias_tree_cleaned.tre"
"vcva.csv"
##script:
"60spp_concpotency.SAS"
"asclepias_vcv.R"

This code stabilish the statistics for Figure 1

# METHODOLOGICAL INFORMATION FOR: Feature_models

##Methods used to collect and process the data:

"60spp_concpotency.csv" see methods in Macroevolution of plant defense favors toxin potency over concentration for the toxicity analysis based on in vitro assays of milkweed leaves against resistant and sensitive enzyme
## Instrument- or software-specific information needed to interpret the data:
using R studio 2025.05.0 for export the asclepias_tree_cleaned.tre as matrix and SAS script for the statistical analysis
