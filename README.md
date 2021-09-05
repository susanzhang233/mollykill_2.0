# Mollykill 2.0

## Abstract

This project aims to build a model that would aid novel drug design processes. Somewhat related to [this](https://github.com/susanzhang233/mollykill) mollykill, this project hopes to simplify limitations of the generator and decoder by disregarding the GAN structure. Here, we'll be more focused on employing the accuracy and efficiency of the discriminator. Then, instead of letting the generator to come up with new molecules starting from zero. We'll be applying a larger real world molecule datasets(ie. Zinc15), to mimic the traditional virtual/actual screening process to come up with potential inhibitors.


## Main Structure
![Screen Shot 2021-09-05 at 10 47 40 PM](https://user-images.githubusercontent.com/67823308/132131090-3829f4d7-97d4-43c2-a5c7-fe4c4f95ed19.png)

## Featurizer
- training set: 3cl protease?

- testing set: 

- possible target molecule synthesized

- 3clp expressed: an in vitro assay system to be created


## Dataset
The example dataset used for demonstration of this model is originally from [PubChem AID1706](https://pubchem.ncbi.nlm.nih.gov/bioassay/1706), previously handled by [JClinic AIcure](https://www.aicures.mit.edu/) team at MIT into this [binarized label form](https://github.com/yangkevin2/coronavirus_data/blob/master/data/AID1706_binarized_sars.csv).
The dataset is also hosted in the [data folder](https://github.com/susanzhang233/mollykill/tree/main/data) of this project.


## Repository Explaination
- [`FancyModule.py`](https://github.com/susanzhang233/mollykill_2.0/blob/main/FancyModule.py) contains the major functions of this project
- [`example.ipynb`](https://github.com/susanzhang233/mollykill_2.0/blob/main/example.ipynb) is an example usage in pipeline of the model



## Limitations(Future work)
- Currently, the generation of molecules is limited to a specific length that is shorter than most molecules in the real world. Future work involving some concepts of Conditional GAN might be employed.
- The dimension of the discriminator might be improved by adding more features of the molecules(ie. hybridization, stereochemistry, etc)
- The efficiency of the featurizer in treating edges informations might be improved(viable representation of rings, etc)



## Acknowledgements
