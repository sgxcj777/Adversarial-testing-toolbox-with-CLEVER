# Evaluating a Tensorflow Model's robustness to adversarial attacks using CLEVER metrics

The files in this folder contains examples of how one will evaluate robustness of a Tensorflow model using CLEVER metrics.
There are examples of evaluation under a white-box setting, as well as under black-box setting. 

## Evaluation environments

### White-box
In a white-box setting, several parameters are required and need to be accessible from the model:
- Activation functions and weights values: used to compute the gradients (via partial differentiation)
- Any defence system in place in the model
IBM ART library provides a convenient wrapper `KerasClassifier(model)` for keras/tensorflow framework that provides functions that provide the above mentioned parameters. (details in the examples).

### Black-box



## Required packages

- Tensorflow 2.0 (note that eager evaluation needs to be disabled as ART library does not support this feature yet)


