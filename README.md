# Face Recognition

Face Recognizer identifies the face of an individual by their name with the help of their facial features.
Face Recognizer uses deep learning algorithms to compare a live capture or digital image with the stored faceprints(also known as datasets) to verify identity.
The algorithm used for detection is haar cascade by Paul Viola and Michael Jones and for recognition is the LBPH Face Recognition algorithm.

### Haar Cascade for face detection

The technique trains a cascade function (boxes of shapes) that appears in images with faces and learns the general pattern of a face through the change in colours/shadows in the image. In the original paper, the author claims to have achieved 95% accuracy in face detection. You can find a detailed explanation in the OpenCV documentation.

References:
* https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html
* https://towardsdatascience.com/face-detection-haar-cascade-vs-mtcnn-414c97cf3388

### LBPH Algorithm for face recognition

Local Binary Pattern (LBP) is a simple yet very efficient texture operator which labels the pixels of an image by thresholding the neighbourhood of each pixel and considers the result as a binary number. Using the LBP combined with histograms we can represent the face images with a simple data vector. 

References:
* https://towardsdatascience.com/face-recognition-how-lbph-works-90ec258c3d6b

# Getting Started

## Prerequisites
1. [OpenCV 3.x](https://www.python.org/downloads/)
2. [Python 3](https://pypi.org/project/opencv-python/)
3. [Numpy](https://pypi.org/project/numpy/)

## Installing and Running
1. Download the project as a zip file and unzip it.
2. Download all the prerequisite libraries to run the program. 
```pip install opencv-python 
   pip install opencv-contrib-python
   pip install numpy```
3. Run 'createData.py'. This python file will ask for an ID(type any integer value) to enter and will help create a dataset by turning on the camera and capturing the images. You can also run the command ``` python createData.py``` in your CLI.
4. Now comes training the dataset. run ```python trainData.py``` this will also create a trainData.yml file that will help in configuration while recognising someone.
5. Finally we will run ```python recogniseData.py``` this will turn on your camera and will recognise the face.