# MTL_ChiParameter
Sample code for "Predicting polymer-solvent miscibility using machine-learned Flory-Huggins interaction parameters

## Sample data

In the folder of sample_data, we provided the full data set of experimental Chi parameter values (data_Chi.csv) extracted from the supplementary table of Orwoll and Arnold, Physical Properties of Polymers Handbook, 2nd ed., Springer: New York, USA, 2007. We also included the manual classification labels for the polymers in each data point. The SMILES of polymers and solvents in the data column 'ps_pair' were joined by '_'. Due to data sharing restriction by the PoLyInfo database, we only provide an artificial set of data for solubility (data_PI.csv), where the data is simply a copy of data_Chi.csv with solubility defined as the Chi values being smaller than 0.5. For the computational Chi parameter data (data_COSMO.csv), we only included results of polymer/sovlent pairs that appeared in data_Chi.csv, i.e., excluding those calculated data for polymer/solvent pairs extracted from PoLyInfo. The descriptors of each data set were also shared (desc_XX.csv).

## Sample code

While we only provide a subset of the training data used in this study, the user parameters and all other settings in the sample code were exactly the same as when we ran the code to produce the results in the paper. Readers can follow the code to understand the details of our model construction and training procedure. There are descriptions on the parameters inside the sample code to help user try different settings, including training with only one or two tasks instead of all three tasks together, or to use linear or quadratic temperature dependence model for predicting Chi values.

## Key packages

The sample code has been tested on the following environment using a workstation with NVIDIA A100 GPU. 

* python == 3.8.13
* jupyterlab == 3.3.4
* pandas == 1.4.2
* numpy == 1.22.3
* scikit-learn == 1.0.2
* scipy == 1.8.0
* rdkit == 2020.09.5
* xenonpy == 0.6.5
* pytorch == 1.11.0
* pickleshare == 0.7.5
* cudatoolkit == 11.3.1
