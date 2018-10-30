# Vision
Provide the ability to recognize images of ships and then be able to track location and prevent piracy based on known bad routes.

# Datasets
Available at https://www.kaggle.com/c/airbus-ship-detection/data
Data set downloaded to S3


# Testing
## needs updating
# Modeling Strategy

Pre-Processing step to align the data with the process outlined in the Object Detection Sage Maker notebook

Steps:
 - We will use the Sagemaker object recogniton algorithm - Single Shot multibox Detector (SSD) algorithm to detect the ship in the image.
 - This allows us to roll the two goals into 1 algorithm. 
 - We will first generate a json file containing the bounding boxes around the ships in the training data.
 - We will create a validation set from the training set and use k-fold cross validation to optimize the loss function.
 - We will use the test set images to see if the algorithm is able to what's needed. 
 
 
 More Steps: (Possibly Iteration 2)

 - Data Augmentation - generate more images by transposing, rotating images 
 - Data cleaning to remove noise from image that might hinder detection of ships

# End Goal

The end goal is two-fold.

 - Goal 1: Classify the image as SHIP/noSHIP. We will print out the probability of SHIP once an image is uploaded. 
 - Goal 2: Recognize the ship in the image if P('SHIP') >= x
