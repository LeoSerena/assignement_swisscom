# Swisscom assignment

## Description

This repo constitutes the assignment for Swisscom in 2020. The goal is to perform gender classification on speech samples using various models.

## Content

The repository includes 2 jupyter notebooks:

- MFCC features extractions
- models implementation
- student_assignment.md

The first filters the data and generated the MFCCs features while the second implements 4 different models to perform the classification task.

The *student_assigmement.md* is the description of the task.

## Installation

Before running any of the jupyter notebooks run the following command (or use anaconda):

```
pip install librosa pandas numpy tqdm tensorflow keras sklearn matplotlib
```

## Usage

To run the models, first download the data on [openslr](http://www.openslr.org/) and select the *dev_clean* dataset of Librispeech (SLR12) and unzip it in the root of the repository.

Install the following dependencies

Run the *MFCC features extractions* jupyter and wait for the dataset to be created.

Then run the second jupyter notebook *models implementation*.

## Summary

### MFCC features extraction

The first part starts by filtering out the noise of the signal by computing their envelope and removing the irrelevant parts according to a threshold.

Then the MFCCs features are computed on each chunk of equal frame length data and put in a file with their corresponding labels such that we can later use them as dataset.

### models implementation

The logistic regression, MLP and CNN models were implemented using tensorflow while the SVM uses the sklearn library.

## Results

### Baselines

 #### Logistic Regression

The first model is a simple logistic regression, to assess how a very simple model performs. The model was tested using different learning rates, from 0 to 0.01. The best test accuracy was **0.8915**.

#### Multi Layered Perceptron

The second baseline model is a MLP. The model was tested combining its complexity using 2 different number of layers, 2 and 3, different layer depth, 16 and 32, and different learning rates, from 0 to 0.001.

##### number of layers = 2, depth = 16

The best test accuracy is of **0.9019**

##### number of layers = 2, depth = 32

The best test accuracy is of **0.8997**

##### number of layers = 3, depth = 16

The best test accuracy is of **0.9041**

##### number of layers = 3, depth = 32

The best test accuracy is of **0.9075**

So overall the best accuracy is achieved with the most complex MLP, having 3 layers and 32 neurons per layer.

### CNN and SVM

#### Convolutional Neural Network

The CNN was tested with different activation functions in the convolutional layer and with a variety of learning rates from 0 to 0.001.

##### relu 

The best achieved accuracy is **0.9149**

##### tanh

The best achieved accuracy is of **0.8993**

##### selu

The best achieved accuracy is **0.9192** 

#### Support Vector Machine

The SVM was tested with different regularization parameters and different kernels.

##### polynomial kernel (p = 3)

The best achieved accuracy is **0.9015**

##### rbf

The best achieved accuracy is **0.9067**

So overall the CNN performed better, since it captures the temporal correlations of the MFCCs better due to its architecture.