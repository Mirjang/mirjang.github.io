---
layout: post
title: "Neural Rendering for Transparent Objects"
date: 2020-05-15 13:32:20 +0300
description: Neural rendering with neural textures that can handle transparent objects. # Add post description (optional)
img: grtransp/pipe.png  # Add image post (optional)
tags: [Neural Rendering, Neural Textures, Transparent Rendering, Texture Reconstrucion]
---

<!-- ![Pipeline]({{site.baseurl}}/assets/img/grtransp/pipe.png) <br><br> -->

Neural rendering combines classical rendering techniques with learnable elements. It has shown great potential in areas, where the geometry of an object cannot be obtained at a fine enough resolution for the object to be re-rendered using the classical pipeline. Neural rendering has also great success generating images from novel view points.

In this work we apply the deferred neural rendering technique to transparent objects and complex scenes. We use a classical algorithm known as depth peeling. This algorithm renders the scene multiple times and during each iteration stores and removes the nearest surface from the scene, by using a depth mask. For each depth peeling pass, we compute per-pixel UV-coordinates and use them to look up a neural texture, as is done in [Deferred Neural Rendering](https://niessnerlab.org/projects/thies2019neural.html). We then stack all these layers and pass them through a neural network to obtain a final image. This allows us to see through transparent objects, where the term "transparent" also includes objects with holes, that are covered by a simplified geometry. It also complicates the original deferred neural rendering problem, as our network not only has to learn a rendering function, but also how to perform a blending operation on multiple objects.

<p align="center">
<video class="video video-grid img-fluid" loop="loop" autoplay="" muted="" width="640" height="480" controls>
<source src="/assets/img/grtransp/Media2.mp4.webm" type="video/webm">
</video>
<video class="video video-grid img-fluid" loop="loop" autoplay="" muted="" width="640" height="480" controls>
<source src="/assets/img/grtransp/Media1.mp4.webm" type="video/webm">
</video>
</p>

Advisor: [Justus Thies](https://justusthies.github.io/)<br>
Supervisor: [Matthias Nießner](https://niessnerlab.org/)

[Presentation](https://mirjang.github.io/assets/radner_GR_transparent_pres.pdf)<br>
[Paper](https://mirjang.github.io/assets/radner_GR_transparent.pdf)<br>
[Github](https://github.com/Mirjang/TransparentNeuralRendering) <br>
