### Title: Instance Normalization: The Missing Ingredient for Fast Stylization

#### Author: Dmitry Ulyanov, Andrea Vedaldi, Victor Lempitsky

#### Published: Arxiv

#### Code: Almost all deep learning frameworks implement Instance Normalization operation


## Why
The qualitative results of fast stylization methods does not match the results of the origin slow stylization method.

## What
Using instacne normalization instead of batch normalization.

## How
> Just introduce the definition of instance normalization

A simple version of contrast/instance normalization

$$y_{tijk} = \frac{x_{tijk}}{\sum_{l=1}^W\sum_{m=1}^Hx_{tijk}}$$

The definition of instance normalization

$$y_{tijk} = \frac{x_{tijk} - \mu_{ti}}{\sqrt{\sigma_{ti}^2} + \epsilon}$$

$$\mu_{ti} = \frac{1}{HW}\sum_{l=1}^{W}\sum_{m=1}^Hx_{tilm}$$

$$\sigma_{ti}^2 = \frac{1}{HW}\sum_{l=1}^{W}\sum_{m=1}^H(x_{tilm} - m\mu_{ti})^2$$

But I think there should not be a $m$ before $\mu_{ti}$.

## Results
The qualitive results are better than the origin fast stylization methods.


## Thoughts
Small tricks are very important in training.