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
### Code
Image Classifier Project .ipynb consists of the code required to load, clean, explore and visualize the data and answer the questions.
### Data
census.csv
