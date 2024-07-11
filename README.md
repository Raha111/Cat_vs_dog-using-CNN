# Cat vs Dog Classifier

This project contains a Jupyter Notebook that demonstrates the process of building a machine learning model to classify images of cats and dogs. The notebook includes data preprocessing, model training, evaluation, and predictions.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Visualization](#visualization)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The goal of this project is to create a classifier that can distinguish between images of cats and dogs. This is a common problem in computer vision and serves as a good introduction to image classification using deep learning.

## Dataset

The dataset used in this project is the popular [Kaggle Dogs vs. Cats dataset] (https://www.kaggle.com/datasets/salader/dogs-vs-cats) It contains 25,000 images of dogs and cats (12,500 from each class) for training, and 12,500 images for testing.

## Installation

To run this project, you need to have Python and Jupyter Notebook installed. Additionally, install the necessary packages by running:

```bash
pip install -r requirements.txt

```

## Usage

`1.` Clone this repository:
```bash
git clone https://github.com/Raha111/Cat_vs_dog-using-CNN.git
```

## Model Architecture

The model used in this project is a Convolutional Neural Network (CNN) built using Keras with a sequential API. It consists of multiple convolutional layers, followed by max-pooling layers, dropout layers for regularization, and dense layers for classification.

```bash
model = models.Sequential([
    layers.Conv2D(32, (3, 3), activation='relu', input_shape=(150, 150, 3)),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(64, (3, 3), activation='relu'),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(128, (3, 3), activation='relu'),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(128, (3, 3), activation='relu'),
    layers.MaxPooling2D((2, 2)),
    layers.Flatten(),
    layers.Dense(512, activation='relu'),
    layers.Dense(1, activation='sigmoid')
])
```

## Results
The model is trained for 10 epochs, and the performance is evaluated using accuracy and loss metrics. Below are the training and validation accuracy and loss plots:

The final test accuracy and loss are as follows:
```bash
loss, accuracy = model.evaluate(test_generator)
print("Test Loss:", loss)
print("Test Accuracy:", accuracy)
```



## Visualization
### Confusion Matrix
The confusion matrix is plotted to visualize the performance of the classifier on the test set.
### Feature Maps
The feature maps of the convolutional layers are visualized to understand what the model has learned. 
  
## Contributing
If you would like to contribute to this project, please follow these steps:

- Fork the repository.
- Create a new branch (git checkout -b feature/your-feature).
- Commit your changes (git commit -am 'Add new feature').
- Push to the branch (git push origin feature/your-feature).
- Create a new Pull Request.
  


