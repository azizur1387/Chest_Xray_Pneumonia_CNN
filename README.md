Pneumonia Detection from Chest X-Ray Images Using CNN

Project Overview

This Digital Image Processing project implements a binary image classification system for classifying chest X-ray images into two classes:

- NORMAL
- PNEUMONIA

A Convolutional Neural Network (CNN) was trained to learn visual features from chest X-ray images and predict the corresponding class.

«Educational project only. This system is not a clinical diagnostic tool.»

Dataset

The project uses the publicly available Chest X-Ray Images (Pneumonia) dataset.

Dataset source:
https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

The dataset contains two classes: NORMAL and PNEUMONIA.

Dataset Distribution Used

Dataset| Number of Images
Training| 5,216
Validation| 16
Testing| 624

Project Pipeline

Chest X-Ray Images
        ↓
Image Preprocessing
        ↓
Data Augmentation
        ↓
CNN Model
        ↓
Model Training
        ↓
Testing
        ↓
Prediction
        ↓
Evaluation

Preprocessing

The following preprocessing techniques were applied:

- Images were resized for CNN input.
- Pixel values were normalized.
- Training images were augmented.
- Data augmentation included rotation, zoom, and horizontal flipping.

CNN Architecture

The project uses a Convolutional Neural Network consisting of:

1. Convolutional Layer – 32 filters
2. Max Pooling Layer
3. Convolutional Layer – 64 filters
4. Max Pooling Layer
5. Convolutional Layer – 128 filters
6. Max Pooling Layer
7. Flatten Layer
8. Dense Layer – 128 neurons
9. Dropout Layer
10. Sigmoid Output Layer

Training Configuration

- Optimizer: Adam
- Loss Function: Binary Cross-Entropy
- Evaluation Metric: Accuracy
- Epochs: 10
- Batch Size: 32

Evaluation

The trained model was evaluated using the test dataset.

Test Accuracy

78.21%

Classification Report

Class| Precision| Recall| F1-Score
NORMAL| 0.95| 0.44| 0.60
PNEUMONIA| 0.75| 0.98| 0.85

Overall accuracy: 78.21%

The project also generates:

- Accuracy curve
- Loss curve
- Confusion matrix
- Classification report
- Sample predictions

Sample Prediction

The notebook includes sample predictions from six test X-ray images. Each sample shows the actual class and the model's predicted class.

Confusion Matrix

A confusion matrix is generated to compare the actual classes with the predicted classes and to identify correct and incorrect classifications.

Model Saving

After training, the trained model was saved as:

chest_xray_cnn_model.keras

The model can be reused later without training from the beginning.

Project Files

Chest_Xray_Pneumonia_CNN/
│
├── Chest_Xray_Pneumonia_Detection_CNN.ipynb
├── chest_xray_cnn_model.keras
└── README.md

How to Run

Using Google Colab

1. Open "Chest_Xray_Pneumonia_Detection_CNN.ipynb" in Google Colab.
2. Install the required Python libraries.
3. Connect Google Drive if required.
4. Prepare/extract the chest X-ray dataset.
5. Run the notebook cells in order.
6. Train the CNN model.
7. Evaluate the model on the test dataset.
8. Generate predictions, graphs, and the confusion matrix.

Required Libraries

kaggle
tensorflow
matplotlib
seaborn
scikit-learn
numpy

Results

The CNN model achieved a test accuracy of 78.21% on 624 test images.

The model performed particularly well in identifying the PNEUMONIA class, while the NORMAL class had lower recall. This indicates that there is room for improvement in the model's ability to correctly identify all NORMAL cases.

Limitations

- The validation dataset used in this project is small.
- The model does not achieve perfect classification.
- X-ray image quality can affect prediction performance.
- The system is intended for educational purposes and should not replace professional medical diagnosis.

Future Work

Future improvements may include:

- Using a larger validation dataset.
- Using a more balanced dataset.
- Applying transfer learning with models such as ResNet or EfficientNet.
- Improving preprocessing and augmentation.
- Tuning the CNN architecture and hyperparameters.
- Developing a web or mobile interface for image prediction.

Conclusion

This project demonstrates the use of a Convolutional Neural Network for binary classification of chest X-ray images into NORMAL and PNEUMONIA classes.

The trained model achieved a 78.21% test accuracy and produced meaningful evaluation results including a classification report, confusion matrix, accuracy curve, loss curve, and sample predictions.

The project provides a practical demonstration of applying deep learning techniques to digital image classification.
