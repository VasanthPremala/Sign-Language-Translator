# Sign-Language-Translator


A Simple Sign Language Translator used to predict the live signs.


The term " dumb " is a word that used to address speech-impaired people. People affected by speech impairment can not communicate using hearing and speech, they completely rely on sign language for communicating with others. Sign language is used among everybody who is dumb, but they find a hard time communicating with people which are non-signers (normal people). Each ordinary person sees tunes in and responds to others. But there are some unfortunate people who don’t have this significant god’s gift. Such people, chiefly hard of hearing and unable to speak, rely upon correspondence by means of gestures-based communication with others. Be that as it may, correspondence with customary people is a significant disability for them since only one out of every odd run of the mill individuals grasp their gesture-based communication. So the requirement of a sign language translator is a must for speech-impaired people. There have been favorable progress in the field of gesture recognition with current advancements in deep learning. There is also been quite a significant advancement in computer vision which would enable us to easily track hand gestures. The system is to build up a framework that makes an interpretation of the communication via gestures into content that can be perused by anybody. This framework is called Sign Language Translator. It is the equivalent of real-time translation of hand gestures into equivalent English text. 

Dataset Download
Link:https://drive.google.com/drive/folders/1ty8xxjEp2nbJuFiSbTCTs4poW2xiZtzB?usp=sharing


In order to train a model you need to download dataset using above link and run load image python program to generate train_images,train_labels,test_images,test_labels,val_images,val_labels  or download train_images,train_labels,test_images,test_labels,val_images,val_labels using this link:
https://drive.google.com/drive/folders/1ty8xxjEp2nbJuFiSbTCTs4poW2xiZtzB?usp=sharing




This system takes hand gestures as input through video and translates it text which could be understood by a non-signer. There will be the use of CNN for the classification of hand gestures. This system will make communication speech impaired people less complex.


REQUIREMENTS SPECIFICATION

2.SOFTWARE REQUIREMENTS
3.Operating System: Windows 10
4.Software: PyCharm 2019.2.6 or Above


6.4.2  HARDWARE REQUIREMENTS


8.RAM: 8 GB
9.Hard Disk: 250 GB
10.Camera:Laptop Web Camera
11.CPU:Intel 5i Processor 
12.GPU:2GB or Above(Recommended)
13.Input Devices: Keyboard, Mouse
14.Output Devices:Monitor,Speaker

IMPORTING MODULES

NumPy


NumPy is the fundamental package for scientific computing with Python. As it is used to divide the given image from a construction site into n-dimensional objects such that it can be easily compared with the dataset.

Pandas


Pandas is for data manipulation and analysis. The main purpose that we are using the pandas in the neural network because it analyses the given input data and it will recognize that the given thing is an object and it will further proceed.

Matplotlib


Matplotlib is a Python 2D plotting library that is used to plot a given image in a number of small images and it will check with the dataset and it will produce publication-quality figures in a variety of hard copy formats and interactive environments across platforms. 

OpenCV



OpenCV was started at Intel in 1999 by Gary Bradsky and the first release came out in 2000. Vadim Pisarevsky joined Gary Bradsky to manage Intel’s Russian software OpenCV team. 
Pickle
It  is the process whereby a Python object hierarchy is converted into a byte stream, and “unpickling” is the inverse operation, whereby a byte stream is converted back into an object hierarchy.
 
glob


The glob module finds all the pathnames matching a specified pattern according to the rules used by the Unix shell, although results are returned in arbitrary order. No tilde expansion is done, but *, ?, and character ranges expressed with [] will be correctly matched. 

TensorFlow


TensorFlow is a Python library for fast numerical computing created and released by Google. It is a foundation library that can be used to create Deep Learning models directly or by using wrapper libraries that simplify the process built on top of TensorFlow.


SQLite


SQLite3 can be integrated with Python using sqlite3 module, which was written by Gerhard Haring. It provides an SQL interface compliant with the DB-API 2.0 specification described by PEP 249. 

pyttsx 


Pyttsx  is a text-to-speech conversion library in Python. Unlike alternative libraries, it works offline, and is compatible with both Python 2 and 3.

Thread


The Python standard library provides threading , which contains most of the primitives you'll see in this article. Thread , in this module, nicely encapsulates threads, providing a clean interface to work with them. 

ALGORITHM 


Algorithm Real time sign language conversion to text and Start.


Step-1: Set the hand histogram to adjust with the skin complexion and the lighting conditions. 


Step-2: Apply data augmentation to the dataset to expand it and therefore reduce the overfitting. 


Step-3: Split the dataset into train, test and validation data sets.


Step-4: Train the CNN model to fit the dataset. 


Step-5: Generate the model report which includes the accuracy, error and the confusion matrix. 


Step-6: Execute the prediction file – this file predicts individual gestures, cumulates them into words, displays the words as text, relays the voice output. 



Stop

