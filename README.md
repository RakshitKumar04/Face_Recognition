# Face Recognition

Face Recognizer identifies the face of an individual by their name with the help of their facial features.
Face Recognizer uses deep learning algorithms to compare a live capture or digital image with the stored faceprints(also known as datasets) to verify identity.
The algorithm used for detection is haar cascade by Paul Viola and Michael Jones and for recognition is LBPH Face Recognition algorithm.

### Haar Cascade for face detection

Basically, the technique trains a cascade function (boxes of shapes) that appears in images with faces, and learns the general pattern of a face through the change in colors/shadows in the image. In the original paper, the author claims to have achieved 95% accuracy in face detection. You can find detailed explanation in OpenCV documentation.

References:
* https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html
* https://towardsdatascience.com/face-detection-haar-cascade-vs-mtcnn-414c97cf3388

### LBPH Algorithm for face recognition

Local Binary Pattern (LBP) is a simple yet very efficient texture operator which labels the pixels of an image by thresholding the neighborhood of each pixel and considers the result as a binary number. Using the LBP combined with histograms we can represent the face images with a simple data vector. 

References:
* https://towardsdatascience.com/face-recognition-how-lbph-works-90ec258c3d6b

# Getting Started

## Prerequisites
1. [OpenCV 3.x](https://www.python.org/downloads/)
2. [Python 3](https://pypi.org/project/opencv-python/)
3. [Numpy](https://pypi.org/project/numpy/)



## Installing
1. Download the project as zip file and unzip.
2. Run 'train_face.py'. This python file will create dataset for you. You can do that with command file.
```python train_face.py```
3. Create ID (for example, you can give you name) and press capture. Then follow the steps in program.
4. After you saw "Done!" in label you can close the frame
5. Run 'detect_main.py' and enjoy it!
```python detect_main.py```
