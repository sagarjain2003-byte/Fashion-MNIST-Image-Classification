# Fashion-MNIST-Image-Classification
A Deep Learning project that classifies Fashion MNIST images into 10 categories using TensorFlow and Keras.

# Fashion MNIST Image Classification using TensorFlow and Keras

A beginner-friendly Deep Learning project that classifies grayscale clothing images from the Fashion MNIST dataset using an Artificial Neural Network (ANN) built with TensorFlow and Keras.

## Project Overview

The Fashion MNIST dataset contains 28×28 grayscale images belonging to 10 different fashion categories. In this project, the dataset is loaded, normalized, visualized, split into training and validation data, and used to train a neural network for multi-class image classification.

## Dataset Classes

| Label | Class |
|---|---|
| 0 | T-shirt/top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle boot |

## Model Architecture

```text
Input Image (28 × 28)
        ↓
Flatten Layer
28 × 28 → 784 features
        ↓
Dense Layer (300 neurons, ReLU)
        ↓
Dense Layer (100 neurons, ReLU)
        ↓
Output Layer (10 neurons, Softmax)
        ↓
Predicted Fashion Class
```

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Pandas
- Pydot / Graphviz (for model visualization)

## Project Workflow

1. Load the Fashion MNIST dataset.
2. Explore image shapes and data types.
3. Normalize pixel values by dividing by 255.
4. Create training and validation datasets.
5. Visualize sample images.
6. Build an ANN using Keras Sequential API.
7. Train the model for 30 epochs.
8. Visualize training and validation performance.
9. Evaluate the model on the test dataset.
10. Predict classes for new test images.

## Dataset Split

- Training data: 55,000 images
- Validation data: 5,000 images
- Test data: 10,000 images

## Installation

Clone this repository:

```bash
git clone https://github.com/YOUR_USERNAME/fashion-mnist-image-classification.git
cd fashion-mnist-image-classification
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

## Run the Project

Open Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
Fashion_MNIST_dataset.ipynb
```

Run the notebook cells sequentially.

## Model Compilation

The model can be compiled using:

```python
model.compile(
    loss="sparse_categorical_crossentropy",
    optimizer="sgd",
    metrics=["accuracy"]
)
```

## Prediction

The trained model predicts probabilities for all 10 classes. The class with the highest probability is selected using:

```python
y_pred = np.argmax(model.predict(X_new), axis=-1)
```

## Learning Outcomes

Through this project, I learned:

- Image classification fundamentals
- Data preprocessing and normalization
- Training, validation, and test datasets
- Building neural networks using Keras
- Flatten and Dense layers
- ReLU and Softmax activation functions
- Sparse categorical cross-entropy
- Stochastic Gradient Descent (SGD)
- Model training and evaluation
- Making predictions using a trained neural network
- Visualizing training history

## Future Improvements

- Improve accuracy using different optimizers such as Adam.
- Add dropout layers.
- Experiment with different numbers of neurons.
- Add confusion matrix visualization.
- Compare ANN with CNN.
- Deploy the trained model as a web application.

## Author

**Sagar Jain**

B.Tech CSE | AI/ML Enthusiast

## License

This project is created for educational and learning purposes.

