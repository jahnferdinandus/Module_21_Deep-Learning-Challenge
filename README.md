# Report on Neural Network Model Performance for Alphabet Soup

## Overview of the Analysis

The analysis aimed to create a predictive model for Alphabet Soup to determine the success of charitable organizations based on various features. Despite multiple attempts to optimize the neural network model and the utilization of a Random Forest classifier, the target accuracy of 75% was not achieved. This report summarizes the key steps and results of the analysis.

## Data Preprocessing

### Target and Features

- **Target Variable(s):** `IS_SUCCESSFUL`
- **Feature Variable(s):** All other variables, excluding `EIN` and `NAME`.
- **Variables Removed:** `EIN` and `NAME` were removed from the input data as they do not contribute to the predictive power of the model.

## Compiling, Training, and Evaluating the Model

### Neural Network Architecture

#### Attempt 1 (AlphabetSoupCharity - Initial Attempt)

- **Number of Neurons:**
  - First hidden layer: 10 neurons
  - Second hidden layer: 5 neurons
  - Output layer: 1 neuron (sigmoid activation)
- **Number of Layers:** 3 layers in total.
- **Activation Functions:** ReLU for hidden layers, Sigmoid for the output layer.

#### Attempt 2 (AlphabetSoupCharity_Optimization_1)

- **Number of Neurons:**
  - First hidden layer: 10 neurons
  - Second hidden layer: 5 neurons
  - Output layer: 1 neuron (sigmoid activation)
- **Number of Layers:** 3 layers in total.
- **Activation Functions:** ReLU for hidden layers, Sigmoid for the output layer.

#### Attempt 3 (AlphabetSoupCharity_Optimization_2)

- **Number of Neurons:**
  - First hidden layer: 20 neurons
  - Second hidden layer: 10 neurons
  - Additional hidden layer: 5 neurons
  - Output layer: 1 neuron (sigmoid activation)
- **Number of Layers:** 4 layers in total.
- **Activation Functions:** ReLU for hidden layers, Sigmoid for the output layer.

#### Attempt 4 (AlphabetSoupCharity_Optimization_3)

- **Number of Neurons:**
  - First hidden layer: 20 neurons
  - Second hidden layer: 10 neurons (tanh activation)
  - Additional hidden layer: 5 neurons
  - Output layer: 1 neuron (sigmoid activation)
- **Number of Layers:** 5 layers in total.
- **Activation Functions:** ReLU and tanh for hidden layers, Sigmoid for the output layer.

#### Attempt 5 (AlphabetSoupCharity_Optimization_4)

- **Number of Neurons:**
  - First hidden layer: 40 neurons
  - Second hidden layer: 20 neurons (tanh activation)
  - Additional hidden layer: 5 neurons
  - Output layer: 1 neuron (sigmoid activation)
- **Number of Layers:** 6 layers in total.
- **Activation Functions:** ReLU and tanh for hidden layers, Sigmoid for the output layer.

### Model Performance

- **Achieved Accuracy:**
  - Attempt 1: 72.44%
  - Attempt 2: 72.43%
  - Attempt 3: 72.58%
  - Attempt 4: 72.35%
  - Attempt 5: 71.29%

### Attempts to Increase Model Performance

1. **Adjusted Neurons and Layers:** Experimented with different combinations of neurons and layers to find an optimal configuration.
2. **Changed Activation Functions:** Explored different activation functions to enhance the model's learning capability.
3. **Feature Engineering:** Considered additional feature engineering techniques to extract more meaningful information.

## Summary

In summary, all attempts to optimize the neural network model fell short of the target accuracy. Despite adjusting the number of neurons, layers, and activation functions, the model's accuracy ranged from 71.29% to 72.58%. Additionally, a Random Forest model was trained, achieving an accuracy of 
70.74%, also below the target.

### Alternative Model Recommendation

Considering that both the neural network and Random Forest models did not meet the target accuracy, it is recommended to explore more advanced algorithms or ensemble methods. Gradient Boosting algorithms, such as XGBoost or LightGBM, are known for their high performance in classification tasks and could be investigated as alternatives. Further fine-tuning of hyperparameters and additional feature engineering may be necessary to achieve the desired accuracy. Exploring different algorithms may lead to a more accurate and interpretable solution to the classification problem.
