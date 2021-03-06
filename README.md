# Heart tissue monitor

This is a project I'm working on during a 2 month lab rotation in a cardiology/physics lab. My goal is to create a real time frequency analyzer for 2D heart tissue using python and opencv. The ultimate goal is to eventually create an interactive GUI and save the frequency data without having to store large amounts of video for data analysis.  

## Current progress:

* Using the Opencv background subtraction algorithm I am able to find the average pixel intensity of a video. The higher the pixel        intensity the higher the displacement of cardiomyocytes. This will create peaks which show frequency.  
https://docs.opencv.org/3.4/db/d5c/tutorial_py_bg_subtraction.html

* I Used PyQtGraph to dynamically plot the frequency by graphing mean pixel intensity obtained by the background subtraction algorithm.
http://www.pyqtgraph.org/


* The program will save the data when 's' is pressed to a text document with the date, FPS, and total number of frames analyzed. A figure     is also saved along with the data using matplotlib in order to quickly visualize and extract the wanted data out of the text file. 

## Current goals
1) Clean the code, because I don't have the experience to structure code proficiently.

2) Add a PyQt button to save the data instead of pressing 's', because it is sticky and does not always save the data. 

3) Add a peak detection function which produces a sound whenever the pixel intensity peaks in the dynamic plotter. 

4) Allow mouse interaction, letting you pick a region of interest on the origianl video window and only applying the background subtraction on that area. 

5) Have an option to save video when you want, possibly with the video writing functions in opencv along with a toggle switch.

### Example of the current analyzer
<a href="https://imgflip.com/gif/31sb1j"><img src="https://i.imgflip.com/31sb1j.gif" title="made at imgflip.com"/></a>
