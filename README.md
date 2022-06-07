# AI-Project-Virtual-Mouse
This is a Computer Engineering 6th sem project. AI Based virtual Mouse 
Savitribai Phule Pune University
A
Project Report On
“Virtual Mouse Using Python”
Submitted by
Mr. Swapnil Rajendra Take
Mr. Prashant Arun Zirpe
UNDER THE GUIDANCE BY
Prof. Ghadge R.A.
DEPARTMENT OF COMPUTER ENGINEERING
VISHWABHARATI ACADEMY’S COLLAGE OF ENGINEERING
SAROLA BADDI AHMEDNAGAR 414201
ACADEMIC YEAR 2021-22
DEPARTMENT OF COMPUTER ENGINEERING
VISHWABHARATI ACADEMY’S COLLAGE OF ENGINEERING
Sarola Baddi, Ahmednagar
CERTIFICATE
This is to certify that Prashant Arun Zirpe has successfully completed his Report on “Virtual Mouse Using Python” at Vishwabharti Academy’s College of Engineering, Ahmednagar in the partial fulfillment of the Graduate Degree course in T.E. at the Department of Computer Engineering, in the academic Year 2021-2022 Semester-VI as prescribed by the Savitribai Phule Pune University
Prof. Ghadge R.A Prof. Joshi S.G. Prof. Dhongde V.S.
Project Guide Head of Department Principal
Date:
Place: Ahmednagar
Acknowledgement
We would like to extend our sincere appreciation and indebtedness to the teacher of the Computer Department Prof. Ghadge R.A. for providing the technical, informative support, valuable guidance and constant inspiration and encouragement as a project guide which has brought this stage one project report in this form.
We would also like to express our gratitude to Prof. Dhongade V.S. for his constant source of encouragement and friendly guidance throughout the project work And at the end we would like to express our gratitude to all staff member who have directly or indirectly contributed in their own way and all my friends Computer Department for their suggestions and constructive criticism.
Mr. Prashant Arun Zirpe
Table of Contents
1. Abstract.........................................................................................................................................
2. Introduction..................................................................................................................................
3. Algorithm Used for Hand Tracking...........................................................................................
4. S/W & H/W Requirement..........................................................................................................
5. Methodology.................................................................................................................................
6. Flowchart.....................................................................................................................................
7. Screenshot....................................................................................................................................
8. Applications..................................................................................................................................
9. Future Scope................................................................................................................................
10. Conclusions..............................................................................................................................................
11. References ...............................................................................................................................................
1. Abstract
This project promotes an approach for the Human Computer Interaction (HCI) where cursor movement can be controlled using a real-time camera, it is an alternative to the current methods including manual input of buttons or changing the positions of a physical computer mouse. Instead, it utilizes a camera and computer vision technology to control various mouse events and is capable of performing every task that the physical computer mouse can.
The Virtual Mouse colour recognition program will constantly acquiring real-time images where the images will undergone a series of filtration and conversion. Whenever the process is complete, the program will apply the image processing technique to obtain the coordinates of the targeted colours position from the converted frames. After that, it will proceed to compare the existing colours within the frames with a list of colour combinations, where different combinations consists of different mouse functions. If the current colours combination found a match, the program will execute the mouse function, which will be translated into an actual mouse function to the users' machine.
2. Introduction
With the development technologies in the areas of augmented reality and devices that we use in our daily life, these devices are becoming compact in the form of Bluetooth or wireless technologies. $is paper proposes an AI virtual mouse system that makes use of the hand gestures and hand tip detection for performing mouse functions in the computer using computer vision.
Main objective of the proposed system is to perform computer mouse cursor functions and scroll function using a web camera or a built-in camera in the computer instead of using a traditional mouse device. Hand gesture and hand tip detection by using computer vision is used as a HCI with the computer. With the use of the AI virtual mouse system, we can track the fingertip of the hand gesture by using a built-in camera or web camera and perform the mouse cursor operations and scrolling
Function and also move the cursor with it. While using a wireless or a Bluetooth mouse, some devices such as the mouse, the dongle to connect to the PC, and also, a battery to power the mouse to operate are used, but in this paper, the user uses his/her built-in camera or a webcam and uses his/her hand gestures to control the computer mouse operations. In the proposed system, the web camera captures and then processes the frames that have been captured and then recognizes the various hand gestures and hand tip gestures and then performs the particular mouse function.
3. Algorithm Used for Hand Tracking
For the purpose of detection of hand gestures and hand tracking, the MediaPipe framework is used, and OpenCV library is used for computer vision. The algorithm makes use of the machine learning concepts to track and recognize the hand gestures and hand tip.
MediaPipe :
MediaPipe is a framework which is used for applying in a machine learning pipeline, and it is an opensource framework of Google. The MediaPipe frame- work is useful for cross platform development since the framework is built using the time series data. The MediaPipe framework is multimodal, where this framework can be applied to various audios and videos. The MediaPipe framework is used by the developer for building and ana- lyzing the systems through graphs, and it also been used for developing the systems for the application purpose. The steps involved in the system that uses MediaPipe are carried out in the pipeline configuration. The pipeline created can run in various platforms allowing scalability in mobile and desktops.
The MediaPipe framework is based on three fundamental parts; they are performance evaluation, framework for retrieving sensor data, and a collection of components which are called calculators [11], and they are reusable. A pipeline is a graph which consists of components called calculators, where each calculator is connected by streams in which the packets of data flow through. Devel- opers are able to replace or define custom calculators anywhere in the graph creating their own application. The calculators and streams combined create a data-flow dia- gram; the graph (Figure 1) is created with MediaPipe where each node is a calculator and the nodes are connected by streams Single-shot detector model is used for detecting and recognizing a hand or palm in real time. The single-shot detector model is used by the MediaPipe
OpenCV :
OpenCV is a computer vision library which contains image-processing algorithms for object detection. OpenCV is a library of python programming language, and real-time computer vision applications can be developed by using the computer vision library. The OpenCV library is used in image and video processing and also analysis such as face detection and object detection.
20
4
0. WRIST
1. THUMB_CMC
2. THUMB_MCP
3. THUMB_IP
4. THUMB_TIP
5. INDEX_FINGER_MCP
6. INDEX_FINGER_PIP
7. INDEX_FINGER_DIP
8. INDEX_FINGER_TIP
11. MIDDLE_FINGER_DIP
12. MIDDLE_FINGER_TIP
13. RING_FINGER_MCP
14. RING_FINGER_PIP
15. RING_FINGER_DIP
16. RING_FINGER_TIP
17. PINKY_MCP
18. PINKY_PIP
19. PINKY_DIP
9. MIDDLE_FINGER_MCP 20. PINKY_TIP
10. MIDDLE_FINGER_PIP
FIgurE 2: Co-ordinates or land marks in the hand
Figure 1: MediaPipe hand recognition graph
Camera
Camera
Temporal
Temporal backback edgeedge toto nextnext frameframe
Display
Display
AnnotationRenderer
AnnotationRenderer
DETECTIONS
DETECTIONS RECTRECT
IMAGE
IMAGE
ImageCropping
ImageCropping
DETECTIONS
DETECTIONS RECTRECT
IMAGE
IMAGE
HandDetection
HandDetection DETECTIONSDETECTIONS
RealTimeFlowLimiter
RealTimeFlowLimiter
Hand Detection only
Hand Detection only runsruns on:on: FirstFirst FrameFrame HandHand isis missingmissing
12
12
11
11
16
16
15
15
10
10
14
14
19
19
13
13
18
18
17
17
4. S/W & H/W Requirement
Software Requirement:
• Python 3.10
• Visual Studio
Hardware Requirement: • Processor – Intel Pentium • Motherboard- Intel Chipset Motherboard
• RAM- 128MB
• Web Cam
5. Methodology
The various functions and conditions used in the system are explained in the flowchart of the real-time AI virtual mouse system in Figure 3. Camera Used in the AI Virtual Mouse System. The proposed AI virtual mouse system is based on the frames that have been captured by the webcam in a laptop or PC. By using the Python computer vision library OpenCV, the video capture object is created and the web camera will start capturing video, as shown in Figure 4.
The web camera captures and passes the frames to the AI virtual system Capturing the Video and Processing. The AI virtual mouse system uses the webcam where each frame is captured till the termination of the program. $e video frames are processed from BGR to RGB color space to find the hands in the video frame by frame as shown in the following code:
def findHands(self, img, draw = True):
imgRGB = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
self.results = self.hands.process(imgRGB)
(Virtual Screen Matching) Rectangular Region for Moving through the Window. $e AI virtual mouse system makes use of the transformational algorithm, and it converts the coordinates of fingertip from the webcam screen to the computer window full screen for controlling the mouse. When the hands are detected and when we find which finger is up for performing the specific mouse function, a rectangular box is drawn with respect to the computer window in the webcam region where we move throughout the window using the mouse cursor, as shown in Figure 5.
Detecting Which Finger Is Up and Performing the Particular Mouse Function. In this stage, we are detecting which finger is up using the tip Id of the respective finger that we found using the MediaPipe and the respective co-ordinates of the fingers that are up, as shown in Figure 6, and according to that, the particular mouse function is performed.
Mouse Functions Depending on the Hand Gestures and Hand Tip Detection Using Computer Vision. For the Mouse Cursor Moving around the Computer Window. If the index finger is up with tip Id = 1 or both the index finger with tip Id = 1 and the middle finger with tip Id = 2 are up, the mouse cursor is made to move around the window of the computer using the AutoPy package of Python, as shown in Figure 7.
For the Mouse to Perform Left Button Click. If both the index finger with tip Id = 1 and the thumb finger with tip Id = 0 are up and the distance between the two fingers is lesser than 30px, the computer is made to perform the left mouse button
FIgurE 4: Capturing video using the webcam (computer vision).
FIgurE 5: Rectangular box for the area of the computer screen where we can move the cursor
FIgurE 6: Detection of which finger is up.
FIgurE 7: Mouse cursor moving around the computer window.
FIgurE 8: Gesture for the computer to perform left button click.
FIgurE 9: Gesture for the computer to perform left button click
Figure 10: Gesture for the computer to perform right button click.
lesser than 40 px, the computer is made to perform the right mouse button
click using the pynput Python package, as shown in Figure 10. For the Mouse to Perform
Scroll up Function. If both the index finger with tip Id = 1 and the middle finger with
Tip Id = 2 are up and the distance between the two fingers is greater than 40 px and if
the two fingers are moved up the page, the computer is made to perform the scroll up
mouse function using the PyAutoGUI Python package, as shown in Figure 11.
Figure 11: Gesture for the computer to perform scroll up function
For the Mouse to Perform Scroll down Function. If both the index finger with
tip Id = 1 and the middle finger with tip Id = 2 are up and the distance between the two
fingers is greater than 40px and if the two fingers are moved down the page, the
computer is made to perform the scroll down mouse function using the PyAutoGUI
Python package, as shown in Figure 12.
Figure 12: Gesture for the computer to perform scroll down function.
For No Action to be Performed on the Screen. If all the fingers are up with tip Id = 0, 1,
2, 3, and 4, the computer is made to not perform any mouse events in the screen, as
shown in Figure 13.
Figure 13: Gesture for the computer to perform no action.
6. Flowchart
Capture
Capture framesframes usingusing WECAMWECAM
Detect Hands and
Detect Hands and Hand Tips usingHand Tips using MediaPipeMediaPipe and OpenCV & draw the Hand and OpenCV & draw the Hand LandmarksLandmarks AndAnd aa boxbox aroundaround thethe handhand fromfrom webcamwebcam
Draw a rectangle box where this is
Draw a rectangle box where this is thethe regionregion ofof thethe PCPC windowwindow wherewhere wewe areare goinggoing toto useuse mousemouse
Detect
Detect whichwhich fingerfinger isis UPUP
If
If indexindex FingerFinger isis up or if both Index up or if both Index andand middlemiddle FingersFingers areare upup
Mouse Cursor moving
Mouse Cursor moving aroundaround thethe WindowWindow
If
If bothboth
Thumb
Thumb and index Fingersand index Fingers areare upup andand lengthlength betweenbetween
Perform
Perform LeftLeft ButtonButton ClickClick
If both Index
If both Index andand MiddleMiddle FingersFingers areare
Up
Up andand lengthlength betweenbetween
Perform
Perform RightRight ButtonButton ClickClick
If
If bothboth indexindex
And middle fingers Are up and
And middle fingers Are up and MovedMoved TowardsTowards upup
Perform
Perform ScrollScroll UpUp FunctionFunction
And
And middlemiddle fingersfingers AreAre
If
If bothboth indexindex
moved Towards
moved Towards downdown
Perform Scroll
Perform Scroll DownDown FunctionFunction
If all the Five
If all the Five FingersFingers AreAre upup
No Action
No Action isis PerformedPerformed
Press
Press Stop to TerminateStop to Terminate
7. Screenshot
8. Applications
The AI virtual mouse system is useful for many applications. it can be used to reduce the space for using the physical mouse, and it can be used in situations where we cannot use the physical mouse. The system eliminates the usage of devices, and it improves the human-computer interaction.
Major applications:
(i) The proposed model has a greater accuracy of 99% which is far greater than the that of other proposed models for virtual mouse, and it has many applications
(ii) Amidst the COVID-19 situation, it is not safe to use the devices by touching them because it may
result in a possible situation of spread of the virus by touching the devices, so the proposed AI virtual
mouse can be used to control the PC mouse functions without using the physical mouse
(iii) $e system can be used to control robots and automation systems without the usage of devices
(iv) 2D and 3D images can be drawn using the AI virtual system using the hand gestures
(v) AI virtual mouse can be used to play virtual realityand augmented reality-based games without the
wireless or wired mouse devices
(vi) Persons with problems in their hands can use this system to control the mouse functions in the
Computer
(vii) In the field of robotics, the proposed system like HCI can be used for controlling robots
(viii) In designing and architecture, the proposed system can be used for designing virtually for prototyping
9. Future Scope
The proposed AI virtual mouse has some limitations such as small decrease in accuracy of the right click mouse function and also the model has some difficulties in executing clicking and dragging to select the text. These are some of the limitations of the proposed AI virtual mouse system, and these limitations will be overcome in our future work. Furthermore, the proposed method can be developed to handle the keyboard functionalities along with the mouse functionalities virtually which is another future scope of Human-Computer Interaction (HCI) and AI.
10. Conclusion
The main objective of the AI virtual mouse system is to control the mouse cursor functions by using the hand gestures instead of using a physical mouse. The proposed system can be achieved by using a webcam or a built-in camera which detects the hand gestures and hand tip and processes these
Frames to perform the particular mouse functions. From the results of the model, we can come to a conclusion that the proposed AI virtual mouse system has performed very well and has a greater accuracy compared to the existing models and also the model overcomes most of the limitations of the existing systems. Since the proposed model has greater accuracy, the AI virtual mouse can be used for real-world applications, and also, it can be used to reduce the spread of COVID-19, since the proposed mouse system can be used virtually using hand gestures without using the traditional physical mouse.
The model has some limitations such as small decrease in accuracy in right click mouse function and some difficulties in clicking and dragging to select the text. Hence, we will work next to overcome these limitations by improving the finger tip detection algorithm to produce more accurate results
11. References
[1] J. Katona, “A review of human–computer interaction and virtual reality research
fields in cognitive InfoCommunications,” Applied Sciences, vol. 11, no. 6, p. 2646, 2021.
[2] D. L. Quam, “Gesture recognition with a DataGlove,” IEEE Conference on Aerospace and Electronics, vol. 2, pp. 755–760, 1990.
[3] D.-H. Liou, D. Lee, and C.-C. Hsieh, “A real time hand gesture recognition system
using motion history image,” in Proceedings of the 2010 2nd International Conference on Signal Processing Systems, July 2010.
[4] S. U. Dudhane, “Cursor control system using hand gesture recognition,” IJARCCE,
vol. 2, no. 5, 2013.
[5] K. P. Vinay, “Cursor control using hand gestures,” International Journal of Critical Accounting, vol. 0975–8887, 2016.
[6] L. Thomas, “Virtual mouse using hand gesture,” International Research Journal of Engineering and Technology (IRJET, vol. 5, no. 4, 2018.
[7] P. Nandhini, J. Jaya, and J. George, “Computer vision system for food quality evaluation—a review,” in Proceedings of the 2013 International Conference on Current Trends in Engineering
and Technology (ICCTET), pp. 85–87, Coimbatore, India, July 2013.
[8] J. Jaya and K. Tanushkodi, “Implementation of certain system for medical image diagnosis,” European Journal of Scientific Research, vol. 53, no. 4, pp. 561–567, 2011.
[9] P. Nandhini and J. Jaya, “Image segmentation for food quality evaluation using
computer vision system,” International Journal of Engineering Research and
Applications, vol. 4, no. 2,pp. 1–3, 2014.
