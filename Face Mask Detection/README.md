# Face Mask Detection System

This project aims to develop a face mask detection system using a Convolutional Neural Network (CNN). The system classifies images into two categories: with mask and without mask.

## Dataset

The dataset used for this project can be downloaded from [Kaggle - Face Mask Dataset](https://www.kaggle.com/datasets/omkargurav/face-mask-dataset). Make sure to download and place the dataset in the appropriate directory structure before running the code.

## Installation

To run this project, you need to have Python installed along with the following libraries:
- numpy
- matplotlib
- opencv-python
- Pillow
- scikit-learn
- tensorflow

You can install these libraries using pip:

```bash
pip install numpy matplotlib opencv-python Pillow scikit-learn tensorflow
```

## Project Structure

- `data/with_mask`: Directory containing images of people wearing masks.
- `data/without_mask`: Directory containing images of people not wearing masks.

## Steps to Run the Project

### 1. Importing the Dependencies

Ensure the necessary libraries for image processing, data manipulation, and model training are imported.

### 2. Loading and Exploring the Dataset

List the image files in the `with_mask` and `without_mask` directories to verify the data.

### 3. Creating Labels

Assign labels to the images:
- `1` for images with a mask
- `0` for images without a mask

### 4. Displaying Sample Images

Display a sample image from each category to visualize the data.

### 5. Image Preprocessing

Resize images to a standard size and convert them into numpy arrays for model training. This involves:
- Resizing images to 128x128 pixels.
- Converting images to RGB format.
- Storing the processed images in a list.

### 6. Train-Test Split

Split the data into training and testing sets using an 80-20 split.

### 7. Data Scaling

Scale the data to keep the range of values between 0 and 1 for better model performance.

### 8. Building the Convolutional Neural Network

Create a CNN model with the following layers:
- Convolutional layers with ReLU activation and max pooling.
- Flatten layer to convert 2D data to 1D.
- Dense layers with ReLU activation and dropout for regularization.
- Output layer with sigmoid activation for binary classification.

### 9. Model Compilation

Compile the model using Adam optimizer and sparse categorical crossentropy loss function.

### 10. Model Training

Train the model on the training data and validate it using a validation split from the training data. The training involves multiple epochs to optimize model weights.

### 11. Model Evaluation

Evaluate the model using the test data to determine its accuracy.

### 12. Plotting the Training History

Plot the training and validation loss and accuracy to visualize the model's performance over epochs.

### 13. Predictive System

Create a predictive system to classify a new image as with mask or without mask. This involves:
- Reading and resizing the input image.
- Scaling the image.
- Making predictions using the trained model.
- Displaying the result and the image.

## Conclusion

This project demonstrates how to build a face mask detection system using a Convolutional Neural Network. The model is trained on a dataset of images with and without masks and achieves good accuracy in classifying new images.

## References

- Dataset: [Kaggle - Face Mask Dataset](https://www.kaggle.com/datasets/omkargurav/face-mask-dataset)
- TensorFlow Documentation: [TensorFlow](https://www.tensorflow.org/)
- OpenCV Documentation: [OpenCV](https://opencv.org/)