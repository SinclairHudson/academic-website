---
title: "Machine Learning Engineer at DarwinAI"
collection: experience
permalink: /experience/2021-darwinai
date_start: 2021-05-03
date_end: 2021-08-28
location: "Waterloo, Ontario, Canada"
---

Focusing on building models for manufacturing clients.


## Defect Detection is Anomaly Detection
When I was at DarwinAI, the team was largely focused on solving the problem of defect detection using computer vision.
Essentially, a lot of our clients would have parts coming off a manufacturing line, and they wanted to be able to automatically detect defects.
The team often solved this problem using classification, sometimes multi-class.
It worked fairly well, but there were some issues.
To start, there was always a massive class imbalance; almost all the parts were not defective.
Also, some detects, like a foreign object in the part, were very diverse and so certain class instances looked nothing alike.
One of the things I'm most proud of during my time at DarwinAI was tackling this challenge.
I explained to the reserach team that I thought that defect detection was better cast as an anomaly detection problem, not a classification problem.
After some discussion, I was allowed to spin up a research repository for the company, exploring unsupervised learning approaches for defect detection.
The main idea I had was to train the autoencoder on exclusively "normal" images, to achieve a low reconstruction loss on those sorts of images.
The autoencoder is not prepared to reconstruct anomalous images (defective parts), and so a high reconstruction loss correlates with an anomaly.
I implemented many autoencoders from current research, and tested their performance on client and public datasets.
This unsupervised approach to defect detection had the advantage of not requiring labeled data of every defect. 
It was also robust to different, even unseen defect modalities, so long as they were visually different from nominal inputs.

DarwinAI was acquired by Apple in 2024.
