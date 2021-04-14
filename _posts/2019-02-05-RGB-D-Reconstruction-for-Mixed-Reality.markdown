---
layout: post
title: "RGB-D Reconstruction for Mixed Reality"
date: 2019-02-05 13:32:20 +0300
description: RGB-D reconstruction based on Kinect Fusion. The environment mesh is passed to Unity to allow for real-time interaction # Add post description (optional)
img: 3dscan/table_unity.png  # Add image post (optional)
tags: [3D Reconstruction, Mixed Reality, RGB-D, Games]
---

For the [3D Scanning & Motion Capture](https://niessnerlab.org/teaching.html) at TUM course we implemented a realtime 3D reconstruction algorithm based on Kinect Fusion. Additionally we show, how such an algorithm can be used for Mixed Reality by implementing an interface between our implementation (C++, CUDA, DirectCompute) and the Unity game engine. The implemented Unity "game" gets the current position and scene geometry at each update. 
Results:

![Original Scene]({{site.baseurl}}/assets/img/3dscan/table.png)
![Interaction]({{site.baseurl}}/assets/img/3dscan/table_unity.png)
![Reconstruction]({{site.baseurl}}/assets/img/3dscan/table_reconstruction.png)


Team Members: Patrick Radner, [Juan Raul Padron Griffe](https://github.com/juanraul8), [Wojciech Zielonka](https://github.com/Zielon), [Baris Yazici](https://github.com/BarisYazici)<br> 
Instructors: [Angela Dai](https://www.3dunderstanding.org/), [Justus Thies](https://justusthies.github.io/)

[Github](https://github.com/Zielon/3DScanning) <br>
[Poster](https://mirjang.github.io/assets/3dscan_poster.pdf)

