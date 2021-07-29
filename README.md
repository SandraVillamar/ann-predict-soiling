# Artifical Neural Network (ANN) to Predict Soiling
Code to build an ANN in order to predict daily change in soiling ratio at a solar plant test facility. This work was done during my time at EDF Renewables as a Data Analytics Intern, and has been censored in order to protect confidential information.

## Objective
To find a data driven methodology for computing soiling rate at locations where we do not have measured data yet. The term *soiling* refers to the accumulation of material (such as snow, dirt, and dust) on solar panels. This material blocks or scatters light, leading to a loss in power output.

## Process
- Retrieved data for (present-day) PM10, WS, WD, RH, Temp + (previous-day) PM10, WS, RH 

- Defined output as daily change in soiling ratio (not including days after rain or a cleaning event) 

- Built a multilayer perceptron (feed-forward neural network) and utilized GridSearch CV to tune the hyperparameters 

- Model hyperparameters: 

  - Levenberg Marquardt (LM) algorithm used as optimization tool for back-propagation training 

  - Hidden layer activation function = hyperbolic tangent sigmoid transfer function 

  - Input/Output layers activation function = linear function 

  - epochs = 10, batch size = 10 

  - neurons in hidden layer = 14 

  - kernel initializer = glorot uniform 

- Tested on 2 solar plant sites and obtained results that were similar in magnitude to the true output 
