# Gesture-Recognition-using-TDNN
Recognizing hand gestures by varying input delay depths, hidden layers and using Time Delay Neural Network in MATLAB
The datasets have data from 4 movements, each repeated 3 times by each of the six subjects as follows:
Four movement types (all with approximate 1Hz frequency, 10 repetitions/record, and within a vertical XZ plane parallel to, and in front of the subject’s torso):
1-CW circle
2-CW triangle
3-Linear, left to right
4-Linear, up-down
Signal sampling rate: 30Hz
Recoding device: on-wrist wearable with 3-axis accelerometer

## Pre - Fold
Using subject 2 for neural network training, we use 9 different configurations for input delay depths and hidden layer and test the TDNN network in each case. We use the best configuration for calculating the decision profile matrix for subject specific and subject independent cases. 

## Subject Specific Training
Using the best configuration from pre fold, we create 6 individual decision profile matrices for each of the 6 subjects using 3 fold cross validation. 

Best configuration: 20 input delay depths and 20 hidden layers.

## Subject Independent Training
Using the best configuration from pre fold, we use 5 subjects for training and 1 for testing and generate a decision profile matrix using 6 fold cross validation. 

## Additional
Using committee of networks of the top three performances of input delay depths and hidden layers, we compare the area under the curve for TDNN network and committee of tdnn network for subject specific model.

Delay: 20
Hidden layer: 20, 10, 30

## Observations and Conclusion
Subject specific works slightly better than subject independent model.
And if we use committee of networks, it works better than the individual models of subject specific and subject independent.


