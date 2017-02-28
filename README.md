# Lane-Detection
Lane Detection - A naive implementation 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* The pipeline should work on images and video stream

---

### Reflection

### PipeLine Description 

**Image Processing Pipeline**

1. Read Image 
2. Convert the image to Grayscale 
3. Apply Gaussian Blur 
4. Use Canny Edge Detection to detect edges 
5. Select the Region of Interest 
6. Using Hough Transform draw the line 
7. Apply weighted image to display both the original line and 

**Extrapolating the lines**

The draw_lines function extrapolates the lines detected by hough transforms. The draw line function performs the following:

1. Find the slopes for the left and right lines 
2. Use numpy "linalg.lstsq" function to find the left and right intercepts for the lines. 
3. Extend the lines using the slope and intercept returned from the average_lines function

### Shortcomings

1. The current pipeline would not work for steep curves 
2. Verticies for extracting the region of interest are currently hardcoded
3. Video streaming for steep curve is not optimized as yet and the processed video/detected line might be jittery

### Improvements to current pipeline 
1. The solution for video processing pipeline can be optimized by converting yellow lines to white lines 
2. A neural network/deep learning approach could automate the lane detection process 

