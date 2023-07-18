# Real-time-face-recognition
A facial recognition system is a technology capable of matching a human face from a digital image or a video frame against a database of faces. Face recognition is a way of recognize a human face through technology and is one of the most widely used technology for human identification.
Haar Cascade classifiers are an effective way for object detection. This method was proposed 
by Paul Viola and Michael Jones in their paper Rapid Object Detection using a Boosted
Cascade of Simple Features . Haar Cascade is a machine learning-based approach where a lot 
of positive and negative images are used to train the classifier. Initially, the algorithm needs a 
lot of positive images (images of faces) and negative images (images without faces) to train the 
classifier. Then we need to extract features from it. 
Here first we need to have to generate the dataset. First collect images. For 
this purpose, Open-CV package can be used. And haarcascade_frontalface_default xml file
is used to get the coordinate of my face so that I can crop it and use it to make dataset and for 
future prediction. And  convert  images from RGB (Red, Green, Blue) to grayscale. 
RGB image has 3 channel whereas grayscale image has only 1 channel. It reduces lot of 
complexity if we convert so. Next using face classifier and using detectMultiScale method, we 
can get the coordinates. We have to pass scale factor and minimum neighbors. Scale factor 
refers to the factor of how much to change from the original image. Minimum neighbors 
indicates how many faces to detect. Higher value results in less detection but with higher 
quality. We have to play with this value. Depending on our output, we can make changes to this 
values. Then all we have to do is, just collect the image and stop the execution when it reaches 
200 images or when we press enter button from keyboard. Next step is to train the classifier. 
Our system doesn't understand images, right? It needs to be converted into Numpy array format 
so that it can make certain decision based on this data. This part creates classifier.xml file, 
which is the file that includes certain information (data) of our face. Then add bounding box and name. This will detect the face.

