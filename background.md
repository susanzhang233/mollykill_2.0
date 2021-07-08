# tbd

### Abstract

This project aims to build a model that would aid novel drug design processes. Somewhat related to [this](https://github.com/susanzhang233/mollykill) mollykill, this project hopes to simplify limitations of the generator and decoder by disregarding the GAN structure. Here, we'll be more focused on employing the accuracy and efficiency of the discriminator. Then, instead of letting the generator to come up with new molecules starting from zero. We'll be applying a larger real world molecule datasets(ie. Zinc15), to mimic the traditional virtual/actual screening process to come up with potential inhibitors.


### Planned Deliverables
Dry-lab subpart: a model that could be applied to proteins in general terms would be created.
Wet-lab subpart: in vitro demonstration backing the validation of the model.


### Resources Required
- training set: 3cl protease?

- testing set: 

- possible target molecule synthesized

- 3clp expressed: an in vitro assay system to be created


### Tools/Skills Required
- might involve web scrapping

- wet lab designs

- tensorflow(setting weight)

- rdkit

### Risks(hinderance)
- not being able to construct the model for setting weight of each molecules: simplify it
- not being able to select out any potential new inhibitors from screened drug banks: pay especially attention on the target protein in background research phase, are there any reported inhibitor? Find other possible targets, such as DDR1, for testing.

### Tentative Timeline

- [ ] 1. Conduct pre-research on existing model & protein targets. Sum their advantages and possible points for improvements
- [ ] 2. Obtain training dataset of screening assays
- [ ] 3. Improve the discriminator model: weights, stereochemistry, etc
- [ ] 4. Obtain screening dataset
- [ ] 5. Apply the screening set to the discriminator
- [ ] 6. User-friendlirize the model(make it into importable packages)
- [ ] 7. Create a wet lab assay system 
- [ ] 8. Assert the efficiency of the model with selected molecule and the assay system

>Timeline

| week1(~7.17) | week2(7.24) | week3(7.31) | week4(8.7) |
| ---- | ---- | ---- | ---- |
| 1 & 2 & 3 | 2 & 3 | 3 & 4 | 5 & 6 & 7 |

| week5(8.14) | week6(8.21) | week7(8.28) | week8(9.4) |
| ---- | ---- | ---- | ---- |
| 7 | 7 & 8 |  |  |


