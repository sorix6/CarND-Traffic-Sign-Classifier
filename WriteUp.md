# **Traffic Sign Recognition** 

## Writeup



**Build a Traffic Sign Recognition Project**

The goals / steps of this project are the following:
* Load the data set (see below for links to the project data set)
* Explore, summarize and visualize the data set
* Design, train and test a model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images
* Summarize the results with a written report



## Rubric Points

###Submission files
The solutions to the questions have been provided in the file Traffic_Sign_Classifier.ipynb
The HTML output of the code has been provided in the file Traffic_Sign_Classifier.html
The project writeup has been provided in the current file (WriteUp.md)
The images downloaded from the internet have been provided in the folder downloaded-images

###Dataset Summary
A basic summary of the dataset has been provided:
Number of training examples = 34799
Number of testing examples = 12630
Image data shape = (32, 32, 3)
Number of classes = 43

###Exploratory Visualization
50 random images from the training set have been displayed

###Preprocessing
In the preprocessing step, images have been 
 - Resized (only if needed - this step is only called on the images downlaoded from the internet)
 - Transformed to grayscale
 - Normalized using cv2.normalize with the type NORM_MINMAX

###Model Architecture
The model architecture is the basic LeNet Architecture
 - Parameters: mu = 0 and sigma = 0.1
 - The model consists of 5 layers with the following sizes:
     - Layer 1: Convolutional. Input = 32x32x1. Output = 28x28x6.
     - Layer 2: Convolutional. Input = 14x14x6. Output = 10x10x16.
     - Layer 3: Fully Connected. Input = 400. Output = 120
     - Layer 4: Fully Connected. Input = 120. Output = 84
     - Layer 5: Fully Connected. Input = 84. Output = 43
     
###Model Training
The training has been done by using the AdamOptimizer

Training parameters:
    - Number of epochs: 25
    - Batch size: 128
    - Learning rate: 0.001
    - Dropout percentage: 0.5
    
###Solution Approach
The solution has an accuracy of the validation set of over 93%

###Acquiring New Images
A set of 8 new images downloaded from the internet have been provided in the downloaded-images folder
All images are correctly classified (Test Accuracy = 1.000)

###Model Certainty - Softmax Probabilities
Top five softmax probabilities for the predictions on the new images have been provided in the solution file



