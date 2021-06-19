<h1 align="center">Drawing Printer Using Open CV</h3>
 
  <p align="center">
   <img width="300" src="https://github.com/tyrone890123/Drawing-Printer/blob/main/Assets/Screenshot%202021-06-19%20163327.png?raw=true"> &nbsp;&nbsp;&nbsp;&nbsp;
 <img width="110" src="https://qph.fs.quoracdn.net/main-qimg-bd2dad722786a6a8a7b42350f0428def"> 
  </p>
</p>

 - This project makes use of the OpenCV library as well as Pynput to automate the drawing of images for personal use in applications such as Paint, skribbl, etc.


 
<details open="open">
  <h2>Table of Contents</h2>
  <ol>
    <li>
      <a href="#intro">Introduction</a>
      <ul>
        <li><a href="#reqs">Requirements and Dependencies</a></li>
      </ul>
    </li>
    <li>
      <a href="#setup">Setup</a>
    </li>
    <li><a href="#revisions">Revisions</a></li>
  </ol>
</details>

<h2 id="intro">Introduction</h2>

This python program is a made for drawing images using canny edge detection and pynput to easily draw complex images, this program is intended to be used when playing with friends on multiplayer drawing games.

<h2 id="reqs">Libraries Used</h2>

 - OpenCV
 - Pynput
 - Time
 - Keyboard

`OpenCV` is used to detect the edges of an image as well as to determine the points that will be used to draw the image. Upon initial implementation, two methods were tested as to how the points of the image would be obtained, the first through the use of contours and the second through edge detection.

When it came to simple images, the difference between the two methods (Contour on the middle and Canny edge detection on the far right) were seemingly negligible as seen below:
<p align="center">
   <img width="200" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20183937.png"> 
&nbsp;&nbsp;&nbsp;&nbsp;
 <img width="200" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20183927.png"> 
 &nbsp;&nbsp;&nbsp;&nbsp;
 <img width="200" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20183855.png"> 
  </p>
When these images were drawn in paint the output were as follows:
<p align="center">
   <img width="400" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20183326.png"> 
  </p>
When it came to complex images however, the difference became apparent in that the canny edge detection method was able to capture more details from the image; thus, this method was chosen (Contour on the middle and Canny edge detection on the far right) :
  <p align="center">
   <img width="150" src="https://qph.fs.quoracdn.net/main-qimg-bd2dad722786a6a8a7b42350f0428def"> 
   &nbsp;&nbsp;&nbsp;&nbsp;
   <img width="150" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20182118.png"> 
      &nbsp;&nbsp;&nbsp;&nbsp;
   <img width="150" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20181849.png"> 
  </p>
</p>
This yielded the following output when drawn in paint:

<p align="center">
   <img width="400" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20182955.png"> 
  </p>

`Pynput` was used in order to control the mouse of the user for drawing as well as for monitoring the starting position and ending position of the drawing canvas. 
`Time` is an optional aspect of the program in order to slow down the drawing process of the image as well as to lessen any errors that may come due to the speed of the drawing. 
`Keyboard` is a library used to listen for the escape button in the keyboard in order to exit the drawing process in the event that an issue arises.


<h2 id="setup">Setup</h2>


Once the application is up and running the first procedure is to run the libraries and the second cell of code. this cell would prompt the user for 2 inputs the first being the starting point of the canvas and the second being the ending point of the canvas. this is to calibrate the scale of the drawing for whatever canvas this program is being used for

<p align="center">
   <img width="600" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20171811.png"> 
  </p>
  
The third step is to input the location of the image to be drawn, **Note** that this program has trouble drawing complex images and is better suited for cartoons and line art. Once the program is ran,  an initial mouse press is required(this is used to go to the tab of the drawing canvas) and the mouse will return to the staring position that was done in the initial press in cell 2.

<p align="center">
   <img width="500" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20171837.png"> 
&nbsp;&nbsp;&nbsp;&nbsp;
 <img width="200" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/For%20Testing.jpg"> 
 &nbsp;&nbsp;&nbsp;&nbsp;
 <img width="600" src="https://raw.githubusercontent.com/tyrone890123/Drawing-Printer/main/Assets/Screenshot%202021-06-19%20171956.png"> 
  </p>
  
  
The speed of the drawing can be adjusted in the `time.sleep()`. If there is an error in the execution of the program in cell 3, pressing the escape button on the keyboard would stop the drawing process.
  
  <p align="center">
   <img width="400" src="https://github.com/tyrone890123/Drawing-Printer/blob/main/Assets/drawingdemo.gif?raw=true"> 
  </p>

<h2 id="revisions">Revisions</h2>

 - June 19, 2021 Version 1 pushed

