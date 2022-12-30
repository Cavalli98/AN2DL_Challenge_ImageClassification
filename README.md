# Politecnico di Milano - Image Classification challenge for Artificial Neural Network and Deep Learning course


This is the model used in the [Image Classification challenge](https://codalab.lisn.upsaclay.fr/competitions/8522
) as part of the "Artificial Neural Networks and Deep Learning" course at Politecnico di Milano in 2022.
The goal of the challenge was to classify 8 different plant species from photographs that were 96x96 pixels with 3 color channels. We employed a transfer learning approach, using ConvNeXtLarge as the base model.

This model let us win the challenge, reaching an accuracy of 95.48 ([Results](https://codalab.lisn.upsaclay.fr/competitions/8522#results)).

## Model details

For more details about the model check the [Report](). Briefly, we used the following techniques:
* Transfer Learning with ConvNeXtLarge model with the "Weight Initialization" technique: the whole model was trained, in two phases. First, only the classification top with an high learning rate and then the whole model with a low learning rate.
* CutMix and MixUp data augmentation techniques: one or the other technique was applied to each input image
* Standard data augmentation (flip, rotate, zoom)
* Test-Time data augmentation (self-ensemble technique) with shifts and flips
* Class weighting to fight the imbalance of the dataset

## Set up
1. Download the dataset from [here](https://drive.google.com/file/d/1uaK_kzFDFelW9z4Voceb5jiX-MdR-4Fa/view) and save the zip inside the data folder.
2. Run the model
