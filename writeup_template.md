# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Attempt challenge section .


---

### Reflection

### 1.My Initial Steps 
* Intially I went converting the image to gray scale. HSV was attempted to attempt challenge section . After grayscale , blurring and Canny edge detection was done. Rest is as per the currrent pipeline.

### 1. Pipeline

My pipeline consists of 
* Converting an image to HSV. 
* Thresholding the HSV image to two different yellow and white masks seperately and combining them
* Applying the mask on the orginal image to get an image with only contours of interest
* Canny Edge Detection on mask applied original image. 
* Cutting of ROI
* Applying Hough Transform
* Working on functions to support to draw lines. 

### 2. Modifying the draw_lines() function.

The draw_lines function 
* Prior In order to draw a smooth line on both lanes , we need to find the slope and intercept to get a pair of (x y) points for both the lanes . This was achieved using function find_slopes_and_min_max_points. Return the points in a list as (x0, y0) and (x1,y1) for both the slopes.
. Averaging was done for a smooth rendering of the red line marks from frame to frame. THis was achieved using getaveragexy function.


### 3. Identify potential shortcomings with your current pipeline

* A white vechile right in front of the vehicle can cause trouble I guess so. 

### 4. Challenge 
* Attempted challenge. The result does not give a smooth rendering


