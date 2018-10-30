# Vision
Provide the ability to recognize images of ships and then be able to track location and prevent piracy based on known bad routes.

# Datasets
Available at https://www.kaggle.com/c/airbus-ship-detection/data
Data set downloaded to S3


# Testing
## needs updating
# Modeling Strategy

 - We will use the Sagemaker object recogniton algorithm - Single Shot multibox Detector (SSD) algorithm to detect the ship in the image.
 - This allows us to roll the two goals into 1 algorithm. 
 - We will create a validation set from the training set and use this to optimize the loss function.
 - We will use the test set images to see if the algorithm is able to what's needed. 
 
 More Steps:
 

  


# End Goal

The end goal is two-fold.

Goal 1: Classify the image as SHIP/noSHIP. Print out probability of SHIP once an image is uploaded. 


Goal 2: Recognize the ship in the image if P('SHIP') >= x
