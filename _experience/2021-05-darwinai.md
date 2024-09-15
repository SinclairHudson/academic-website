---
title: "Machine Learning Engineer at DarwinAI"
collection: experience
permalink: /experience/2021-darwinai
date_start: 2021-05-03
date_end: 2021-08-28
location: "Waterloo, Ontario, Canada"
---

Machine Learning Engineer, focused on building models for manufacturing clients.


## Defect Detection is Anomaly Detection
When I was at DarwinAI, the team  was largely focused on solving the problem of defect detection using computer vision.
Essentially, a lot of our clients would have parts coming off the line, and they wanted to be able to automatically detect defects.
The team often solved this problem using classification, sometimes multi-class. It was 
One was for anomaly detection in images, using autoencoders.
I implemented many autoencoders from current research, and tested their performance on client and public datasets.
The main idea there is to train the autoencoder on exclusively "normal" images, to achieve a low reconstruction loss on those sorts of images.
The autoencoder is not prepared to reconstruct anomalous images, and so a high reconstruction loss correlates with an anomaly.
This unsupervised approach to anomaly detection will likely be critical in defect detection cases, since it flags new anomalies as they arise in the manufacturing process; not only the ones in the training set.


