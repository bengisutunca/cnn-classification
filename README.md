# 🖼️ Image Classification Project

## Project for KTU - YZM3032 Image Processing Class (Final Project)

### Project Overview
This project involves building a convolutional neural network (CNN) for image classification using a dataset located in the "dataset" directory. The dataset consists of multiple classes of images, each resized to 32x32 pixels for standardization.

### Steps and Components

#### 1. Data Loading and Preprocessing
- **Data Loading:** The script starts by loading images from each class directory within "dataset".
- **Preprocessing:** Images are resized to 32x32 pixels, converted to grayscale, histogram equalized, and normalized to improve model performance.

#### 2. Data Splitting
- The dataset is split into training, validation, and test sets using `train_test_split`. The splits are stratified to maintain class distribution.

#### 3. Data Augmentation
- **ImageDataGenerator:** Augments training data by applying random rotations, zooms, and shifts to increase dataset variability and improve generalization.

#### 4. Model Architecture
- **Convolutional Layers:** Sequential layers of convolution and max-pooling to extract features from input images.
- **Dropout Layers:** Applied to reduce overfitting during training.
- **Dense Layers:** Fully connected layers for classification.
- **Activation and Loss:** Uses ReLU activation, softmax output, and categorical cross-entropy loss for multiclass classification.

#### 5. Model Training
- **Compilation:** The model is compiled with the Adam optimizer and categorical cross-entropy loss.
- **Training:** Trains the model using `fit_generator` with data augmentation, validating on the validation set.

#### 6. Performance Evaluation
- **Visualization:** Utilizes `matplotlib` and `seaborn` for visualizing class distributions in training, validation, and test sets.
- **Metrics:** Tracks training and validation accuracy and loss over epochs to monitor model performance.

### Project Execution
To execute the project:
- Ensure Python environment with necessary libraries (`opencv`, `numpy`, `matplotlib`, `seaborn`, `tensorflow` or `keras`).
- Adjust paths and parameters as needed, especially regarding dataset location and augmentation settings.
- Run the script and monitor training progress through displayed metrics and plots.

### Conclusion
This project demonstrates the use of CNNs for image classification tasks, emphasizing data preprocessing, augmentation, model architecture, and training. Adjustments to hyperparameters and augmentation techniques can further optimize model performance.
