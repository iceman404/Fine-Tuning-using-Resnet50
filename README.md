# Fine-Tuning-using-Resnet50

I was able to get around 88% accuracy without the risk of overfitting. It's not the above 95% but I think it's still best fit.

## Fine Tuning of Flower Classification with ResNet50
### Introduction:
**This notebook presents a comprehensive approach to classifying flower images using a pre-trained ResNet50 model. The ResNet50 architecture, known for its deep residual learning framework, effectively handles complex classation tasks by leveraging skip (residual) connections to mitigate issues related to vanishing gradients and model depth.**

## Objective:
**The primary objective of this project is to fine-tune a pre-trained ResNet50 model on the 102 Flower Dataset. The dataset consists of images of flowers across 102 categories. The goals of this notebook include:**

**Data Preparation: Loading and preprocessing the flower images and their corresponding labels. Model Definition: Modifying the ResNet50 model for the specific classification task. Training and Validation: Training the model with a focus on optimizing accuracy and preventing overfitting. Evaluation: Assessing the model's performance on a validation set.**

## Methodology:
**Data Loading and Preprocessing: Load the dataset and split it into training, validation, and test sets. Apply image transformations to enhance model robustness, including resizing, normalization, and data augmentation.**

**Model Customization: Load the pre-trained ResNet50 model. Modify the final fully connected layer to match the number of classes in the dataset. Implement dropout to prevent overfitting.**

**Training and Optimization: Define the loss function and optimizer. Utilize a learning rate scheduler to adaptively adjust the learning rate. Implement automatic mixed precision (AMP) to optimize GPU memory usage and training speed.**

**Evaluation and Early Stopping: Monitor model performance on the validation set. Apply early stopping to prevent overfitting and save the best model.**

## Prerequisites:
**Ensure you have the following Python packages installed:**
```bash
torch
torchvision
albumentations
scipy
PIL
numpy
tqdm
```
**You can install these packages using pip if they are not already installed:**
```bash
!pip install torch torchvision albumentations scipy pillow numpy tqdm
```
## Download the dataset (adjust the link if needed)
```bash
!wget http://www.robots.ox.ac.uk/~vgg/data/flowers/102/102flowers.tgz
!wget http://www.robots.ox.ac.uk/~vgg/data/flowers/102/imagelabels.mat
!wget http://www.robots.ox.ac.uk/~vgg/data/flowers/102/setid.mat
```
## Extract the images
```bash
!tar -xzf 102flowers.tgz
```
## Trained Output:
![Preview](https://github.com/iceman404/Fine-Tuning-using-Resnet50/raw/main/asset/download.jpeg)
.
**I think, it can be further improved. But at the moment it's the best solution without the risk of overfitting.**
