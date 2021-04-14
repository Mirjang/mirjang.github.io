---
layout: post
title: "Video Synthesis from a Single Image"
date: 2020-12-15 13:32:20 +0300
description: Master´s Thesis on video prediction from images using a style-based RNN architecture. # Add post description (optional)
img: mtvid/vids/sky/title.gif # Add image post (optional)
tags: [GANs, Video Generation, Video Prediction]
---

<script>
MathJax = {
    tex: {
    inlineMath: [
        ['$', '$'],
        ['\\(', '\\)']
    ]
    }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

<!-- Bootstrap core CSS -->
<link href="vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">

<!-- Custom fonts for this template -->
<link href="vendor/font-awesome/css/font-awesome.min.css" rel="stylesheet" type="text/css">
<link href="vendor/simple-line-icons/css/simple-line-icons.css" rel="stylesheet" type="text/css">
<link href="https://fonts.googleapis.com/css?family=Lato:300,400,700,300italic,400italic,700italic" rel="stylesheet"
type="text/css">

<!-- Custom styles for this template -->
<link href="css/landing-page.min.css" rel="stylesheet">

<h2>Abstract</h2>
<p align="justify">
In this work a novel architecture is developed to perform video prediction. In particular the task of "bringing landscape images to live" is investigated. This is an especially challenging video prediction task, as only a single input image is given and the model has to predict what might happen next in the scene, for example clouds moving or flowing rivers and waterfalls. The changes per frame in these types of videos are usually very small detailed. As no flow or segmentation is given the model also has to learn, which image elements to animate. 
The proposed architecture combines recurrent, feature pyramid architectures from previous works such as DVD-GAN with styled convolutions introduced by StyleGAN to predict the final video. 
A new dataset for the task of "bringing landscape images to live", which focuses on fine details rather than global changes. The proposed model is evaluated against state-of-the-art baselines and is shown to also work on standard video prediction benchmarks, while requiring smaller compute resources for training.      
</p>

<img src="/assets/img/mtvid/style_arch.png" style="width:512px;height:512px;"/>
<p>Video prediction architecture based on <a href="https://arxiv.org/abs/1912.04958">StyleGAN2</a> and <a href="https://arxiv.org/abs/1907.06571">DVD-GAN</a>. 
    The green arrow indicates the predicted style vector.
    The dashed red line logically separates the generator into an encoder and decoder part.
</p>

<h2>Showcase: Sky Timelapse Dastaset</h2>
<div class ="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/sky/fake_block9.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/sky/fake_block45.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/sky/fake_block113.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/sky/fake_block133.mp4.webm" type="video/webm">
    </video>
</div>

<h2>Showcase: Custom Dastaset</h2>
<div class ="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block7.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block25.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block40.mp4.webm" type="video/webm">
    </video>
</div>
<div class ="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block77.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block128.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block117.mp4.webm" type="video/webm">
    </video>
</div>
<div class ="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block164.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block177.mp4.webm" type="video/webm">
    </video>
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/style128_sample/fake_block185.mp4.webm" type="video/webm">
    </video>
</div>


<h2>Comparison</h2>
<div class="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
        <source src="/assets/img/mtvid/vids/bair_cmp/style/out.webm" type="video/webm">
    </video>
</div>
<div class="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
    <source src="/assets/img/mtvid/vids/bair_cmp/dvd/out.webm" type="video/webm">
    </video>
</div>
<p>Comparison between our method (top) and a down-scaled version of DVD-GAN (bottom) on the bair robot pushing dataset.</p>

<h2>Showcase: GauGAN videos</h2>
<div class="row">
    <video class="video video-grid img-fluid" loop="loop" autoplay="" muted="">
        <source src="/assets/img/mtvid/vids/gau_block.webm" type="video/webm">
    </video>
</div>
<p>
Video prediction on images created with <a href="https://www.nvidia.com/en-us/research/ai-playground/"><b>GauGAN</b></a>.
The video prediction model was trained on our custom dataset. 
</p>

Advisor: [Justus Thies](https://justusthies.github.io/)<br>
Supervisor: [Matthias Nießner](https://niessnerlab.org/)

[Presentation](https://mirjang.github.io/assets/radner_mt_vids_pres.pdf)<br>
[Paper](https://mirjang.github.io/assets/radner_mt_vids.pdf)<br>
[Project Page](https://mirjang.github.io/mt_videosynthesis/)<br>
[Github](https://github.com/Mirjang/mt_videosynthesis) <br>
