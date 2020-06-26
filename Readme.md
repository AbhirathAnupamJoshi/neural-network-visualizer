# MNIST Neural Network Visualizer

## Overview

An Artificial Neural Network written using Keras / Tensorflow for prediction of handwritten digits. The Neural Network is based on and has been trained and evaluated using the [MNIST Data Set of Handwritten Digits](http://yann.lecun.com/exdb/mnist/).

This repository contains a [Flask Python](https://flask.palletsprojects.com/en/1.1.x/) [Streamlit](https://www.streamlit.io/) Application which is intended to serve as a Back-End Server API used in conjunction with an Streamlit Application which can be found [HERE!](http://visualize-neuralnetwork.herokuapp.com/)

The Flask App provides one end-point ```/``` in which a function is called to make a prediction of the image passed in the request object and return that prediction to the client along with 2 Layers as output. The application employs Tensorflow and Numpy in order to manipulate the image converting it to grayscale, resizing and transforming to an array of pixels in prepartion for passing it to the Model for prediction.

## MNIST Data Set

The MNIST data set of handwritten digits is a subset of a larger set available from [NIST](https://www.nist.gov/). MNIST contains a training set of 60,000 samples and test set of 10,000 samples. The digits have been size-normailised and centered in a fixed-size image. This application employs the MNIST data set in order to train, evaluate and predict using a [Keras](https://keras.io/) Neural Network Model.

Example of MNIST Digits

![MNIST Example](https://camo.githubusercontent.com/b06741b45df8ffe29c7de999ab2ec4ff6b2965ba/687474703a2f2f6e657572616c6e6574776f726b73616e64646565706c6561726e696e672e636f6d2f696d616765732f6d6e6973745f3130305f6469676974732e706e67)

## Neural Networks

The repository contains a Jupyter Notebook in which an artifical neural network is used to train a model for predicting species the number chosen randomly from the MNIST Data Set.

## Prerequistes

As this is a Python based application, Python is a must and can be downloaded from the [Anaconda](https://www.anaconda.com/products/individual) open distribution which includes all of the . If you are on OSX you can simply install Python using [Homebrew](https://brew.sh/).
```bash
brew install python3
```
And install additional dependencies such as numpy and requests as needed using the pip package manager and the `requirements.txt` file.
```bash
pip install -r requirements.txt
```
Some URL for installing other dependencies:
* [Tensorflow](https://www.tensorflow.org/install)
* [Keras](https://keras.io/)
* [Flask](https://flask.palletsprojects.com/en/1.1.x/)

## Getting Started

1. Clone this repository
```bash
git clone https://github.com/AbhirathAnupamJoshi/neural-network-visualizer.git
```
2. Start the server
```bash
python ml_server.py
```
3. Start Streamlit Web App
```bash
Streamlit run app.py
```

## Buildind the Model

This repository already includes a h5 Model file - `model.h5`. However should you want to rebuild the model using the associated Jupyter Notebook file `Neural_Network.ipynb`. Building a new Model everytime the server is started is unnecessary and will slow down the application starting.
The last training result of the current model:
```
Epoch 250/250
60000/60000 - 0s - loss: 2.9358e-06 - accuracy: 1.0000 - val_loss: 0.5157 - val_accuracy: 0.9543
```