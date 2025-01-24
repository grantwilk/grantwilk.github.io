---
title: 3D Wireframe Renderer
description: A simple 3D wireframe render engine capable of rendering STL models.
date: 2021-05-01 00:00:00 -0600
image:
  path: /assets/img/posts/2021-05-01-3d-wireframe-renderer/3d-wireframe-renderer.jpg
---

An orthographic 3D wireframe renderer, written from scratch and compiled for Linux.

As an extension of the [2D Drawing App](grantwilk.github.io/posts/2021-04-01-2d-drawing-app) I made for my Computer Graphics course, I decided to add some 3D rendering capabilities. I had the opportunity to dive deep into 3D transformations to produce a 3D orthographic wireframe renderer with mouse control. Having been a bit of a 3D junkie since 8th grade, this was an amazing project to work on. I've wondered how rendering engines work for so long now, and to finally have some degree of an answer is incredibly satisfying. 

I later revisited this project in my senior year GPU programming course and implemented some CUDA kernels to further accelerate the rendering process. With this, I was able to improve rendering capabilities from hundreds of tris per frame to millions of tris per frame. This was super exciting given the whole thing is built on X11. 

This demo video doesn't show the CUDA accelerated version, but it still gets the idea across!

{% include embed/youtube.html id='-4-Ggb3o0h4' %}