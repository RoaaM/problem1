# Face plurring

### In this simple project I wrote code to blurrs out people's faces in any given colored image or vedio without affecting the remaining parts of the image or vedio.

In this project I use jupyter notebook in VS Code IDE.. so in the first cell I write the code for image and the second cell I write code for vedio.
you can run this code using anaconda or visual studio code . 

### **Face blurring for image:**

1- initializes a 'CascadeClassifier' object named face_cascade which is trained on the 'haarcascade_frontalface_default.xml' file.
This file contains pre-trained features for detecting frontal faces in an image.

2- read an image file named girl.jpg from the specified location and stores it in the img variable

3- This line detects the faces in the 'img' variable using the detectMultiScale() method of the 'CascadeClassifier' object. The second and third arguments, 1.1 and 6, respectively, are the scaling factor and minimum number of neighbors required for a detected object to be considered a face. The output of this method is a list of detected faces, represented as a tuple of (x,y,w,h), where (x,y) are the coordinates of the top-left corner of the face rectangle, and (w,h) are the width and height of the face rectangle.

4- for loop which iterates through each detected face in the detection list.
then applies a Gaussian blur effect to the detected face region in the img variable. The GaussianBlur() function takes three arguments: the image region to be blurred, the kernel size (15x15 in this case), and the border type (which is set to cv2.BORDER_DEFAULT).
and draws a rectangle around the detected face region on the img variable using the rectangle() function

5- last thing display the image with the detected faces now blurred and outlined with rectangles.


### **Face blurring for vedio:**

1- I create a function named 'resize' that takes an image img and a new width new_width as arguments. This function first calculates the aspect ratio of the image, then uses this ratio to calculate the new height based on the new width. Finally, the cv2.resize() function is used to resize the image to the new dimensions.

2- initializes a CascadeClassifier object named face_cascade which is trained on the haarcascade_frontalface_default.xml file. This file contains pre-trained features for detecting frontal faces in an image.

3- initializes a VideoCapture object named cap which opens the video file specified by the file path.

4- create main loop of the program that reads frames from the video file, resizes the frames using the resize() function, and detects faces in each frame using the Haar cascade classifier.

5- create another loop inside the main loop that processes each detected face by applying a Gaussian blur filter to the face region, drawing a blue rectangle around the face, and displaying the resulting frame in a window named "output". The loop also checks for the 'Esc' key to be pressed to exit the program.



