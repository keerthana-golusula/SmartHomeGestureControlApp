# SmartHomeGestureControlApp
SMARTHOME GESTURE CONTROL APPLICATION PART-2

A python application to classify Smart Home Gestures using CNN model
Train and test a CNN model

Technology Requirements 
● TensorFlow
● Python 3.6.9
● OpenCV for Python
● Keras

Functionality of the application 

1.	 Generate the penultimate layer for the training videos. 
Steps to generate the penultimate layer for the training set: 
•	Extract the middle frames of all the training gesture videos.
•	For each gesture video, you will have one frame extract the hand shape feature by calling the get_Intsance() method of the HandShapeFeatureExtractor class. (HandShapeFeatureExtractor class uses CNN model that is trained for alphabet gestures)
•	For each gesture, extract the feature vector.
•	Feature vectors of all the gestures is the penultimate layer of the training set.
2.	Generate the penultimate layer for the test videos 
Follow the steps for Task 1 to get the penultimate layer of the test dataset. 
3.	 Gesture recognition of the test dataset. 
Steps: 
•	Apply cosine similarity between the vector of the gesture video and the penultimate layer of the training set. Corresponding gesture of the training set vector with minimum cosine difference is the recognition of the gesture.
•	Save the gesture number to the Results.csv
•	Recognize the gestures for all the test dataset videos and save the results to the results.csv file.


This project contains following files

cnn_model.h5 
Model used to train the data.

Main.py 
Import the handfeature extractor class
Get the penultimate layer for training data
Extract the middle frame of each gesture train video
Get the penultimate layer for test data
Extract the middle frame of each gesture test video
Gets the Gesture Number and stores in Results.csv

handshape_feature_extractor.py 
This is a Singleton class which bears the ml model in memory model is used to extract handshape 

Frameextractor.py
code to get the key frame from the video and save it as a png file.





