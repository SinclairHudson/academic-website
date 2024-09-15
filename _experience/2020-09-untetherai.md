---
title: "Software Engineer at UntetherAI"
collection: experience
permalink: /experience/2020-untetherai
date_start: 2020-09-03
date_end: 2022-12-22
location: "Remote in Canada"
---

Developing a Python library to optimize and process neural networks for an accelerated inference chip.

## Integer only!
UntetherAI's flagship chip at the time was integer-only, by design.
Specifically, it was an "at-memory compute" chip, and all of the cores could only do int-8 operations.
Any activation or weight could only have 256 unique values.
This experience really opened my eyes to the world of DNN optimization and quantization.
The math that enables int-8 quantization to work is really cool, and I learned a lot about how neural networks run, down to the hardware level.
My team was the framework team; we built a Python library that helped users get their neural networks ready for deployment on this special chip.
This meant finding optimal quantization schemes, quantization-aware training, debugging, etc.
Our main pipeline took in a pre-trained model, trained it a little bit to make sure the quantization noise wouldn't tank performance, and then prune and pre-process the graph before handing it off to the compiler.

## Non-Max Suppression
One of the things I'm most proud of from my time at Untether is developing a version of non-max suppression (NMS), that used integer-only operations.
At the time, NMS was the dominant post-processing step after single-shot object detectors.
UntetherAI would do all the CNN computation on-chip, but then pass the output to the host to decode bounding boxes and perform NMS.
This really slowed things down for the single-shot detector (SSD) pipeline; the CPU on the host machine was the bottleneck.
I spent a lot of time figuring out how to do all the steps of NMS with only 256 unique values; the bounding box decoding, the sort, the selection of boxes.
It was a cross-team effort, and I had a few talks with the chip design gurus at the company, about the feasibility of certain algorithms.
In the end though, it worked out, and we had a (pseudo) NMS algorithm that would be able to run on chip. 
Based on our clock-cycle estimations, it would remove the CPU bottleneck completely and take SSD pipelines from hundreds of frames per second to thousands of frames per second.

## Vim era
This is also where I started learning how to use vim, and how to use vim properly.
Big shout out to my mentor Ingo; he showed me what 20 years of vim experience looks like, and encouraged me constantly. 🐐
