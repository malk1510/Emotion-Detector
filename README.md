# Facial-Emotion-Detector

This is my submission for the SOC Winter project by WnCC IITB. Bascally, the project involves creating a model to detect the emotion of a face in a given 48-by-48 grayscale image using ConvNets, MaxPools, BatchNorms and Padding.

The training data was actually too big to be committed to Github, so here's the link for it: https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data?select=fer2013.tar.gz

## INSTALLATIONS:
 ### Tensorflow (Keras)
 The CNN model used to detect emotions was made using Keras, the Tensorflow framework.
 ### OpenCV
 I used OpenCV to implement the Haar Cascade Classifier to detect faces, and the above model was used to detect their emotion.

## DOCUMENTATION:
The model built had many parameters to train, so, it took a lot of time on my host computer. This is why, I used Kaggle's TPU to build and train the model. It would be very difficult to run the training directly in the host system without some extra processing unit. The model has been trained to 20 epochs, and it has a training accuracy of 95%. However, it has been overfit, (oops, I forgot to add dropouts:P) so during testing the model is definitely prone to errors. I did not calculate the testing accuracy.

The model was trained with the adam optimzer, and I saved into my host computer from Kaggle, where I used OpenCV to detect the user's face and the model to detect the expression of that face (again, not the most accuracy you could get).

This repo contains two Jupyter notebooks - one for training the model and the other for using the model to detect emotions on the livestream (note that some of the file paths mentioned in the two notebooks would give an error, as I had to make the whole project on Windows).

The repo also has the .h5 file of the model and a small video of me testing the final project on my own face.
