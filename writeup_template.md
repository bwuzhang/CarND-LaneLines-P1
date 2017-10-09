# **Finding Lane Lines on the Road**

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"
[image2]: ./test_images_output/blur.png "Blur"
[image3]: ./test_images_output/edge.png "Edge"
[image4]: ./test_images_output/cropped.png "Cropped"
[image5]: ./test_images_output/hough.png "Hough"


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I ....

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image:

![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]
![alt text][image5]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be that it sometimes couldn't find any lanes when the dash lane marks are small. This only happen in some extreme cases and normally disappears when moving into the next frame. 

The another shortcoming is that my algorithm only works on road with small curvature. It can't adapt to more rapid turning roads.


### 3. Suggest possible improvements to your pipeline

The first one can be solve by taking the temporal info into consideration. Basically we can make a prediction from the previous frames about lane marks if none is detected in this frame.

To solve the second shortcoming, we need to find a way to model curve lines.
