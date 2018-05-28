# **Finding Lane Lines on the Road**

![Project 1](https://img.shields.io/badge/Computer%20Vision%20Fundamentals-Finished-green.svg?longCache=true&style=for-the-badge)

---

The goals  of this project are the following:

* Make a pipeline that finds lane lines on the road

---
[//]: # (Image References)

[image0]: ./test_images/solidWhiteCurve.jpg
[image1]: ./examples/white_yellow_image.jpg 
[image2]: ./examples/gray_image.jpg 
[image3]: ./examples/edges.jpg
[image4]: ./examples/final_image.jpg

![image0]

#### The image processing pipeline consisted of four steps
1. All the colours except **white** and **yellow** were removed from the image. 
![image1]

2. The masked image was converted to grayscale
![image2]

3. **Canny Threshold** of the image was taken
![image3]

4. **Hough Line Transform** was applied to the image in the selected region of interest and lines were drawn on the  original image .
![image4]


![final output](https://media.giphy.com/media/7zy01fZ1XLbdxCostX/giphy.gif)

#### Some potential shortcoming with the pipeline
- The region of interest is static at the moment and is being hard coded. This can lead to potential issues in the real world.
- The lines drawn are somewhat jittery. This can be improved by using **np.polyfit** instead of manually averaging the lines. 
- The pipeline is not very robust in the areas of extreme brightness. 
- As the color makes are hardcoded different intensity/color of the lane lines could lead to issues.
- The challenge video lanes are being detected as straight lines instead of curves.

#### Possible improvements
- The region of interest should be dynamically selected. 
- Dynamic feature selection from the image will lead to a more robust pipeline.
- Detecting curves in the challenge video instead of straight lines will lead to more accurate drawing of the lanes. 
