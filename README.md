# LeVAsa

## Introduction

This repository contains the code for the paper "It’s LeVAsa not LevioSA! Latent Encodings for Valence-Arousal Structure Alignment." The code has been tested on Pytorch 1.3.1 and Python 3.6.8.

## Abstract

In recent years, great strides have been made in the field of affective computing. Several models have been developed to represent and quantify emotions. Two popular ones include (i) categorical models which represent emotions as discrete labels, and (ii) dimensional models which represent emotions in a Valence-Arousal (VA) circum- plex domain. However, there is no standard for annotation mapping between the two labelling methods. We build a novel algorithm for mapping categorical and dimensional model labels using annotation transfer across affective facial image datasets. Further, we utilize the transferred annotations to learn rich and interpretable data representations using a variational autoencoder (VAE). We present “LeVAsa”, a VAE model that learns implicit structure by aligning the latent space with the VA space. We evaluate the efficacy of LeVAsa by comparing performance with the Vanilla VAE using quantitative and qualitative analysis on two benchmark affective image datasets. Our results reveal that LeVAsa achieves high latent-circumplex alignment which leads to improved downstream categorical emo- tion prediction. The work also demonstrates the trade-off between degree of alignment and quality of reconstructions.

## Methods

### Algorithm
![Algorithm](https://github.com/vishaal27/LeVAsa/blob/master/Images/Annotation_Transfer_Algorithm.png)
### Architectures
![Architecture](https://github.com/vishaal27/LeVAsa/blob/master/Images/Model_Architecture.png)
### Datasets
We make use of three main datasets:
- AFEW emotional database: annotated with discrete VA values (between -10 and 10)
- Affectnet database: annotated with continuous VA values (between -1 and 1)
- IMFDB dataset (no VA annotations, only 6 discrete emotion labels)

## Experiments

https://drive.google.com/drive/folders/1a6Z6scRZvOX6CPB-Qs0WbwrodtFAg7aI?usp=sharing



For transferring VA annotations, we use Affectnet as the anchor dataset and leverage various transfer sampling strategies which can be found in the `Code Notebooks/Annotations_Transfer.ipynb` notebook. The transferred annotations are saved as .json files, which can be found inside the `Annotations` folder.

## Training and Evaluating the models
- The `Code Notebooks/Models_Training_1.ipynb` and `Code Notebooks/Models_Training_2.ipynb` notebooks contain the model classes and training scripts including the code to save checkpoints.
- The `Code Notebooks/Analysis.ipynb` notebook contains the code for evaluating the models both qualitatively (latent space visualization with TSNEs) and quantitatively (classification/regression scores).

## Saved Weights
The saved model checkpoints can be found [here](https://drive.google.com/drive/folders/1WtyiefkL7juCL4fPAFTQQr92qWUuN6C1?usp=sharing).

Project done by:
- Vishaal Udandarao (vishaal16119@iiitd.ac.in)
- Surabhi S. Nath (surabhi16271@iiitd.ac.in)
