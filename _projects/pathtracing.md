---
layout: project
title: "Analysis of the Path Tracing rendering method on CPU and GPU"
date: 2020-04-30
categories: [projects]
tags: [project, c++, path tracing, CUDA, OpenMP]
excerpt: "Path Tracing performance architecture analysis"
comments: false
---

This is my final degree project with which I got a grade of 10. The project consists of the implementation of a Path Tracer for both CPU, using OpenMP, and GPU, using CUDA. The objective of the project was to analyze which architecture provides us with more performance in an application of these characteristics. This application allows the creation of 3D scenes through 3D models defined in OBJ format. These models can be defined by their material: diffuse, metallic or dielectric (e.g. glass). Also, we can define a texture for the model. Currently, there is no support for models with more than one defined texture. We can also make use of skyboxes.

For each implementation, we have a version that uses a Bounding Volumes Hierarchy to optimize the query of if a ray has hit an object or not. Besides, for the ray/triangle calculation, we have used the Möller-Trumbore algorithm, which is characterized by its efficiency, both in memory expenditure and in calculations.

Finally, a series of denoising filters were also implemented to improve the quality of the output image.

<figure>
	<img src="{{site.url}}/pathtracing/cornell_deer.png">
</figure>
