# fashion-mnist-tensorflow-classification-models

This project focuses on building and training multiple models using TensorFlow to classify images from the Fashion MNIST dataset.


Project Overview:

We use three different model architectures to classify fashion items into 10 categories. Each model is progressively more complex, aiming to achieve higher accuracy.

Dataset:
The Fashion MNIST dataset contains 60,000 training images and 10,000 test images, each labeled as one of the following categories:

0: T-shirt/top
1: Trouser
2: Pullover
3: Dress
4: Coat
5: Sandal
6: Shirt
7: Sneaker
8: Bag
9: Ankle boot

Each image is 28x28 pixels and is normalized before being passed into the models.

Models:-

Model 1:
This model is the simplest architecture:

Input: Flatten the 28x28 images into a 1D array of 784 elements.

Hidden Layer: A Dense layer with 128 units and ReLU activation.

Output Layer: A Dense layer with 10 units (one for each class) and Softmax activation to predict the class probabilities.

Use Case: This model serves as a baseline for classification tasks on small datasets.

Model 2
This model increases complexity to improve accuracy:

Input: Flatten the input images as in Model 1.

Hidden Layer: A Dense layer with 512 units and ReLU activation for deeper feature learning.

Output Layer: A Dense layer with 10 units and Softmax activation for class prediction.

Use Case: Designed for better performance on the Fashion MNIST dataset due to its increased depth.

Model 3 (With Callback):

Model 3 builds upon Model 2 and incorporates a callback mechanism to stop training early if certain conditions are met:

Input: Same as Model 2.

Hidden Layer: Same as Model 2 with 512 units.

Output Layer: Same as Model 2.

Callback: The training stops if accuracy exceeds 60% or if the loss falls below 0.4, preventing overfitting and unnecessary computation.

Use Case: Useful when you want to optimize training time by stopping once acceptable performance is reached.

Steps:

Data Preprocessing:

Normalize image pixel values between 0 and 1 by dividing by 255.
Model Training:

Each model is compiled using the Adam optimizer and sparse categorical crossentropy as the loss function.
The models are trained for 5 epochs.

Evaluation:
The models are evaluated on the test set after training.
Model 3 uses a callback to stop training early if performance criteria are met.

Install dependencies:
pip install -r requirements.txt

Run the script:
fashion_mnist_classification.ipynb


