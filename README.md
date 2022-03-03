<div align="center">
<h1>Optical Flow to track object Movement</h1>
</div>

<h1>Objectives</h1>
The objectives as part of this project are:
<ol>
<li>To plot the vector field for objects in each frame of a video. The video consists of the movement of cars in a highway</li>
<li>Perform background subtraction to view the movement of the cars alone.</li>
</ol>

<h1>Use optical flow to plot the vector field to track movement of objects in each frame</h1>

<h2>Conept of Optical Flow</h2>
Optical flow refers to the per pixel motion estimation between two consecutive frames in a video. The motion can be estimated by using the Lucas-Kanade method which works on the assumption that nearby pixels have the same displacement direction.

##Algorithm
1. Read the first frame of the video and use the shi-tomasi corner detection algorithm to store the corner
points.
2. Read the subsequent frames and use the inbuilt function cv2.calcOpticalFlowPyrLK() to extract the
points and the error.
3. The lines are drawn connecting the points from the current frame to the previous frame to represent
the vector field.

<p align="center">
<img src="https://github.com/jayesh68/LUkas-Kadane-Tracker/blob/main/optical%20flow.png"/>
</p>

<h1>Background Subtraction</h1>
The background removal was performed by using the function cv2.bgsegm.createBackgroundSubtractorMOG() and applying it to every frame of the video. This
would create a grayscale image with the background of the highway being darkened and the cars clearly seen as it drives along the highway.
<p align="center">
<img src="https://github.com/jayesh68/LUkas-Kadane-Tracker/blob/main/background%20subtraction.png"/>
</p>

<h1>Project Results</h1>
<ul>
  <li>Optical FLow: https://youtu.be/KgKM0lsJvDU</li>
  <li>Background Subtraction: https://youtu.be/RiwrNDQIxD0</li>
</ul>
