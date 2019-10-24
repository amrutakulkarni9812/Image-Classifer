![Alt text](https://raw.githubusercontent.com/rtspeaks360/flower-taxonomy/master/assets/Flowers.png?raw=true "Image Classifier")
# Image-Classifer
In this project, I built an image classifier to recognize different species of flowers. I loaded and preprocessed the image dataset, applied transformations on training dataset images to help the network generalize for better performance. define a new, untrained feed-forward network as a classifier, using ReLU activations and dropout, trained the classifier layers using backpropagation using the pre-trained network to get the features and tracked the loss and accuracy on the validation set to determine the best hyperparameters. 
## Installation
For running this project, we need PyTorch and Torchvision libraries along with the usual ones instaklled with Python 3 version of Anaconda Distribution.
## Introducing the datasets
The dataset for this project is an image dataset of [102 Category Flower Dataset](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html). Each class consists of between 40 and 258 images. The images have large scale, pose and light variations. In addition, there are categories that have large variations within the category and several very similar categories.
## File Description
### Readme
This file provides high level overview of the work done in project.
### Data
flowers folder contains training, test and validation datasets.
cat_to_name.json file contains the mapping from category label to category name
### Code
image_classifier_project.ipynb notebook consists of the code required to load, preprocess, split the data, train and test the image classification neural network and save the checkpoint. 
### Supplementary
workspace_utils.py contains the code to avoid having your workspace disconnect during the long-running tasks in this notebook. 
predict.py and train.py are the files to convert the image classifier project into a command line application.
### License
This file has copyright details.
### HTML Report
image_classifier_project.html provides python notebook in html format.
## Project Motivation
The motivation is to develop something in a phone app that tells you the name of the flower your camera is looking at and then export it for use in a command line application.
## Data Preparation
I split the data into training, validation and test sets.
I applied transformations such as random scaling, cropping, and flipping on training data to help the network generalize leading to better performance. I made sure the input data is resized to 224x224 pixels as required by the pre-trained networks.
The validation and testing sets are used to measure the model's performance on data it hasn't seen yet and they don't need any scaling or rotation transformations, but only need resizing and cropping of the images to appropriate size.
The pre-trained network used here was trained on the ImageNet dataset where each color channel was normalized separately. Hence, for all three sets I needed to normalize the means and standard deviations of the images to what the network expects.  These values shifted each color channel to be centered at 0 and range from -1 to 1.
## Building, Training and Testing the Classifier and Inference
I loaded a [pre-trained network](https://pytorch.org/docs/master/torchvision/models.html). (As a starting point, the VGG networks since they are straightforward to use)
I defined a new, untrained feed-forward network as a classifier, using ReLU activations and dropout
I trained the classifier layers using backpropagation using the pre-trained network to get the features
I tracked the loss and accuracy on the validation set to determine the best hyperparameters
