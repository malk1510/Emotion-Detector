# Facial-Emotion-Detector

This is my submission for the SOC Winter project by WnCC IITB. Bascally, the project involves creating a model to detect the emotion of a face in a given 48-by-48 grayscale image using ConvNets, MaxPools, BatchNorms and Padding.
This model is a deep CNN with 3-4 such blocks, because of which the model has many, many parameters to train.

So, I used Kaggle's TPU here. It would be very difficult to run the training directly in the host system without some extra processing unit. The model has been trained to 20 epochs, and it has a great training accuracy of 92%. However, it has been overfit, (oops, I forgot to add dropouts:P) so during testing the model is likely to show errors when the facial expression isn't too easily seen, but mostly it's going to be neutral.

Either way, the model was trained with the adam optimzer, and I saved into my host computer from Kaggle, where I used OpenCV to detect the user's face and the model to detect the expression of that face (again, not the most accuracy you could get).

The facial detection has been done using Haar Classifier. Note that if you wish to use the code on your own, you'll have to change the address of the given Frontalface Haar Classifier .xml file; or you will get an error.

Once this is executed, the camera on one's devices checks for faces, which when found, resizes the portion of the image, grayscales it, and checks the emotion using the model shown above. 

I haven't found the test accuracy for this, however, I have tested this for my own face, and the goofy expressions it was able to make. But, those are just screenshots. This model can check the emotion of a face during a livestream, virtually instantaneously; with the help of OpenCV.

I'd finally like to graciously thank WnCC for the help they provided with this project and Pierre-Luc Carrier and Aaron Courville who prepared the dataset I used for this project.
