### Title: A Light CNN for Deep Face Representation with Noisy Labels

#### Author: Xiang Wu, Ran He, Zhenan Sun, Tieniu Tan

#### Published: Arxiv

#### Code: [Caffe](https://github.com/AlfredXiangWu/face_verification_experiment) [PyTorch](https://github.com/AlfredXiangWu/LightCNN)



## Why
1. Face Recognition is an old problem.
2. There are many noisy labels in massive datasets. 

## What
1. Propose MFM(Maximum Feature Map) to reduce parameters and seperate the informative signals from noisy signals.
2. Propose 3 different networks(lightcnn4, lightcnn9, lightcnn29) and analysis different effects.
3. Propose a semantic boostrapping method to re-label datasets.

## How
### MFM Definition
MfM 2/1
$$\hat{x}_{ij}^k = \max(x_{ij}^k, x_{ij}^{k+N})$$



MFM 3/2

$$\hat{x}_{ij}^{k_1} = \max(x_{ij}^k, x_{ij}^{k+N}, x_{ij}^{k+2N})$$

$$\hat{x}_{ij}^{k_2} = median(x_{ij}^{k}, x_{ij}^{k+N},x_{ij}^{k+2N})$$


## Results



## Thoughts
### Differences between Verification and Identification
Verification: Given an image of a person and another image or a number of images of a person, check whether they are the same person.
Identificaiton: Given an image of a person, check whether this person enrolled in your system and is so, identify who he is.
Recognition: this term is a generic term, ofthen contains both above.