# Object-Detection-using-SIFT

This is an object detection program using SIFT which is a feature detection algorithm in computer vision to detect and describe local features in images. In this project I was able to detect my mobile phone as an object in front of the webcam. At first I drew a bounding box or a rectangular region of interest (ROI) in the image captured from the webcam. When the object which is to be detected comes inside the box is identifed and is being highlighted by drawing a green box around it.

Using SIFT I firstly detected interesting keypoints in the image. These are the areas of the image where variation exceeds a certain threshold and are better than edge descriptors. Then I created vector descriptors for these interesting areas. Scale invariance is achieved via the following process:
               
   1. Interest points are scanned at several different scales.
   1. The scale at which I meet a specific stability criteria, is then selected and is encoded by the vector descriptor.
   Therefore, regardless of the initial size, the more stable scale is found which allows me to be scale invariant. 
   
Here I have also introduced FLANN based Matcher for making a match between the target object and the template image. It contains a collection of algorithms optimized for fast nearest neighbor search in large datasets and for high dimensional features.

## Requires
   * Python
   * OpenCV
   * Numpy
   
## Output

When no object is there in front of the webcam.

![screenshot from 2018-11-17 19-35-10](https://user-images.githubusercontent.com/40036314/48661963-65e56700-eaa0-11e8-99d2-0486b9fe9f7f.png)

When object is inside the ROI, it is found.

![screenshot from 2018-11-17 19-35-46](https://user-images.githubusercontent.com/40036314/48661980-b957b500-eaa0-11e8-8528-fabb8bb3f1d6.png)
