## Dataset Source
Dataset Link:
https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing


## Task 1: Dataset Understanding

#### Number of Rows and Columns

* The dataset contains 2000 rows and 17 columns.
* Rows represent customer records and columns represent features.

#### Type of Input Features

* The dataset contains both numerical and categorical features.
* Categorical columns include:

  * region
  * plan_type
  * contract_type
  * payment_method
* Remaining columns are numerical features.

#### Target Variable Description

* The target variable is `churn`.
* This is a binary classification problem.

  * 0 represents retained customers
  * 1 represents churned customers

#### Missing Value Check

* The dataset does not contain any missing values.
* All columns have 2000 non-null entries.

#### Basic Statistical Summary

* The statistical summary shows varying ranges of values across numerical columns.
* Feature scaling is required during preprocessing.

#### Distribution of the Target Variable

* The dataset is highly imbalanced.
* Retained customers: 1969
* Churned customers: 31

## Task 2: Data Preprocessing

#### Handling Missing Values

* No missing values were present in the dataset.
* Missing value handling was not required.

#### Encoding Categorical Columns

* Categorical columns were converted into numerical format using one-hot encoding.
* Encoded columns include:

  * region
  * plan_type
  * contract_type
  * payment_method
* The customer_id column was removed because it is only an identifier.

#### Scaling or Normalizing Numerical Features

* Numerical features were scaled using StandardScaler.
* Scaling improved neural network training stability and efficiency.

#### Splitting the Dataset

* The dataset was divided into training and testing sets using an 80:20 ratio.
* Training data was used for learning.
* Testing data was used for evaluation on unseen samples.

## Task 3: Neural Network Model Building

#### Input Layer

* A Sequential feed-forward neural network architecture was used.
* After preprocessing and encoding, the dataset contained 24 input features.
* The input layer consisted of 24 input neurons.

#### Hidden Layer

* One hidden layer with 16 neurons was used.

#### Activation Function

* ReLU activation function was used in the hidden layer.
* ReLU helped the model learn non-linear patterns efficiently.

#### Output Layer

* The output layer contained one neuron.
* Sigmoid activation was used because the problem is binary classification.

#### Loss Function

* Binary crossentropy was used as the loss function.

#### Optimizer

* Adam optimizer was used for updating model weights.
* Accuracy was used as the evaluation metric.

## Task 4: Training and Evaluation

#### Training Accuracy and Loss

* The model was trained for 10 epochs with batch size 32.
* Training accuracy improved from approximately 57% to around 97%.
* Training loss decreased from approximately 0.90 to around 0.50.
* Validation accuracy remained stable around 97%–98%.

#### Testing Accuracy and Loss

* Testing accuracy achieved approximately 97.5%.
* Test loss was approximately 0.24.
* Training and testing performance remained similar, indicating stable generalization.

#### Confusion Matrix

* Correctly classified retained customers: 389
* Correctly classified churn customers: 1
* Retained customers incorrectly predicted as churn: 5
* Churn customers incorrectly classified as retained: 5

#### Interpretation of Results

* The neural network achieved high accuracy and low loss values.
* The dataset imbalance affected churn prediction performance.
* Performance for retained customers was significantly better than churn customers.

## Task 5: Hyperparameter Experimentation

#### Experiment With Different Number of Hidden Layers

##### Model With Two Hidden Layers

* Additional hidden layer added for experimentation.

##### Model With Three Hidden Layers

* Three hidden layers used for comparison.

#### Experiment With Different Number of Neurons

##### Model With 32 Neurons

* Hidden layer size increased to 32 neurons.

##### Model With 64 Neurons

* Hidden layer size increased to 64 neurons.

#### Experiment With Different Learning Rates

##### Model With Learning Rate = 0.01

* Higher learning rate used for experimentation.

##### Model With Learning Rate = 0.0001

* Lower learning rate used for experimentation.

#### Comparison Table

* Multiple models were compared using:

  * Training accuracy
  * Validation accuracy
  * Loss values
  * Confusion matrix results

#### Hyperparameter Experiment Results

* Changing hidden layers, neurons, and learning rate affected model performance slightly.
* All models continued to face difficulty predicting churn customers because of severe class imbalance.

## Task 6: Final Reflection

#### Role of Weights and Biases

* Weights and biases help the neural network learn relationships between input features and the target variable.
* During training, these values are updated continuously to reduce prediction error.

#### Importance of Activation Function

* Activation functions introduce non-linearity into the neural network.
* Without activation functions, the model behaves like a linear model.

#### Effect of Learning Rate

* Very high learning rates can cause unstable training.
* Very low learning rates make training slow.
* Proper learning rate selection is important for stable convergence.

#### Underfitting and Overfitting

* The model did not show major signs of overfitting.
* Training and testing accuracy remained close.
* Class imbalance affected the prediction of minority churn samples.


## Author

* Shinoj K R
