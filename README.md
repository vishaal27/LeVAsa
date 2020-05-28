# ValenceArousalVAE

## Introduction
This repository contains the code for modelling valence and arousal as latent vector spaces of regularized and vanilla VAEs. The code has been tested on Pytorch 1.3.1 and Python 3.6.8. This project was done as part of the Affective Computing (Spring '20) course at IIIT Delhi.

Emotions are popularly represented through real valued Valence (V) and Arousal (A) values. Together, these form a continuous circumplex model vector space to represent emotions. The goal of this project is to leverage one class of generative models (VAE) and explore if their latent space can be modelled as a circumplex vector space. Generating such a latent space highly aligned with VA will enable a more descriptive and disentangled representation of the emotional images.

For this project, we make use of three main models:
- Vanilla VAE
- Discrete Regularized VAE
- Continuous Regularized VAE

A common architecture representing the three models is shown below:
![Architecture](https://github.com/vishaal27/ValenceArousalVAE/blob/master/Models/Model_Architecture.jpg)

## Datasets
We make use of three main datasets:
- AFEW emotional database: annotated with discrete VA values (between -10 and 10)
- Affectnet database: annotated with continuous VA values (between -1 and 1)
- IMFDB dataset (no VA annotations, only 6 discrete emotion labels)

For transferring VA annotations, we use Affectnet as the anchor dataset and leverage various transfer sampling strategies which can be found in the `Annotations_Transfer.ipynb` notebook.

## Training and Evaluating the models
- The `Models_Training_1.ipynb` and `Models_Training_2.ipynb` notebooks contain the model classes and training scripts including the code to save checkpoints.
- The `Analysis.ipynb` notebook contains the code for evaluating the models both qualitatively (latent space visualization with TSNEs) and quantitatively (classification/regression scores).

Project done by:
- Vishaal Udandarao (vishaal16119@iiitd.ac.in)
- Surabhi S. Nath (surabhi16271@iiitd.ac.in)
