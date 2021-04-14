---
layout: post
title: "RGB Face Tracking and Reconstrucion"
date: 2020-02-08 13:32:20 +0300
description: Real-time 3D Face Tracking and Reconstrucion from RGB video using a morhpable model. # Add post description (optional)
img: facerec/model.png  # Add image post (optional)
tags: [Morphable Model, Face2Face, Face Reconstrucion]
---

For the 3D-Scanning and Spatial Learning practical course we implemented an (almost) real-time face reconstruction algorithm based on [Face2Face](https://niessnerlab.org/projects/thies2016face.html). The algorithm takes the RGB-stream from a webcam as input and fits a parametric model to the face using differential rendering and LM optimization. Facial keypoints are predicted using DLIB and serve as additional input for the optimization. The rendering pipeline was implemented in OpenGL and the optimization was done using CUDA. 

![Editor View]({{site.baseurl}}/assets/img/facerec/Obama.gif) <br><br>
![VR View]({{site.baseurl}}/assets/img/facerec/Trudeau.gif) <br><br>


Team Members: Patrick Radner, [Wojciech Zielonka](https://github.com/Zielon), [Mustafa Işık](https://www.mustafaisik.net/)<br>
Instructor: [Justus Thies](https://justusthies.github.io/)

<br>
[Github](https://github.com/isikmustafa/face-tracking) <br>
