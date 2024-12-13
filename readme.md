# Atlantic World Slave Voyages

This repo provides R code that makes it easier for scholars to statistically analyze the Trans-Atlantic and Intra-American slave voyages databases available on [SlaveVoyages.org](https://www.slavevoyages.org).

## Objective

To facilitate statistical modeling of the [SlaveVoyages.org](https://www.slavevoyages.org) data by reorganizing in a format consistant with biomedical retrospective datasets.

## Why update the datasets?

The SlaveVoyages.org interface is excellent for teaching and for calculating basic data summaries, but it cannot be easily used to compare the datasets with statistical software, borrow strength between the datasets, or to model relationships among variables. Using the update in this repo, it is possible to model uncertainty, to do multiple imputation for missing data, to do statistical modeling, as well as machine learning and AI. 


## What we have done

The [SlaveVoyages.org](https://www.slavevoyages.org) website allows users to download the Trans-Atlantic and Intra-American databases separately, for analyses.

The R code in this repo:

1. Combines the datasets into one, with a grouping variable called _intra_or_trans_ to distinguish the two original datasets.
2. Makes the variable names user friendly (e.g., REGDIS1 has been renamed _first_region_of_disembarkation_.)
3. Converts dates from character format to date format for easier date arithmetic
4. Replaces numeric codes with real names. For example, in the original datasets, the variable representing the slave ship's rig is called RIG, and it has numbers for values instead of the actual rig names. The new Atlantic-World dataset has the actual rig names. For example, in the original datasets the number 35 represents "Snauw." The Atlantic-World dataset replaces the 35 with the word Snauw. Likewise, in the original datasets, the variable representing first intended port of embarkation is called EMBREG, and its values are in the form of numbers, such as 60500, which means “Bight of Benin.” The Atlantic-World dataset renames EMBREG _first_embarkation_region_, and uses “Bight of Benin” instead of 60500.

7. Reconciles the codebooks with the data. The most data available for download is consistent with the 2022 Codebook, rather than the 2023 Codebook. 
8. Removes diatcritical marks, which can confound some statistical packages.
9. Follows R convention by using NA for missing values.

## Output

The R script makes an R dataframe called AtlanticWorld, which is the combined, modified [SlaveVoyages.org](https://www.slavevoyages.org) datasets, and it also exports that new dataset to a .csv file to use in other statistical software.

## Quick start

1. copy this the _code_and_files_ folder to your computer.
2. Download the current Trans-Atlantic and Intra-American datasets in CSV format. Put them in the folder with the R script. There should now be three files in _code_and_files_ (the two datasets and an R script) plus a folder called _numeric_lookup_files_.
3. In R, run the R script called **AtlanticWorldSlaveVoyages.R** (useage: AtlanticWorldSlaveVoyages(intra.csv,trans.csv), but replace intra.csv and trans.csv with the names of your downloaded files)

## Short biblography
