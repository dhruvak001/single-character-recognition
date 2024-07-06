# Single Character Recognition (OCR)

The Single Character Recognition code is designed for recognizing individual characters from images using convolutional neural networks (CNNs). It achieves an accuracy of 97.2% on the provided dataset. This code utilizes PyTorch for model building and training...

## Usage:

- Ensure the dataset is organized in the required folder structure, with training and testing data paths specified.
- Set the REBUILD_DATA flag to True if it's the first time running to rebuild the dataset.
- Train the model by running the training loop for a specified number of epochs.
- Evaluate the model on the testing dataset to obtain accuracy metrics.
  

## Note:

- Ensure proper organization of the dataset folders and adjust the paths accordingly.
- Experiment with hyperparameters such as batch size, learning rate, and number of epochs to optimize performance.
- Customize the model architecture or training process based on specific requirements and constraints.





## Code Overview:

Dataset Preparation:</br>
The code expects the dataset to be organized in specific folders, with each folder representing a class (e.g., letters A-Z, digits 0-9).
It reads images from the specified training and testing data paths, preprocesses them (resizing to a fixed size), and creates training and testing datasets.

Model Architecture:</br>
The neural network architecture consists of three convolutional layers followed by two fully connected (linear) layers.
Each convolutional layer is followed by a max-pooling layer and a ReLU activation function.
The output layer has 36 units corresponding to the 36 classes (26 letters + 10 digits).

Training:</br>
The model is trained using the Adam optimizer with a mean squared error (MSE) loss function.
Training is performed in batches over multiple epochs.
Training progress is displayed, and the loss is printed for each epoch.

Testing:</br>
After training, the model is evaluated on the testing dataset to measure its accuracy.
The accuracy is calculated by comparing the predicted classes with the true classes and calculating the ratio of correct predictions to the total number of samples.
