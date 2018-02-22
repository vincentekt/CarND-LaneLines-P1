# **Finding Lane Lines on the Road** 
![image](resources/output.png)
---

### Reflection

### 1. Pipeline.

My pipeline consisted of 5 steps.

1. Grayscale
![image](resources/gray_scale.png)
2. Gaussian blur
![image](resources/gaussian_blur.png)
3. Canny edge
![image](resources/canny_edge.png)
4. Masked edges
![image](resources/masked_edges.png)
5. Hough transform
![image](resources/hough_transform.png)
![image](resources/output.png)
 

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be the non-smooth changes of coefficients of linear regressor. 
That has regretfully caused the lines to be quite jumpy along with some inaccuracy.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to smoothen the changes of the coefficients by performing time-series prediction to 
assist the current observation. Clipping on the change would be helpful too.