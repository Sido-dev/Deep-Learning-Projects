# Intel Image Classification using CNNs

## Project Description
This project implements a Convolutional Neural Network (CNN) to classify images from the Intel Image Classification dataset into six categories: buildings, forest, glacier, mountain, sea, and street. The notebook covers data download, preprocessing, model definition, training, and prediction on custom images.

## Dataset
The dataset used for this project is the **Intel Image Classification** dataset, available on Kaggle. It consists of approximately 25,000 images divided into training and testing sets, across six distinct categories.

## Installation
To run this notebook, you will need to have the following libraries installed:
- `tensorflow` (and `keras`)
- `numpy`
- `matplotlib`
- `opencv-python` (`cv2`)
- `kaggle` (for downloading the dataset)

You can install them using pip:
```bash
pip install tensorflow numpy matplotlib opencv-python kaggle
```

Additionally, you'll need to set up your Kaggle API key. Follow the instructions in the notebook's "Kaggle Setup and Data Download" section to place your `kaggle.json` file in the correct directory.

## Usage
1.  **Download the Notebook**: Clone this repository or download the `.ipynb` file.
2.  **Open in Colab/Jupyter**: Open the notebook in Google Colab or a local Jupyter environment.
3.  **Execute Cells**: Run all cells sequentially. The notebook is structured into logical sections:
    -   **Setup and Data Extraction**: Handles Kaggle API setup and unzips the dataset.
    -   **Import Libraries**: Loads necessary Python libraries.
    -   **Load and Preprocess Data**: Prepares images for training, including resizing and normalization.
    -   **CNN Model Architecture**: Defines the neural network structure.
    -   **Compile and Train Model**: Configures and trains the CNN model.
    -   **Model Prediction**: Evaluates the trained model on test data.
    -   **Map Predictions to Class Names**: Interprets model outputs into human-readable categories.
    -   **Custom Image Prediction Demo**: Shows how to use the model on new, individual images.

## Model Architecture
The CNN model comprises multiple convolutional layers with `ReLU` activation, followed by max-pooling layers for feature extraction. The extracted features are then flattened and passed through dense layers, culminating in a final `Dense` layer with `softmax` activation for 6-class classification. The model uses `sparse_categorical_crossentropy` as the loss function and `Adam` optimizer.

## Results
The model achieved a high accuracy on the test set, demonstrating its ability to correctly classify images into the six environmental categories. Predictions on custom images also show accurate classifications.

## Custom Image Prediction Example
Below is an example of predicting a custom image:

```python
# Example for a custom image (as shown in the notebook)
import cv2
import matplotlib.pyplot as plt
import numpy as np

# Load and display image
c = cv2.imread("/content/seg_pred/seg_pred/1168.jpg")
c = cv2.cvtColor(c, cv2.COLOR_BGR2RGB) # Convert BGR to RGB
plt.imshow(c)
plt.show()

# Preprocess image for prediction
test3 = cv2.resize(c, (168,168))
test3 = test3.astype("float32") / 255.0
test3 = test3.reshape(1,168,168,3)

# Make prediction
pred = model.predict(test3)
predicted_class_name = train.class_names[np.argmax(pred)]

print(f"Predicted class: {predicted_class_name}")
```

## Conclusion
This project successfully demonstrates the application of CNNs for image classification on a diverse dataset. The model shows strong performance and can be easily extended for further experimentation or deployment.