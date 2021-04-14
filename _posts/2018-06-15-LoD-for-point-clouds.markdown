---
layout: post
title: "Level of Detail Generation for Point Clouds"
date: 2018-06-15 13:32:20 +0300
description: Bachelors thesis exploring methods for LoD generation for point clouds # Add post description (optional)
img: ba/xyzrgb_dragon.png # Add image post (optional)
tags: [Computer Graphics, Point Clouds, DirectX]
---

With the increasing quality of 3D models the conventional approach of representing 3D
models as a closed polygonal surfaces looses efficiency. Point Clouds offer an alternative
by only using point samples of the 3D surface. These samples do not require connectivity
information, drastically simplifying the rendering process. In addition, data from 3D
Scans, LIDAR, etc. is often only available as point data, and would otherwise have to
be converted into a polygonal model. Point clouds can often consist of hundreds of
millions or even billions of samples. It is therefore necessary to find a way to simplify
regions that are further away from the camera in order to not draw an entire dataset
every frame. This is commonly known as Level of Detail.
This Thesis revisits the sub sampling approach presented in Potree. Afterwards we
explore clustering based simplification techniques as a way to not only use the position
of samples, but also take advantage additional information such as curvature and color.
Human-made objects often contain planar surfaces. By using geometric information as
a criterion for creating our level of detail hierarchy, we manage to drastically reduce
the sample density in such planar regions, while still being able to conserve complex
geometries.


Advisor: Henrik Masbruch<br>
Supervisor: Prof. Dr. Rüdiger Westermann <br>

[Github](https://github.com/Mirjang/BA_PointClouds)<br>
[Presentation](https://mirjang.github.io/assets/radner_ba_points_pres.pdf)<br>
[Document](https://mirjang.github.io/assets/radner_ba_points.pdf)<br>
