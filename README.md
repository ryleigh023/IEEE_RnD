**Approach**

In this task, a neural network model was built to classify handwritten digits (0–9). The dataset used was the MNIST dataset, which contains grayscale images of handwritten digits. Each image is 28×28 pixels in size.
The main goal was to train a machine learning model that can correctly identify which digit is present in an image.
The overall approach followed these steps:
1. Load the dataset.
2. Normalize pixel values so they range between 0 and 1.
3. Split the dataset into training and testing sets.
4. Train a neural network model.
5. Evaluate the model using accuracy and other performance metrics.
6. Visualize predictions and analyze errors.
   
**Dataset**

The MNIST dataset contains:
-> 70,000 total images
-> 60,000 training images
-> 10,000 testing images

10 output classes (digits 0 to 9)
Each image is converted into a flat vector of 784 values (28 × 28).

**Data Preprocessing**

Before training the model, the pixel values (which originally range from 0 to 255) were normalized to values between 0 and 1. This helps the neural network learn more efficiently and improves stability during training.
The dataset was then divided into 80% training data and 20% testing data.

**Model Used**
-> A Multi-Layer Perceptron (MLP) classifier was used. This is a type of neural network that consists of:
-> An input layer
-> One hidden layer with 128 neurons
-> An output layer with 10 neurons (one for each digit)
The model was trained for multiple iterations using the Adam optimization algorithm.

**Model Training**

The model was trained on the training dataset. During training, the neural network adjusted its internal weights to minimize classification error.
After training was completed, the model was tested on unseen test data.

**Evaluation Metrics**

The following metrics were used to evaluate performance:
-> Accuracy score
-> Confusion matrix
-> Classification report (precision, recall, F1-score)
The confusion matrix was used to understand which digits were correctly classified and where the model made mistakes.

**Results**

The model achieved high accuracy on the test dataset, showing that the neural network successfully learned patterns in handwritten digits.
The confusion matrix showed strong performance along the diagonal, meaning most digits were classified correctly.
A few misclassifications occurred between visually similar digits (for example, 3 and 5, or 4 and 9).

**Error Analysis**

Misclassified samples were visualized to understand model limitations. Most errors occurred in cases where the handwritten digits were unclear or closely resembled other digits.
This analysis helps identify where improvements can be made, such as increasing training iterations or tuning model parameters.
