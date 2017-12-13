### Title: FaceNet: A Unified Embedding for Face Recognition and Clustering

#### Author: Florian Schroff, Dmitry Kalenichenko, James Philbin

#### Published: CVPR 2015

#### Code: [Tensorflow Version](https://github.com/davidsandberg/facenet)



## Why

Previous methods on face recognition and face verification can not scale.

## What

Propose a system called FaceNet that directly learns a mapping from face images to a compact Euclidean space where distances directly correspond to a measure of face similarity.

## How

#### utilize triplet loss. 
The constraint is $|| f(x_i^a) - f(x_i^p)||_2^2 + \alpha < ||f(x_i^a) - f(x_i^n)||$, and the loss function is $\sum_i^N[||f(x_i^a) -f(x_i^p)||_2^2 - ||f(x_i^a) - f(x_i^n)||_2^2+ \alpha]$ where $x^a$ means anchor, $x_p$ means positive, $x^n$ means negative. We try to minimize the distance between an anchor to the positive, and maximize the distance between the anchor to the negative.

#### using online triplet selection algorithm

selecting triplet between a batch instead of sampling from the whole training datasets, so they can generate triplet online.

#### try different network structure

They have tried the variants of ZF network and the Google's Inception.



## Results

Achieved 99.63% on LFW face verification and 95.12% in YouTube Faces DB.

## Thoughts

The triplet loss can not only using in generating face vector description, but also in image similarity.