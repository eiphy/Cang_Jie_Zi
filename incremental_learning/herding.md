# Dynamic Weight Herding

## Introduction

This herding algorithm aims to form a subset of data set such that the mean of the **subset** could represent the mean of **full set** best and reduction of subset's size cause minimal influence.

This algorithm is firsly proposed by Welling [Herding Dynamic Weights to Learn](https://arxiv.org/abs/1611.07725) and is applied in later incremental learning techniques. 
[iCaRL](https://arxiv.org/abs/1611.07725) delelopes an incremental classifier by the distance between input data and classes' centers. 
[eeil](https://openaccess.thecvf.com/content_ECCV_2018/html/Francisco_M._Castro_End-to-End_Incremental_Learning_ECCV_2018_paper.html) uses this algorithm to generate exampler set.
These two approaches both use the generated subset to represent the whole dataset.

## Algorithm
A algorithm illustration could be found in iCaRL as following:

![Herding Algorithm](/image/herding_alg.png)

The implementation could be down as following:

Fristly, norm the feature vector $\varphi(x)$ so that the distance between the center of the data set and the center of subset could be represented as $<w, \varphi(x)>$. 
The vector $w$ is caculater as follow:

$$
w=w+\mu-\varphi(x^*)
$$

The $\varphi(x^*)$ is the chosen data point for this iteration.
