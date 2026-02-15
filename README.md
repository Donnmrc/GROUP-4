Weather Classification
This notebook trains and tests a neural network using PyTorch to classify images of weather conditions into 4 classes: Cloudy, Rain, Shine, Sunrise.

VGG16 (Simonyan et al., 2014) convolutional features are used for transfer learning, and a feed-forward network is trained to label weather images with over 98% accuracy.

Weather images available at: https://data.mendeley.com/datasets/4drtyfjtfy/1



Data preparation
The Mendeley dataset must be split into 4 folders, one for each class, with each named after the class of images it contains. I.e. all 'cloudy' images must be in WeatherImages/cloudy/.



Dataset
The Mendeley dataset contains 1125 images of classes: Cloudy, Rain, Shine and Sunrise. These make up the dataset in the proportions shown below. Augmentation is used to increase the size of the training dataset.



Training
VGG16 is used for transfer learning, and a simple fully connected network is trained as a classifier on its convolutional features. The complete architecture of the network is shown below:



Results
The network has a test accuracy of 98.23% (222/226 test predictions correct). Further analysis of results demonstrates the model's strong recall and precision scores.



Example labels and predictions:



The network has low confidence scores for the two incorrect predictions shown. This further emphasises the model's ability to predict labels accurately.

References: Karen Simonyan and Andrew Zisserman. Very Deep Convolutional Networks for Large-Scale Image Recognition. 9 2014. https://arxiv.org/abs/1409.1556