![image](https://user-images.githubusercontent.com/53056749/112931276-78284300-9139-11eb-84d4-69eaa5eff8d3.png)


Steps


1.Creating a gesture


First set your hand histogram. You do not need to do it again if you have already done it. But
you do need to do it if the lighting conditions change. To do so type the command given
below and follow the instructions below.

Command: python set_hand_hist.py

❖ A window "Set hand histogram" will appear. "Set hand histogram" will have 50
squares (5x10).


❖ Put your hand in those squares. Make sure your hand covers all the squares. Press 'c’,
another window will appear "Thresh".


❖ On pressing 'c' only white patches corresponding to the parts of the image which has
your skin color should appear on the "Thresh" window.


❖ Make sure all the squares are covered by your hand.


❖ In case you are not successful then move your hand a little bit and press 'c' again.


Repeat this until you get a good histogram. After you get a good histogram press 's' to
save the histogram. All the windows close.


Already added 44 (0-43) gestures. It is on you if you want to add even more gestures or
replace my gestures. Hence this step is OPTIONAL. To create your own gestures or replace
my gestures do the following. It is done by the command given below. On starting executing
this program, you will have to enter the gesture number and gesture name/text. Then an
OpenCV window called "Capturing gestures" which will appear. In the webcam feed, you
will see a green window (inside which you will have to do your gesture) and a counter that
counts the number of pictures stored.


Command: python create_gestures.py


Press 'c' when you are ready with your gesture. Capturing gesture will begin after a few
seconds. Move your hand a little bit here and there. You can pause capturing by pressing 'c'
and resume it by pressing 'c'. Capturing resumes after a few seconds after the counter reaches
1200 the window will close automatically.
After capturing all the gestures you can flip the images using

Command: python flip_images.py


When you are done adding new gestures run the load_images.py file once. You do not need to
run this file again until and unless you add a new gesture.


2.Load The Dataset


Run the following command to load the dataset.


Command: python load_images.py


To get the classification reports about the model make sure you have test_images and
test_labels files which are generated by load_images.py. In case you do not have them run the
load_images.py file again. Then run this file.


3.Training a model


Training can be done with Keras.By using the following command,


Command: python cnn_keras.py


If you use Keras you will have the model in the root directory by the name
cnn_model_keras2.h5.You do not need to retrain your model every time. In case you added or
removed a gesture then you need to retrain it.


4.Get model reports


Run the following command to get the model reports.


Command: python get_model_reports.py


You will get the confusion matrix, f scores, precision, and recall for the predictions by the
model.


5.Testing gestures


First, we need to set our hand histogram. This can be done in the following way,
First set your hand histogram. You do not need to do it again if you have already done it. But
you do need to do it if the lighting conditions change. To do so type the command given
below and follow the instructions below.




Command: python set_hand_hist.py


❖ A window "Set hand histogram" will appear." Set hand histogram" will have 50
squares (5x10).
❖ Put your hand in those squares. Make sure your hand covers all the squares. Press 'c'.
1 other window will appear "Thresh".


❖ On pressing 'c' only white patches corresponding to the parts of the image which has
your skin color should appear on the "Thresh" window.


❖ Make sure all the squares are covered by your hand.


❖ In case you are not successful then move your hand a little bit and press 'c' again.


Repeat this until you get a good histogram. After you get a good histogram press 's' to
save the histogram. All the windows close.

For recognition start the recognize_gesture.py file.


Command: python recognize_gesture.py


You will have a small green box inside which you need to do your gestures.


Command: python fun_util.py



Here is where you will have all the fun.
First set your hand histogram. You do not need to do it again if you have already done it. But
you do need to do it if the lighting conditions change. To do so type the command given
below and follow the instructions below.



Command: python set_hand_hist.py



❖ A window "Set hand histogram" will appear." Set hand histogram" will have 50
squares (5x10).


❖ Put your hand in those squares. Press 'c', another window will appear. "res" and
"Thresh".


❖ On pressing 'c' only the parts of the image which has your skin color should appear on
the "res" window. White patches corresponding to this should appear on the "Thresh"
window.


❖ In case you are not successful then move your hand a little bit and press 'c' again.
Repeat this until you get a good histogram. After you get a good histogram press 's' to
save the histogram. All the windows close.


Command: python fun_util.py


Text Mode (Press 't' to go to text mode)


❖ In the text mode, you can create your own words using fingerspellings or use
predefined gestures.


❖ The text on the screen will be converted to speech on removing your hand from the
green box


❖ Make sure you keep the same gesture on the green box for 15 frames or else the
gesture will not be converted to text.



Calculator Mode (Press 'c' to go to calculator mode)


❖ To confirm a digit make sure you keep the same gesture for 20 frames. On successful
confirmation, the number will appear in the vertical center of the black part of the
window.


❖ To confirm a number make the "best of luck" gesture and keep it in the green box for
25 frames. You will get used to the timing :P.


❖ You can have any number of digits for both the first number and second number



❖ Currently, there are 10 operators.During operator selection, 1 means '+', 2 means '-', 3
means '*', 4 means '/', 5 means '%', 6 means '**', 7 means '>>' or right shift operator, 8
means '<<' or left shift operator, 9 means '&' or bitwise AND and 0 means '|' or
bitwise OR.


![image](https://user-images.githubusercontent.com/53056749/112931640-2d5afb00-913a-11eb-8989-682ef92e4b19.png)

![image](https://user-images.githubusercontent.com/53056749/112931650-321faf00-913a-11eb-9c70-4afb6569216d.png)

5.1CONCLUSION



The project is a simple demonstration of how CNN can be used to solve computer vision problems with an extremely high degree of accuracy. A finger spelling sign language translator is obtained which has an accuracy of 99.98%. The project can be extended to other sign languages by building the corresponding dataset and training the CNN. The main objective has been achieved, that is, the need for an interpreter has been eliminated. There are a few finer points that need to be considered when we are running the project. The thresh needs to be monitored so that we don’t get distorted gray scales in the frames. If this issue is encountered, we need to either reset the histogram or look for places with suitable lighting conditions.The thresh needs to be monitored so that we don’t get distorted gray scales in the frames.
