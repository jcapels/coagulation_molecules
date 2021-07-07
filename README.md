# NCI data pre-process and featurization

## Data collection (coagulation.sdf file):
https://github.com/isidroc/kekulescope/tree/master/datasets/Coagulation

## Scientific article (where the data is explained)
Cortés-Ciriano, I., Bender, A. KekuleScope: prediction of cancer cell line sensitivity and compound potency using convolutional neural networks trained on compound images. J Cheminform 11, 41 (2019). https://doi.org/10.1186/s13321-019-0364-5

## Data description
Molecules that can be used in drug discovery as inhibitors of a specific biological function. Each molecule of the dataset has a pIC50 value assigned for the protein Thrombin. half maximal inhibitory concentration (IC50) is a measure of the potency of a substance in inhibiting a specific biological or biochemical function. 
IC50 is a quantitative measure that indicates how much of a particular inhibitory substance (e.g. drug) is needed to inhibit, in vitro, a given biological process or biological component by 50%.[1] The biological component could be an enzyme, cell, cell receptor or microorganism. 
IC50 values are typically expressed as molar concentration. 
The IC50 values are converted to the pIC50 scale as follows:

![classification results](pIC50_formula.png)

## Pre-process and featurization
The "coagulation.sdf" file was processed using the [rdkit package](https://www.rdkit.org/). 
The following features were estimated for each molecule:

- "molecular weight",
- "LogP",
- "number of rings",
- "number of aliphatic carbocycles",
- "number of aliphatic heterocycles",
- "number of aromatic rings",
- "topological polar surface area",
- "NH and OH number", 
- "NO number",
- "number of hydrogen acceptors", 
- "number of hydrogen donors", 
- "number of valence electrons",
- "number of rotatable bonds", 
- "number of radical electrons"

The pre-processement and featurization process can be reproduced as in the "preprocess_featurization.ipynb" file.