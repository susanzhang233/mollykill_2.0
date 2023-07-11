# Mollykill 2.0

## Abstract

This project aims to build a model that would aid novel drug design processes. Somewhat related to [this](https://github.com/susanzhang233/mollykill) mollykill 1.0, this project hopes to simplify limitations of the generator and decoder by disregarding GAN's over-complicated generative structure. In this 2.0 version, we'll be more focused on employing the accuracy and efficiency of the discriminator. Then, instead of letting the generator to come up with new molecules starting from zero. We'll be applying a larger real world molecule datasets(ie. Zinc15), to mimic the traditional virtual/actual screening process to come up with potential inhibitors.


## Model Structure
![Screen Shot 2021-09-05 at 10 47 40 PM](https://user-images.githubusercontent.com/67823308/132131090-3829f4d7-97d4-43c2-a5c7-fe4c4f95ed19.png)

## Featurizer
To represent the molecules in computer understandable format, this project uses the MolGraphConvFeaturizer from deepchem package that could be referred from [here](https://deepchem.readthedocs.io/en/latest/api_reference/featurizers.html#deepchem.feat.MolGraphConvFeaturizer).
This featurizer concatenates each molecule's multiple features into two arrays: nodes array and edges array. Within each of the two arrays, there are then numbers of one-hot encoded arrays corresponding to numbers of atoms in each molecules, i.e. each atom and each bond is represented by one array.

To ensure that the size of the molecule representations are the same(i.e. to standardize input size), this project went one step further to sum up the atom and bond arrays along each column, therefore ending up with node arrays of length 30 and edges array of 11 for each molecule.


## Dataset
The example dataset used for demonstration of this model is originally from [PubChem AID1706](https://pubchem.ncbi.nlm.nih.gov/bioassay/1706), previously handled by [JClinic AIcure](https://www.aicures.mit.edu/) team at MIT into this [binarized label form](https://github.com/yangkevin2/coronavirus_data/blob/master/data/AID1706_binarized_sars.csv).
The dataset is also hosted in the [data folder](https://github.com/susanzhang233/mollykill_2.0/blob/main/data) of this project.

The model is also tested with a dataset of screening for inhibitors of MMP9(Matrix Metalloproteinases), crucial biomarkers associated with periodontal disease. The data was originally assembled [here](https://github.com/FabianHeide/MMP9_drug_discovery/blob/main/data/MMP9_sm_activity.csv).


## Repository Explanation
- [`FancyModule.py`](https://github.com/susanzhang233/mollykill_2.0/blob/main/FancyModule.py) contains the major functions of this project
- [`example.ipynb`](https://github.com/susanzhang233/mollykill_2.0/blob/main/example.ipynb) is an example usage in the model pipeline



## Limitations(Future work)
- Currently, the model accuracy is around 86-88%. More attempts with different model structure might be tested for possible improvements.
- The efficiency of the featurization and training process might be improved.
- Future wet-lab experiments could be done for confirmation from another aspect.



## Acknowledgements

- Featurizer https://deepchem.readthedocs.io/en/latest/api_reference/featurizers.html#deepchem.feat.MolGraphConvFeaturizer
- Featurizer paper https://arxiv.org/pdf/1603.00856.pdf
